---
description: Beschreibt die in der Header Datei "Winerror. h" definierten Fehlercodes 0-499 und ist für Entwickler bestimmt.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: System Fehler Codes (0-499) (Winerror. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861204"
---
# <a name="system-error-codes-0-499"></a>System Fehler Codes (0-499)

> [!NOTE]
> Diese Informationen sind für Entwickler gedacht, die Systemfehler Debuggen. Bei anderen Fehlern, wie z. b. Problemen mit Windows Update, finden Sie eine Liste der Ressourcen auf der Seite [Fehlercodes](system-error-codes.md) .

In der folgenden Liste werden die [Systemfehler Codes](system-error-codes.md) (Fehler 0 bis 499) beschrieben. Sie werden von der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) -Funktion mit dem Flag " **Format \_ Message \_ from \_ System** ".

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**Fehler \_ erfolgreich**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Der Vorgang wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**\_ungültige \_ Funktion.**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Falsche Funktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**Fehler \_ Datei \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Die angegebene Datei wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**der Fehler \_ Pfad wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Das System kann den angegebenen Pfad nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**Fehler \_ zu \_ viele \_ geöffnete \_ Dateien**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Das System kann die Datei nicht öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**Fehler \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Zugriff verweigert.“


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**Fehler bei \_ ungültigem \_ handle**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Das Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**Fehler-Arena wurde durchlaufen \_ \_**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Die Speicher Kontroll Blöcke wurden zerstört.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Für die Verarbeitung dieses Befehls sind nicht genügend Speicherressourcen verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**\_ungültiger \_ Block**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Die Speicher Steuerungs Block-Adresse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**Fehler \_ hafte \_ Umgebung**
</dt> <dd> <dl> <dt>

10 (0xa)
</dt> <dt>



Die Umgebung ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**fehlerhaftes \_ \_ Format**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Es wurde versucht, ein Programm mit einem falschen Format zu laden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**Fehler bei \_ ungültigem \_ Zugriff**
</dt> <dd> <dl> <dt>

12 (0xc)
</dt> <dt>



Der Zugriffs Code ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**\_ungültige \_ Daten**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Die Daten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**Fehler beim \_ outo-Memory**
</dt> <dd> <dl> <dt>

14 (0xe)
</dt> <dt>



Für diesen Vorgang ist nicht genügend Speicher verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**\_ungültiges \_ Laufwerk**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Das angegebene Laufwerk kann nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**\_Aktuelles \_ Verzeichnis für Fehler**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Das Verzeichnis kann nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**Fehler \_ beim \_ gleichen \_ Gerät**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Das System kann die Datei nicht auf ein anderes Laufwerk verschieben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**Fehler \_ keine \_ weiteren \_ Dateien**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Es sind keine weiteren Dateien vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**Fehler beim \_ schreiben \_ schützen**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Das Medium ist schreibgeschützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**Fehler \_ hafte \_ Einheit**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Das angegebene Gerät kann nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**Fehler \_ nicht \_ bereit**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Das Gerät ist nicht bereit.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**fehlerhafter \_ \_ Befehl**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Das Gerät erkennt den Befehl nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**Fehler \_ CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Datenfehler (zyklische Redundanz Überprüfung).


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**Fehler \_ hafte \_ Länge**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Das Programm hat einen Befehl ausgegeben, aber die Befehls Länge ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**Fehler \_ Suche**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Das Laufwerk kann keinen bestimmten Bereich oder Nachverfolgung auf dem Datenträger finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**Fehler \_ nicht \_ DOS-Datenträger \_**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Auf den angegebenen Datenträger oder die angegebene Diskette kann nicht zugegriffen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**Fehler \_ Sektor \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Das Laufwerk kann den angeforderten Sektor nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**Fehler \_ \_ in \_ Papier**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



Der Drucker ist nicht mehr im Papier.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**Fehler \_ Schreib \_ Fehler**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



Das System kann nicht auf das angegebene Gerät schreiben.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**Fehler beim \_ Lesen \_ des Fehlers**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



Das System kann das angegebene Gerät nicht lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**Fehler \_ gen \_ fehlgeschlagen**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Ein an das System angefügtes Gerät funktioniert nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**Verletzung der Fehler \_ Freigabe \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Der Prozess kann nicht auf die Datei zugreifen, da sie bereits von einem anderen Prozess verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**Fehler \_ Sperr \_ Verletzung**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



Der Prozess kann nicht auf die Datei zugreifen, da sie teilweise von einem anderen Prozess gesperrt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**Fehler \_ hafte \_ Festplatte**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



