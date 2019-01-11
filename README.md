# mi_e20

������ ��� ����������/�������� ��������� ������ ��� ������-�������� Xiaomi XiaoWa E20.
�������� ���������� - �������� ���������������� �������� �������.
��������� ��� �������� �������� 1.3.0_0542.
������ ������� ��� 3 ������ python, �� 2-�� �� ����������.

<b>��������!!</b> ��� ����������� �� ��������� �� ���� ����� � ����, � �� ������� ������ ��������� ������, ������ ���� �������� ��� ��������. � ���� ������ ������� ������� � ���������� ������� ������-�������� �� ��������, �� ��� �� ������, ��� � ��� ����� �����.

<H4>�������:</H4>

```
unpack -p <dir> -f <file>
pack -p <dir>
serv --ip <IP> --port <PORT>
```


<H4>����������:</H4>

1. ���������� ������������ �������� �����. ������ ������������ � �������� �� ���������� ������, ��� ����������� ���������� ��������� ������ � ���. 
�� ������� ������ �� �������� �� ��� <a href="https://awsbj0.fds.api.xiaomi.com/sapphire/app/voice-pkg/package/english.pkg">english.pkg</a>

2. ������������� ����� � ��������� ����������, �� ��������� "out".
```
python mi_e20 unpack -f english.pkg
```

3. ��� ����� ����� � ���������� ������� � ������� �� ������ � ������. �������� ��������� ������� �������� - "0.mp3", �������������� ��� ������� �� ��������, �������� ���� ����.
�����! �������� ���������� ������ � ����������� ������� ������������ �����, ������� ���������� "mp3".

4. ������������. ���� out.pkg ����� ������ � ���������� �� ��������.
```
python mi_e20 pack
```

5. ��� ������ ������ ��������� ��� ������, � �������� ������� �������� �����. �������� ����� ��������� ������ ��� ������. � �������� IP ��������� ��� IP � ��������� ����. ��� ������� �� 80 ����� �������� ����������� ����� ��������������.
```
python mi_e20 serv --ip 192.168.1.111 --port 80
```

6. � ������� ���������� <a href="https://github.com/rytilahti/python-miio">python-miio</a> ���� ������� �� �������� ������.
��� ������������ ip �������� (�������� 192.168.1.125) � ����� ��������� ���� � ��� ����� (�������� 6d373af1e425a35705b812cd81d8a5b2).
��� �������� ip � ����� ����� ���������� � ������� ������ Roborock.
```
mirobo --ip=192.168.1.125 --token=6d373af1e425a35705b812cd81d8a5b2 raw_command user.dnld_install_sound '{"url":"http://192.168.1.111/out.pkg", "sver":1, "md5":"fc8f45999775089449019df9dbc3b2a9", "sid":3}'
```
� ������ ������ "sver" � "sid" ������ ��������� � �������� � �� ������ �� �����. "md5" ������� �� ���������, �� ����� ���� �����.
��� �������� ��������� ����� ��������������� ��������.
```
mirobo --ip=192.168.1.125 --token=6d373af1e425a35705b812cd81d8a5b2 raw_command  get_sound_progress
```

<a href="http://4pda.ru/forum/index.php?showtopic=901809">���� �� 4PDA</a>