Die falsche Diskette befindet sich im Laufwerk. Fügen Sie %2 (Volumeseriennummer: %3) in Laufwerk %1 ein.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**Fehler \_ Freigabe \_ Puffer \_ überschritten**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Zu viele Dateien für die Freigabe geöffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**Fehler \_ handle \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Das Ende der Datei wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**Fehler \_ beim \_ \_ vollständigen Datenträger.**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



Der Datenträger ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**Fehler \_ nicht \_ unterstützt**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



Die Anforderung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**Fehler- \_ REM \_ nicht \_ auflisten**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Der Netzwerkpfad kann nicht gefunden werden. Überprüfen Sie, ob der Netzwerkpfad richtig ist und der Zielcomputer nicht ausgelastet oder ausgeschaltet ist. Wenn Windows den Netzwerkpfad noch immer nicht finden kann, wenden Sie sich an Ihren Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**Fehler beim \_ DUP- \_ Namen**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



Sie waren nicht verbunden, weil im Netzwerk ein doppelter Name vorhanden ist. Wechseln Sie beim beitreten zu einer Domäne in der Systemsteuerung zum System, um den Computernamen zu ändern, und versuchen Sie es noch mal. Wenn Sie einer Arbeitsgruppe beitreten, wählen Sie einen anderen Arbeitsgruppen Namen aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**Fehler \_ beim \_ netpath.**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



Der Netzwerkpfad wurde nicht gefunden.“


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**Fehler \_ Netzwerk \_ ausgelastet**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



Das Netzwerk ist ausgelastet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**Fehler \_ dev ist \_ nicht \_ vorhanden.**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



Die angegebene Netzwerkressource oder das angegebene Gerät ist nicht mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**Fehler \_ zu \_ viele \_ cmds**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



Der Netzwerk-BIOS-Befehls Grenzwert wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**Fehler beim \_ ADAP- \_ HDW. \_**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Es ist ein Hardwarefehler im Netzwerkadapter aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**Fehler bei fehlerhafter Netzwerk Zuweisung. \_ \_ \_**
</dt> <dd> <dl> <dt>

58 (0x3a)
</dt> <dt>



Der angegebene Server kann den angeforderten Vorgang nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**Fehler beim \_ unexp \_ net \_ Err.**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Unerwarteter Netzwerkfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**Fehler \_ hafte \_ REM- \_ ADAP**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



Der Remote Adapter ist nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**Fehler \_ printq \_ Full**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



Die Drucker Warteschlange ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**Fehler \_ kein \_ \_ spoolspeicher.**
</dt> <dd> <dl> <dt>

62 (0x3e)
</dt> <dt>



Der Speicherplatz zum Speichern der Datei, die gedruckt werden soll, ist auf dem Server nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**Fehler beim \_ Drucken \_ abgebrochen**
</dt> <dd> <dl> <dt>

63 (0x3f)
</dt> <dt>



Die Datei, die darauf wartet, gedruckt zu werden, wurde gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**NetName-Fehler wurde \_ \_ gelöscht.**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Der angegebene Netzwerkname ist nicht mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**Fehler beim \_ Netzwerk \_ Zugriff \_ verweigert**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Der Netzwerk Zugriff wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**fehlerhafter \_ \_ \_ Entwicklungstyp**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



Der Netzwerk Ressourcentyp ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**Fehler bei fehlerhafter \_ \_ Netzwerk \_ Name**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



„Der Netzwerkname wurde nicht gefunden.“


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**Fehler \_ zu \_ viele \_ Namen.**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



Das namens Limit für die Karte des Netzwerkadapters für den lokalen Computer wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**Fehler \_ zu \_ viele \_ Sess**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



Das Limit der Netzwerk-BIOS-Sitzung wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**Fehler \_ Freigabe \_ angehalten**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



Der Remote Server wurde angehalten oder gerade gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**Fehler beim Zurücksetzen des Fehlers. \_ \_ \_**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



Zurzeit können keine weiteren Verbindungen mit diesem Remote Computer hergestellt werden, da es bereits so viele Verbindungen gibt, wie der Computer annehmen kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**Fehler beim \_ redir \_ angehalten**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



Der angegebene Drucker oder das angegebene Datenträger Gerät wurde angehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**Fehler \_ Datei \_ vorhanden**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



Die Datei ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**Fehler \_ beim \_ Erstellen**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Das Verzeichnis oder die Datei kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**Fehler \_ \_ i24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Fehler bei int 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**Fehler \_ aus \_ \_ Strukturen**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



Der Speicher zum Verarbeiten dieser Anforderung ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**Fehler \_ bereits \_ zugewiesen**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



Der Name des lokalen Geräts wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**Fehler \_ ungültiges \_ Kennwort**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



Das angegebene Netzwerkkennwort ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**Fehler bei \_ ungültigem \_ Parameter**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



„Der Parameter ist falsch.“


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**Fehler beim \_ net- \_ Schreib \_ Fehler.**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Im Netzwerk ist ein Schreibfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**Fehler " \_ keine \_ proc \_ Slots"**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



Das System kann zurzeit keinen anderen Prozess starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**Fehler \_ zu \_ viele \_ Semaphoren**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Ein weiteres System Semaphor kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**Fehler durch die \_ \_ \_ bereits \_ im Besitz von SEM**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



Das exklusive Semaphor ist im Besitz eines anderen Prozesses.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**Fehler " \_ SEM" \_ ist \_ festgelegt**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



Das Semaphor ist festgelegt und kann nicht geschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**Fehler \_ zu \_ viele \_ \_ Anforderungen für das Angleichen**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



Das Semaphor kann nicht erneut festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**Fehler \_ \_ beim \_ \_ Interruptzeit ungültig**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Exklusive Semaphoren können zur Interruptzeit nicht angefordert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**Fehler beim "-Besitzer". \_ \_ \_**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



Der vorherige Besitz dieses Semaphors wurde beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**Fehler \_ - \_ Benutzer \_ Limit für Benutzer**
</dt> <dd> <dl> <dt>

106 (0x6a)
</dt> <dt>



Fügen Sie die Diskette für das Laufwerk %1 ein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**Fehler Datenträger \_ \_ Änderung**
</dt> <dd> <dl> <dt>

107 (0x6b)
</dt> <dt>



Das Programm wurde beendet, weil keine Alternative Diskette eingefügt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**Fehler \_ Laufwerk \_ gesperrt**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



Der Datenträger wird von einem anderen Prozess verwendet oder gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**Fehler bei der \_ \_ Pipe.**
</dt> <dd> <dl> <dt>

109 (0x6d)
</dt> <dt>



Die Pipe wurde beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**Fehler beim \_ Öffnen. \_**
</dt> <dd> <dl> <dt>

110 (0x6e)
</dt> <dt>



Das System kann das angegebene Gerät oder die angegebene Datei nicht öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**Fehler \_ Puffer \_ Überlauf**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



Der Dateiname ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**Fehler Datenträger \_ \_ voll**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



There is not enough space on the disk.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**Fehler \_ keine \_ weiteren \_ Such \_ Handles**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Es sind keine weiteren internen Datei Bezeichner verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**Fehler \_ ungültiges \_ Ziel \_ handle**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



Der Bezeichner der internen Ziel Datei ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**\_ungültige \_ Kategorie**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



Der IOCTL-Befehl, der vom Anwendungsprogramm durchgeführt wird, ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**Fehler \_ beim \_ Überprüfen des \_ Schalters**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



Der Wert für den Schalter Parameter "Verify-on-Write" ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**Fehler \_ hafte \_ Treiber \_ Ebene**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



Der angeforderte Befehl wird vom System nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**Fehler-Befehl \_ \_ nicht \_ implementiert**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Diese Funktion wird auf diesem System nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**Fehler \_ - \_ buildtimeout**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Der Timeout Zeitraum für das Semaphor ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**Fehler \_ beim \_ Puffer.**
</dt> <dd> <dl> <dt>

122 (0x7a)
</dt> <dt>



Der an einen System Rückruf über gegebene Datenbereich ist zu klein.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**\_ungültiger \_ Name.**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



Die Syntax für den Dateinamen, den Verzeichnisnamen oder die Volumebezeichnung ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**\_ungültige \_ Ebene**
</dt> <dd> <dl> <dt>

124 (0x7c)
</dt> <dt>



Die System-aufrufsebene ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**Fehler \_ " \_ keine \_ Volumebezeichnung"**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



Der Datenträger weist keine Volumebezeichnung auf.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**Fehler \_ mod \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



Das angegebene Modul wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**Fehler \_ proc \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

127 (0x7f)
</dt> <dt>



Die angegebene Prozedur wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**Fehler beim \_ warten auf \_ kein \_ Kind**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Es sind keine untergeordneten Prozesse vorhanden, auf die gewartet werden soll.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**Fehler untergeordnetes Element \_ \_ nicht \_ fertiggestellt**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



Die Anwendung "%1" kann nicht im Win32-Modus ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**Fehler beim \_ direkt \_ Zugriffs \_ handle**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Es wurde versucht, ein Datei Handle für eine geöffnete Datenträger Partition für einen anderen Vorgang als eine unformatierte Datenträger-e/a zu verwenden


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**Fehler bei \_ negativer \_ Suche**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Es wurde versucht, den Dateizeiger vor dem Anfang der Datei zu verschieben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**Fehler \_ Suche \_ auf \_ Gerät**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



Der Dateizeiger kann für das angegebene Gerät oder die angegebene Datei nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**Fehler \_ ist \_ \_ joinziel**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Ein Join-Befehl oder ein SUBST-Befehl kann nicht für ein Laufwerk verwendet werden, das zuvor verknüpfte Laufwerke enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**Fehler \_ ist \_ verknüpft**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Es wurde versucht, einen Join-oder SUBST-Befehl auf einem Laufwerk zu verwenden, das bereits verknüpft ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**Fehler \_ ist \_ substed**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Es wurde versucht, einen Join-oder SUBST-Befehl auf einem Laufwerk zu verwenden, das bereits ersetzt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**Fehler \_ nicht \_ verknüpft**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



Das System hat versucht, den Join eines Laufwerks zu löschen, das nicht verknüpft ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**Fehler \_ nicht \_ unterteilt**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



Das System hat versucht, die Ersetzung eines nicht ersetzten Laufwerks zu löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**Fehler \_ Verknüpfung \_ für \_ Join**
</dt> <dd> <dl> <dt>

138 (0x8a)
</dt> <dt>



Das System hat versucht, ein Laufwerk einem Verzeichnis auf einem verknüpften Laufwerk beizutreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**Fehler " \_ subst" \_ in " \_ subst"**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



Das System hat versucht, ein Laufwerk zu einem Verzeichnis auf einem ersetzte Laufwerk zu ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**Fehler \_ \_ bei Join mit \_ subst**
</dt> <dd> <dl> <dt>

140 (0x8c)
</dt> <dt>



Das System hat versucht, ein Laufwerk einem Verzeichnis auf einem Ersatz Laufwerk beizutreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**Fehler- \_ subst \_ zum \_ beitreten**
</dt> <dd> <dl> <dt>

141 (0x8d)
</dt> <dt>



Das System hat versucht, ein Laufwerk zu einem Verzeichnis auf einem verbundenen Laufwerk zu unterteilen.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**Fehler \_ ausgelastet- \_ Laufwerk**
</dt> <dd> <dl> <dt>

142 (0x8e)
</dt> <dt>



Das System kann zurzeit keine Verknüpfung oder teilst ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**Fehler beim \_ gleichen \_ Laufwerk**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



Das System kann ein Laufwerk oder ein Verzeichnis auf dem gleichen Laufwerk nicht einem Verzeichnis hinzufügen oder dieses ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**Fehler \_ Verzeichnis \_ nicht \_ root**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



Das Verzeichnis ist kein Unterverzeichnis des Stamm Verzeichnisses.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**Fehler \_ Verzeichnis \_ nicht \_ leer**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



Das Verzeichnis ist nicht leer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**Fehler \_ ist ein \_ subst- \_ Pfad.**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



Der angegebene Pfad wird in einem Ersatz verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**Fehler \_ ist \_ \_ Joinpfad**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Zum Verarbeiten dieses Befehls sind nicht genügend Ressourcen verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**Fehler \_ Pfad \_ ausgelastet**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



Der angegebene Pfad kann zurzeit nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**Fehler \_ ist \_ subst- \_ Ziel**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Es wurde versucht, ein Laufwerk beizutreten oder zu ersetzen, für das ein Verzeichnis auf dem Laufwerk das Ziel eines vorherigen Ersatz ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**Fehler \_ System-Ablauf \_ Verfolgung**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



In ihrer CONFIG.SYS Datei wurden keine System Ablauf Verfolgungs Informationen angegeben, oder die Ablauf Verfolgung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**Fehler \_ bei ungültiger \_ Ereignis \_ Anzahl**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



Die Anzahl der angegebenen Semaphor-Ereignisse für DosMuxSemWait ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**Fehler \_ zu \_ viele \_ muxkellner**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait wurde nicht ausgeführt. zu viele Semaphoren wurden bereits festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**Fehler bei \_ ungültigem \_ Listen \_ Format**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



Die DosMuxSemWait-Liste ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**Fehler \_ Bezeichnung \_ zu \_ lang**
</dt> <dd> <dl> <dt>

154 (0x9a)
</dt> <dt>



Die von Ihnen eingegebene Volumebezeichnung überschreitet die Bezeichnung für das Zeichenlimit des Ziel Dateisystems.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**Fehler \_ zu \_ viele \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9b)
</dt> <dt>



Ein anderer Thread kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**Fehler \_ Signal \_ abgelehnt**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



Der Empfänger Prozess hat das Signal abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**Fehler \_ verworfen**
</dt> <dd> <dl> <dt>

157 (0x9d)
</dt> <dt>



Das Segment wurde bereits verworfen und kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**Fehler \_ nicht \_ gesperrt**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



Das Segment ist bereits entsperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**Fehler \_ hafte \_ ThreadId \_ addr**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



Die Adresse für die Thread-ID ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**Ungültige Argumente für Fehler \_ \_**
</dt> <dd> <dl> <dt>

160 (0xa0)
</dt> <dt>



Mindestens ein Argument ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**Fehler Ungültiger \_ \_ Pfadname.**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



Der angegebene Pfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**Fehler \_ Signal \_ Ausstehend**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Ein Signal steht bereits aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**Fehler beim maximalen Anzahl von \_ \_ thrds. \_**
</dt> <dd> <dl> <dt>

164 (0xa4)
</dt> <dt>



Im System können keine weiteren Threads erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**Fehler beim \_ Sperren \_**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Ein Bereich einer Datei kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**Fehler \_ ausgelastet**
</dt> <dd> <dl> <dt>

170 (0xaa)
</dt> <dt>



Die angeforderte Ressource wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**Fehler \_ \_ beim unterstützen \_ des \_ Geräts.**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



Die Erkennung der Befehls Unterstützung für das Gerät wird durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**Fehler \_ Abbruch \_ Verletzung**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Eine Sperranforderung war für den angegebenen Abbruchbereich nicht ausstehend.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**Fehler \_ atomarische \_ Sperren \_ \_ werden nicht unterstützt**
</dt> <dd> <dl> <dt>

174 (0xae)
</dt> <dt>



Das Dateisystem unterstützt keine atomaren Änderungen am Sperrentyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**Fehler \_ ungültige \_ Segment \_ Nummer.**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



Das System hat eine nicht korrekte Segment Nummer erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**Fehler \_ ungültige \_ Ordnungszahl**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**Fehler ist \_ bereits \_ vorhanden.**
</dt> <dd> <dl> <dt>

183 (0xb7)
</dt> <dt>



Eine Datei kann nicht erstellt werden, wenn die Datei bereits vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**\_ungültige \_ Flag- \_ Nummer.**
</dt> <dd> <dl> <dt>

186 (0xba)
</dt> <dt>



Das über gegebene Flag ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**Fehler " \_ SEM" \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



Der angegebene Name des System Semaphors wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**Fehler \_ beim \_ Starten von \_ Codel.**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**\_ungültiger \_ Stackl-Fehler.**
</dt> <dd> <dl> <dt>

189 (0xbd)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**\_ungültiger \_ ModuleType.**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**Fehler \_ ungültige \_ exe- \_ Signatur.**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



%1 kann nicht im Win32-Modus ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**Fehler- \_ exe als \_ \_ ungültig markiert**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**Fehler fehlerhaftes \_ \_ exe- \_ Format**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 ist keine gültige Win32-Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Fehler bei \_ iterierten \_ Daten über \_ schreiten \_ 64 KB.**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**Fehler \_ ungültige \_ minzuweisung.**
</dt> <dd> <dl> <dt>

195 (0xc3)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**Fehler \_ beim Dynlink \_ aus \_ ungültigem \_ Ring.**
</dt> <dd> <dl> <dt>

196 (0xc4)
</dt> <dt>



Das Betriebssystem kann dieses Anwendungsprogramm nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**Fehler ' \_ IOPL ' ist \_ nicht \_ aktiviert.**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



Das Betriebssystem ist zurzeit nicht für das Ausführen dieser Anwendung konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**Fehler \_ ungültige \_ SEGDPL.**
</dt> <dd> <dl> <dt>

198 (0xc6)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**Der Fehler " \_ autodataseg" über \_ schreitet \_ 64K.**
</dt> <dd> <dl> <dt>

199 (0xc7)
</dt> <dt>



Das Betriebssystem kann dieses Anwendungsprogramm nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**Fehler \_ RING2SEG \_ muss \_ \_ verschiebbar sein.**
</dt> <dd> <dl> <dt>

200 (0xc8)
</dt> <dt>



Das Codesegment darf nicht größer als oder gleich 64 KB sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**Fehler \_ reloc- \_ Kette \_ xeeds \_ seglim**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**Fehler \_ bei infloop \_ in \_ reloc- \_ Kette**
</dt> <dd> <dl> <dt>

202 (0xca)
</dt> <dt>



Das Betriebssystem kann "%1" nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**Fehler bei " \_ \_ nicht \_ gefunden".**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



Die eingegebene Umgebungs Option konnte vom System nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**Fehler " \_ kein \_ Signal \_ gesendet"**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Kein Prozess in der Befehls Teilstruktur verfügt über einen Signalhandler.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**Fehler Name des \_ \_ ausgenommenen \_ Bereichs**
</dt> <dd> <dl> <dt>

206 (0xce)
</dt> <dt>



Der Dateiname oder die Erweiterung ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**Fehler \_ RING2 \_ Stapel \_ wird \_ verwendet**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



Der Stapel 2 wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**Fehler- \_ Meta- \_ Erweiterung \_ zu \_ lang**
</dt> <dd> <dl> <dt>

208 (0xd0)
</dt> <dt>



Die globalen Dateinamen Zeichen, \* oder?, werden falsch eingegeben, oder es werden zu viele globale Dateinamen Zeichen angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**Fehler \_ ungültige \_ Signal \_ Nummer**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



Das Signal, das gesendet wird, ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**Fehler \_ Thread \_ 1 \_ inaktiv**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Der Signalhandler kann nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**Fehler \_ gesperrt**
</dt> <dd> <dl> <dt>

212 (0xd4)
</dt> <dt>



Das Segment ist gesperrt und kann nicht neu zugeordnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**Fehler \_ zu \_ viele \_ Module**
</dt> <dd> <dl> <dt>

214 (0xd6)
</dt> <dt>



An dieses Programm oder Dynamic-Link-Modul sind zu viele Dynamic-Link-Module angefügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**Fehler Schachtelung \_ \_ nicht \_ zulässig**
</dt> <dd> <dl> <dt>

215 (0xd7)
</dt> <dt>



Aufrufe von LoadModule können nicht geschachtelt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**Fehler beim \_ exe- \_ Computer \_ Typen \_ Konflikt**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Diese Version von %1 ist nicht kompatibel mit der Windows-Version, die Sie ausführen. Überprüfen Sie die Systeminformationen Ihres Computers, und wenden Sie sich an den Hersteller der Software.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**Fehler \_ exe \_ kann \_ die \_ signierte \_ Binärdatei nicht ändern**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



Die Bilddatei "%1" ist signiert und kann nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**Fehler \_ exe \_ kann \_ die \_ starke \_ \_ binäre Binärdatei nicht ändern**
</dt> <dd> <dl> <dt>

218 (0xda)
</dt> <dt>



Die Bilddatei "%1" ist stark signiert und kann nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**Fehler \_ Datei \_ ausgecheckt \_**
</dt> <dd> <dl> <dt>

220 (0xdc)
</dt> <dt>



Diese Datei ist ausgecheckt oder für die Bearbeitung durch einen anderen Benutzer gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**Fehler Auschecken \_ \_ erforderlich**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



Die Datei muss vor dem Speichern der Änderungen ausgecheckt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**fehlerhafter \_ \_ \_ Dateityp**
</dt> <dd> <dl> <dt>

222 (0xde)
</dt> <dt>



Der Dateityp, der gespeichert oder abgerufen wird, wurde blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**Fehler \_ Datei \_ zu \_ groß**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



Die Dateigröße überschreitet das zulässige Limit und kann nicht gespeichert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**Fehler \_ Formular Authentifizierung \_ \_ erforderlich.**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Zugriff verweigert. Vor dem Öffnen von Dateien an diesem Speicherort müssen Sie zuerst die Website zur Liste vertrauenswürdiger Sites hinzufügen, die Website aufrufen und die Option zum automatischen Anmelden auswählen.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**Fehler \_ Virus \_ infiziert**
</dt> <dd> <dl> <dt>

225 (0xe1)
</dt> <dt>



Der Vorgang wurde nicht erfolgreich abgeschlossen, weil die Datei einen Virus oder potenziell unerwünschte Software enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**Fehler \_ Virus \_ gelöscht**
</dt> <dd> <dl> <dt>

226 (0xe2)
</dt> <dt>



Diese Datei enthält einen Virus oder potenziell unerwünschte Software und kann nicht geöffnet werden. Aufgrund der Art dieses Virus oder potenziell unerwünschter Software wurde die Datei von diesem Speicherort entfernt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**Fehler \_ Pipe \_ lokal**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



Die Pipe ist lokal.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**Fehler \_ hafte \_ Pipe**
</dt> <dd> <dl> <dt>

230 (0xe6)
</dt> <dt>



Der Pipe-Zustand ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**Fehler \_ Pipe \_ ausgelastet**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Alle Pipeinstanzen sind ausgelastet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**Fehler \_ \_ Daten**
</dt> <dd> <dl> <dt>

232 (0xe8)
</dt> <dt>



Die Pipe wird geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**Fehler \_ Pipe ist \_ nicht \_ verbunden.**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Kein Prozess ist am anderen Ende der Pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**Fehler \_ Weitere \_ Daten**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



Weitere Daten sind verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**Fehler- \_ VC- \_ getrennt**
</dt> <dd> <dl> <dt>

240 (0xF)
</dt> <dt>



Die Sitzung wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**\_ungültiger \_ EA- \_ Name.**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



Der angegebene erweiterte Attribut Name war ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**Fehler- \_ EA- \_ Liste \_ inkonsistent**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Die erweiterten Attribute sind inkonsistent.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**Timeout für Wartezeit \_**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Timeout bei Wartevorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**Fehler \_ keine \_ weiteren \_ Elemente**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Es sind keine weiteren Daten verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**Fehler \_ beim \_ Kopieren**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



Die Kopierfunktionen können nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**Fehler \_ Verzeichnis**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



Der Verzeichnisname ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**Fehler ( \_ EAS) \_ \_**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Die erweiterten Attribute passten nicht in den Puffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**Fehler- \_ EA- \_ Datei \_ beschädigt**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



Die erweiterte Attribut Datei im bereitgestellten Dateisystem ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**Fehler- \_ EA- \_ Tabelle \_ voll**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



Die Tabellen Datei für das erweiterte Attribut ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**Fehler \_ ungültiges \_ EA- \_ handle.**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



Das angegebene erweiterte Attribut Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**Fehler \_ EAS \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



Das bereitgestellte Dateisystem unterstützt keine erweiterten Attribute.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**Fehler \_ nicht \_ Besitzer**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Es wurde versucht, Mutex freizugeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**Fehler \_ zu \_ viele \_ Beiträge**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Es wurden zu viele Beiträge an einem Semaphor vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**Fehler \_ Teil \_ Kopie**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Nur ein Teil einer "Read processmemory"-oder "Write-processmemory"-Anforderung wurde abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**Fehler " \_ Oplock" \_ nicht \_ erteilt**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



Die Oplock-Anforderung wurde verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**Fehler \_ beim \_ Oplock- \_ Protokoll.**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Vom System wurde eine ungültige Oplock-Bestätigung empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**Fehler \_ Festplatte \_ zu \_ fragmentiert**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



Das Volume ist zu fragmentiert, um diesen Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**Fehler beim \_ Löschen \_ Ausstehend**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



Die Datei kann nicht geöffnet werden, da Sie gerade gelöscht wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**Fehler nicht \_ kompatibel \_ mit der \_ \_ \_ \_ Registrierungs \_ Einstellung "globaler Kurzname"**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



Auf diesem Volume können aufgrund der globalen Registrierungs Einstellung keine Kurznamen Einstellungen geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**Fehler \_ \_ Kurznamen \_ sind \_ \_ auf dem \_ Volume nicht aktiviert.**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Kurznamen sind auf diesem Volume nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**Fehler \_ Sicherheitsdaten \_ Strom \_ ist \_ inkonsistent**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



Der Sicherheitsstream für das angegebene Volume befindet sich in einem inkonsistenten Zustand. Führen Sie CHKDSK auf dem Volume aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**\_ungültiger \_ Sperr \_ Bereich.**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Ein angeforderter Vorgang zum Sperren von Dateien kann aufgrund eines ungültigen Byte Bereichs nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**Fehler \_ Bild- \_ Subsystem \_ nicht \_ vorhanden**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



Das für die Unterstützung des Image Typs erforderliche Subsystem ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**Fehler \_ Benachrichtigungs- \_ GUID \_ bereits \_ definiert**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



Der angegebenen Datei ist bereits eine Benachrichtigungs-GUID zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**Fehler bei \_ ungültigem \_ Ausnahme \_ Handler.**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Es wurde eine ungültige ausnahmehandlerroutine erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**Fehler \_ doppelte \_ Berechtigungen**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Doppelte Berechtigungen wurden für das Token angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**Fehler " \_ keine \_ Bereiche \_ verarbeitet"**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Es konnten keine Bereiche für den angegebenen Vorgang verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**\_der Fehler \_ ist \_ in der \_ System \_ Datei nicht zulässig.**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



Der Vorgang ist für eine interne Dateisystem Datei nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**Fehler Datenträger \_ \_ Ressourcen \_ aufgebraucht**
</dt> <dd> <dl> <dt>

314 (0x13a)
</dt> <dt>



Die physischen Ressourcen dieses Datenträgers sind erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**\_ungültiges \_ Token.**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



Das Token, das die Daten darstellt, ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**Fehler \_ Geräte \_ Funktion \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



Das Gerät unterstützt die Befehls Funktion nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**Fehler "Mid" wurde \_ \_ \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



Der Nachrichtentext für die Meldungs Nummer 0x %1 kann nicht in der Nachrichtendatei für %2 gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**Fehler \_ Bereich wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



Der angegebene Bereich wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**Fehler beim \_ undefinierten \_ Bereich**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



Die angegebene zentrale Zugriffs Richtlinie ist auf dem Zielcomputer nicht definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**\_ungültige \_ Obergrenze**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



Die von Active Directory erhaltene zentrale Zugriffs Richtlinie ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**Fehler \_ Gerät \_ nicht erreichbar**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



Das Gerät ist nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**Fehler \_ Gerät " \_ keine \_ Ressourcen"**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



Das Zielgerät verfügt nicht über genügend Ressourcen, um den Vorgang abzuschließen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**\_ \_ Prüfsummen \_ Fehler bei Fehler Daten.**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Ein Prüfsummen Fehler bei der Datenintegrität ist aufgetreten. Die Daten im Dateistream sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**Fehler \_ intergemischter \_ Kernel- \_ EA- \_ Vorgang**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Es wurde versucht, einen Kernel und ein normales Erweitertes Attribut (EA) im selben Vorgang zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**Trim-Fehler \_ Datei \_ Ebene \_ \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



Das Gerät unterstützt keine Trim auf Dateiebene.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**Fehler \_ Offset- \_ Ausrichtungs \_ Verletzung**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



Der Befehl hat einen Daten Offset angegeben, der nicht an der Granularität/Ausrichtung des Geräts ausgerichtet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**\_ungültiges \_ Feld \_ in \_ Parameter \_ Liste.**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



Der Befehl hat ein ungültiges Feld in der Parameterliste angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**Fehler Vorgang wird ausgeführt. \_ \_ \_**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



Zurzeit wird ein Vorgang mit dem Gerät ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**fehlerhafter \_ \_ Geräte \_ Pfad**
</dt> <dd> <dl> <dt>

330 (0x14a)
</dt> <dt>



Es wurde versucht, den Befehl über einen ungültigen Pfad zum Zielgerät zu senden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**Fehler \_ zu \_ viele \_ Deskriptoren.**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



Der Befehl hat eine Reihe von Deskriptoren angegeben, die das vom Gerät unterstützte Maximum überschreiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**Fehler beim Bereinigen der \_ \_ Daten. \_**
</dt> <dd> <dl> <dt>

332 (0x14c)
</dt> <dt>



Das Bereinigen ist für die angegebene Datei deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**Fehler \_ nicht \_ redundanter \_ Speicher**
</dt> <dd> <dl> <dt>

333 (0x14d)
</dt> <dt>



Das Speichergerät bietet keine Redundanz.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**Fehler bei \_ Residenter \_ Datei \_ nicht \_ unterstützt**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Ein Vorgang wird für eine residente Datei nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**Fehler \_ komprimierte \_ Datei \_ nicht \_ unterstützt.**
</dt> <dd> <dl> <dt>

335 (0x14f)
</dt> <dt>



Ein Vorgang wird für eine komprimierte Datei nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**Fehler \_ Verzeichnis \_ \_ wird nicht unterstützt.**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Ein Vorgang wird in einem Verzeichnis nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**Fehler \_ \_ beim Lesen \_ aus der \_ Kopie.**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Die angegebene Kopie der angeforderten Daten konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**Fehler \_ beim \_ NoAction- \_ Neustart**
</dt> <dd> <dl> <dt>

350 (0x15e)
</dt> <dt>



Es wurde keine Aktion durchgeführt, da ein Systemneustart erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**Fehler beim Herunterfahren. \_ \_**
</dt> <dd> <dl> <dt>

351 (0x15f)
</dt> <dt>



Fehler beim Herunterfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**Fehler \_ beim \_ Neustart.**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Der Neustart Vorgang ist fehlgeschlagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**maximale Anzahl von Sitzungen des Fehlers \_ \_ \_ erreicht**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



Die maximale Anzahl von Sitzungen wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**Fehler \_ Thread \_ Modus \_ bereits im \_ Hintergrund**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



Der Thread befindet sich bereits im Hintergrund Verarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**Fehler im \_ Thread \_ Modus nicht im \_ \_ Hintergrund.**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



Der Thread befindet sich nicht im Hintergrund Verarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**Fehler \_ Prozess \_ Modus \_ bereits \_ Hintergrund**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



Der Prozess befindet sich bereits im Hintergrund Verarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**Fehler \_ Prozess \_ Modus \_ nicht im \_ Hintergrund**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



Der Prozess befindet sich nicht im Hintergrund Verarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**\_ungültige \_ Adresse.**
</dt> <dd> <dl> <dt>

487 (0x1e7)
</dt> <dt>



Versuchen Sie, auf eine ungültige Adresse zuzugreifen.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winerror. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Fehler Codes](system-error-codes.md)
</dt> </dl>

 

 




