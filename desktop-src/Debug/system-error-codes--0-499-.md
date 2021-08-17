---
description: Beschreibt die Fehlercodes 0-499, die in der Headerdatei "WinError.h" definiert sind und für Entwickler bestimmt sind.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Systemfehlercodes (0-499) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: a9eddec2baf098f62bb1c0ad88e632360807e7f3fd0ea045f2565587f13e93a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405649"
---
# <a name="system-error-codes-0-499"></a>Systemfehlercodes (0-499)

> [!NOTE]
> Diese Informationen sind für Entwickler bestimmt, die Systemfehler debuggen. Für andere Fehler, z. B. Probleme mit Windows Update, finden Sie auf der Seite [Fehlercodes](system-error-codes.md) eine Liste mit Ressourcen.

In der folgenden Liste werden [Systemfehlercodes](system-error-codes.md) (Fehler 0 bis 499) beschrieben. Sie werden von der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) zurückgegeben, wenn viele Funktionen fehlschlagen. Um den Beschreibungstext für den Fehler in Ihrer Anwendung abzurufen, verwenden Sie die [**FormatMessage-Funktion**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) mit dem **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM-Flag.**

<dl> <dt>

<span id="ERROR_SUCCESS"></span><span id="error_success"></span>**FEHLER \_ ERFOLGREICH**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Der Vorgang wurde erfolgreich abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**FEHLER: \_ UNGÜLTIGE \_ FUNKTION**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Falsche Funktion.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Die angegebene Datei wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**FEHLERPFAD \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

3 (0x3)
</dt> <dt>



Das System kann den angegebenen Pfad nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**FEHLER \_ ZU \_ VIELE \_ \_ GEÖFFNETE DATEIEN**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Das System kann die Datei nicht öffnen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**FEHLERZUGRIFF \_ \_ VERWEIGERT**
</dt> <dd> <dl> <dt>

5 (0x5)
</dt> <dt>



Zugriff verweigert.“


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ HANDLE**
</dt> <dd> <dl> <dt>

6 (0x6)
</dt> <dt>



Das Handle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**FEHLER \_ IM \_ PAPIERKORB**
</dt> <dd> <dl> <dt>

7 (0x7)
</dt> <dt>



Die Speicherkontrollblöcke wurden zerstört.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Für die Verarbeitung dieses Befehls sind nicht genügend Speicherressourcen verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**FEHLER: \_ UNGÜLTIGER \_ BLOCK**
</dt> <dd> <dl> <dt>

9 (0x9)
</dt> <dt>



Die Speichersteuerungsblockadresse ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**FEHLER: \_ FEHLERHAFTE \_ UMGEBUNG**
</dt> <dd> <dl> <dt>

10 (0xA)
</dt> <dt>



Die Umgebung ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**FEHLER: \_ \_ UNGÜLTIGES FORMAT**
</dt> <dd> <dl> <dt>

11 (0xB)
</dt> <dt>



Es wurde versucht, ein Programm mit einem falschen Format zu laden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**FEHLER: \_ UNGÜLTIGER \_ ZUGRIFF**
</dt> <dd> <dl> <dt>

12 (0xC)
</dt> <dt>



Der Zugriffscode ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**FEHLER \_ UNGÜLTIGE \_ DATEN**
</dt> <dd> <dl> <dt>

13 (0xD)
</dt> <dt>



Die Daten sind ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**FEHLER \_ OUTOFMEMORY**
</dt> <dd> <dl> <dt>

14 (0xE)
</dt> <dt>



Für diesen Vorgang ist nicht genügend Speicher verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**FEHLER \_ UNGÜLTIGES \_ LAUFWERK**
</dt> <dd> <dl> <dt>

15 (0xF)
</dt> <dt>



Das angegebene Laufwerk kann vom System nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**FEHLER \_ CURRENT \_ DIRECTORY**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Das Verzeichnis kann nicht entfernt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**FEHLER \_ NICHT \_ \_ IDENTISCHES GERÄT**
</dt> <dd> <dl> <dt>

17 (0x11)
</dt> <dt>



Das System kann die Datei nicht auf ein anderes Laufwerk verschieben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**FEHLER: \_ KEINE \_ WEITEREN \_ DATEIEN**
</dt> <dd> <dl> <dt>

18 (0x12)
</dt> <dt>



Es sind keine Dateien mehr vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**FEHLER \_ BEIM SCHREIBEN VON \_ "PROTECT"**
</dt> <dd> <dl> <dt>

19 (0x13)
</dt> <dt>



Das Medium ist schreibgeschützter.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR \_ BAD \_ UNIT**
</dt> <dd> <dl> <dt>

20 (0x14)
</dt> <dt>



Das system kann das angegebene Gerät nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**FEHLER \_ NICHT \_ BEREIT**
</dt> <dd> <dl> <dt>

21 (0x15)
</dt> <dt>



Das Gerät ist nicht bereit.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**FEHLER: \_ \_ FEHLERHAFTER BEFEHL**
</dt> <dd> <dl> <dt>

22 (0x16)
</dt> <dt>



Das Gerät erkennt den Befehl nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRC"></span><span id="error_crc"></span>**\_FEHLER-CRC**
</dt> <dd> <dl> <dt>

23 (0x17)
</dt> <dt>



Datenfehler (Überprüfung der zyklischen Redundanz)


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**FEHLER \_ \_ UNGÜLTIGE LÄNGE**
</dt> <dd> <dl> <dt>

24 (0x18)
</dt> <dt>



Das Programm hat einen Befehl ausgegeben, aber die Befehlslänge ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR \_ SEEK**
</dt> <dd> <dl> <dt>

25 (0x19)
</dt> <dt>



Das Laufwerk kann keinen bestimmten Bereich oder eine bestimmte Spur auf dem Datenträger finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR \_ NOT \_ DOS \_ DISK**
</dt> <dd> <dl> <dt>

26 (0x1A)
</dt> <dt>



Auf den angegebenen Datenträger oder die angegebene Diskette kann nicht zugegriffen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**FEHLERBRANCHE \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

27 (0x1B)
</dt> <dt>



Das Laufwerk kann den angeforderten Sektor nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**FEHLER \_ AUS \_ \_ PAPIER**
</dt> <dd> <dl> <dt>

28 (0x1C)
</dt> <dt>



Der Drucker ist nicht aus Papier.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**FEHLER \_ BEIM SCHREIBEN \_**
</dt> <dd> <dl> <dt>

29 (0x1D)
</dt> <dt>



Das System kann nicht auf das angegebene Gerät schreiben.


</dt> </dl> </dd> <dt>

<span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**FEHLER \_ BEIM LESEN DES \_ FEHLERS**
</dt> <dd> <dl> <dt>

30 (0x1E)
</dt> <dt>



Das System kann nicht vom angegebenen Gerät lesen.


</dt> </dl> </dd> <dt>

<span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**FEHLER \_ \_ GEN-FEHLER**
</dt> <dd> <dl> <dt>

31 (0x1F)
</dt> <dt>



Ein an das System angeschlossenes Gerät funktioniert nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_ \_ FEHLERFREIGABEVERLETZUNG**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Der Prozess kann nicht auf die Datei zugreifen, da sie bereits von einem anderen Prozess verwendet wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_ \_ FEHLERSPERRVERLETZUNG**
</dt> <dd> <dl> <dt>

33 (0x21)
</dt> <dt>



Der Prozess kann nicht auf die Datei zugreifen, da sie teilweise von einem anderen Prozess gesperrt ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**FEHLER: \_ FALSCHER \_ DATENTRÄGER**
</dt> <dd> <dl> <dt>

34 (0x22)
</dt> <dt>



Die falsche Diskette befindet sich auf dem Laufwerk. Fügen Sie %2 (Seriennummer des Volumes: %3) in Laufwerk %1 ein.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**\_ \_ FEHLERFREIGABEPUFFER \_ ÜBERSCHRITTEN**
</dt> <dd> <dl> <dt>

36 (0x24)
</dt> <dt>



Zu viele Dateien für die Freigabe geöffnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR \_ HANDLE \_ EOF**
</dt> <dd> <dl> <dt>

38 (0x26)
</dt> <dt>



Das Ende der Datei wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**\_FEHLERHANDLE \_ DATENTRÄGER \_ VOLL**
</dt> <dd> <dl> <dt>

39 (0x27)
</dt> <dt>



Der Datenträger ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**FEHLER \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

50 (0x32)
</dt> <dt>



Die Anforderung wird nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR \_ REM \_ NOT \_ LIST**
</dt> <dd> <dl> <dt>

51 (0x33)
</dt> <dt>



Windows den Netzwerkpfad nicht finden. Vergewissern Sie sich, dass der Netzwerkpfad richtig ist und der Zielcomputer nicht ausgelastet oder ausgeschaltet ist. Wenn Windows den Netzwerkpfad immer noch nicht finden können, wenden Sie sich an Ihren Netzwerkadministrator.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**\_FEHLER: \_ DUP-NAME**
</dt> <dd> <dl> <dt>

52 (0x34)
</dt> <dt>



Sie waren nicht verbunden, da im Netzwerk ein doppelter Name vorhanden ist. Wenn Sie einer Domäne beitreten, wechseln Sie zu System in Systemsteuerung , um den Computernamen zu ändern, und versuchen Sie es erneut. Wenn Sie einer Arbeitsgruppe beitreten, wählen Sie einen anderen Arbeitsgruppennamen aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**FEHLER \_ BAD \_ NETPATH**
</dt> <dd> <dl> <dt>

53 (0x35)
</dt> <dt>



Der Netzwerkpfad wurde nicht gefunden.“


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**FEHLER \_ NETZWERK \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

54 (0x36)
</dt> <dt>



Das Netzwerk ist ausgelastet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**FEHLER \_ BEI \_ NICHT \_ VORHANDENER ENTWICKLUNG**
</dt> <dd> <dl> <dt>

55 (0x37)
</dt> <dt>



Die angegebene Netzwerkressource oder das angegebene Gerät ist nicht mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**FEHLER \_ ZU \_ VIELE \_ CMDS**
</dt> <dd> <dl> <dt>

56 (0x38)
</dt> <dt>



Das Netzwerk-BIOS-Befehlslimit wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**FEHLER \_ ADAP \_ HDW \_ ERR**
</dt> <dd> <dl> <dt>

57 (0x39)
</dt> <dt>



Hardwarefehler beim Netzwerkadapter.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ NET-RESP**
</dt> <dd> <dl> <dt>

58 (0x3A)
</dt> <dt>



Der angegebene Server kann den angeforderten Vorgang nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**FEHLER \_ UNEXP \_ NET \_ ERR**
</dt> <dd> <dl> <dt>

59 (0x3B)
</dt> <dt>



Unerwarteter Netzwerkfehler.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**FEHLER: \_ BAD \_ REM \_ ADAP**
</dt> <dd> <dl> <dt>

60 (0x3C)
</dt> <dt>



Der Remoteadapter ist nicht kompatibel.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**FEHLER \_ PRINTQ \_ FULL**
</dt> <dd> <dl> <dt>

61 (0x3D)
</dt> <dt>



Die Druckerwarteschlange ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**FEHLER: \_ KEIN \_ \_ SPOOLSPEICHERPLATZ**
</dt> <dd> <dl> <dt>

62 (0x3E)
</dt> <dt>



Speicherplatz zum Speichern der Datei, die auf das Drucken wartet, ist auf dem Server nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**FEHLER \_ BEIM DRUCKEN \_ ABGEBROCHEN**
</dt> <dd> <dl> <dt>

63 (0x3F)
</dt> <dt>



Ihre Datei, die auf das Drucken wartet, wurde gelöscht.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**FEHLER \_ NETNAME \_ GELÖSCHT**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Der angegebene Netzwerkname ist nicht mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**FEHLER \_ \_ NETZWERKZUGRIFF \_ VERWEIGERT**
</dt> <dd> <dl> <dt>

65 (0x41)
</dt> <dt>



Der Netzwerkzugriff wird verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ ENTWICKLUNGSTYP**
</dt> <dd> <dl> <dt>

66 (0x42)
</dt> <dt>



Der Netzwerkressourcentyp ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ NET-NAME**
</dt> <dd> <dl> <dt>

67 (0x43)
</dt> <dt>



„Der Netzwerkname wurde nicht gefunden.“


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**FEHLER \_ ZU \_ VIELE \_ NAMEN**
</dt> <dd> <dl> <dt>

68 (0x44)
</dt> <dt>



Das Namenslimit für die Netzwerkadapterkarte des lokalen Computers wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**FEHLER \_ ZU \_ VIELE \_ SESS**
</dt> <dd> <dl> <dt>

69 (0x45)
</dt> <dt>



Das Netzwerk-BIOS-Sitzungslimit wurde überschritten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**FEHLERFREIGABE \_ \_ ANGEHALTEN**
</dt> <dd> <dl> <dt>

70 (0x46)
</dt> <dt>



Der Remoteserver wurde angehalten oder wird gerade gestartet.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**FEHLER \_ REQ \_ NOT \_ ACCEP**
</dt> <dd> <dl> <dt>

71 (0x47)
</dt> <dt>



Zu diesem Zeitpunkt können keine weiteren Verbindungen mit diesem Remotecomputer hergestellt werden, da bereits so viele Verbindungen vorhanden sind, wie der Computer akzeptieren kann.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**FEHLER \_ REDIR \_ ANGEHALTEN**
</dt> <dd> <dl> <dt>

72 (0x48)
</dt> <dt>



Das angegebene Drucker- oder Datenträgergerät wurde angehalten.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**FEHLERDATEI \_ \_ VORHANDEN**
</dt> <dd> <dl> <dt>

80 (0x50)
</dt> <dt>



Die Datei ist vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**FEHLER \_ KANN NICHT AUSGELÖST \_ WERDEN**
</dt> <dd> <dl> <dt>

82 (0x52)
</dt> <dt>



Das Verzeichnis oder die Datei kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**FEHLERFEHLER \_ \_ I24**
</dt> <dd> <dl> <dt>

83 (0x53)
</dt> <dt>



Fehler bei INT 24.


</dt> </dl> </dd> <dt>

<span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**FEHLER \_ BEI OUT OF \_ \_ STRUCTURES**
</dt> <dd> <dl> <dt>

84 (0x54)
</dt> <dt>



Storage, um diese Anforderung zu verarbeiten, ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**FEHLER \_ BEREITS \_ ZUGEWIESEN**
</dt> <dd> <dl> <dt>

85 (0x55)
</dt> <dt>



Der Name des lokalen Geräts wird bereits verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**FEHLER: \_ UNGÜLTIGES \_ KENNWORT**
</dt> <dd> <dl> <dt>

86 (0x56)
</dt> <dt>



Das angegebene Netzwerkkennwort ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**
</dt> <dd> <dl> <dt>

87 (0x57)
</dt> <dt>



„Der Parameter ist falsch.“


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**FEHLER \_ NET \_ WRITE \_ FAULT**
</dt> <dd> <dl> <dt>

88 (0x58)
</dt> <dt>



Im Netzwerk ist ein Schreibfehler aufgetreten.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**FEHLER: \_ \_ KEINE PROC-SLOTS \_**
</dt> <dd> <dl> <dt>

89 (0x59)
</dt> <dt>



Das System kann derzeit keinen anderen Prozess starten.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**FEHLER: \_ \_ ZU VIELE \_ SEMAPHOREN**
</dt> <dd> <dl> <dt>

100 (0x64)
</dt> <dt>



Ein weiteres Systemsemaphor kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**FEHLER \_ EXCL \_ SEM ALREADY \_ \_ OWNED**
</dt> <dd> <dl> <dt>

101 (0x65)
</dt> <dt>



Das exklusive Semaphor befindet sich im Besitz eines anderen Prozesses.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**FEHLER \_ SEM \_ IST \_ FESTGELEGT**
</dt> <dd> <dl> <dt>

102 (0x66)
</dt> <dt>



Das Semaphor ist festgelegt und kann nicht geschlossen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**FEHLER: \_ \_ ZU VIELE \_ \_ SEM-ANFORDERUNGEN**
</dt> <dd> <dl> <dt>

103 (0x67)
</dt> <dt>



Das Semaphor kann nicht erneut festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**FEHLER \_ ZUR \_ \_ INTERRUPTZEIT \_ UNGÜLTIG**
</dt> <dd> <dl> <dt>

104 (0x68)
</dt> <dt>



Exklusive Semaphore können nicht zur Interruptzeit anfordern.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**FEHLER \_ SEM \_ OWNER \_ DIED**
</dt> <dd> <dl> <dt>

105 (0x69)
</dt> <dt>



Der vorherige Besitz dieses Semaphors ist beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**FEHLER: \_ \_ SEM-BENUTZERLIMIT \_**
</dt> <dd> <dl> <dt>

106 (0x6A)
</dt> <dt>



Fügen Sie die Diskette für Laufwerk %1 ein.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**FEHLER \_ BEIM ÄNDERN DES \_ DATENTRÄGERS**
</dt> <dd> <dl> <dt>

107 (0x6B)
</dt> <dt>



Das Programm wurde beendet, weil keine alternative Diskette eingefügt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**FEHLERLAUFWERK \_ \_ GESPERRT**
</dt> <dd> <dl> <dt>

108 (0x6C)
</dt> <dt>



Der Datenträger wird von einem anderen Prozess verwendet oder gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**FEHLER BEI \_ \_ PIPEFEHLER**
</dt> <dd> <dl> <dt>

109 (0x6D)
</dt> <dt>



Die Pipe wurde beendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**FEHLER \_ BEIM ÖFFNEN \_**
</dt> <dd> <dl> <dt>

110 (0x6E)
</dt> <dt>



Das angegebene Gerät oder die angegebene Datei kann vom System nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_ \_ FEHLERPUFFERÜBERLAUF**
</dt> <dd> <dl> <dt>

111 (0x6F)
</dt> <dt>



Der Dateiname ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**FEHLER \_ DATENTRÄGER \_ VOLL**
</dt> <dd> <dl> <dt>

112 (0x70)
</dt> <dt>



There is not enough space on the disk.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**FEHLER: \_ \_ KEINE \_ \_ SUCHHANDLES MEHR**
</dt> <dd> <dl> <dt>

113 (0x71)
</dt> <dt>



Es sind keine internen Dateibezeichner mehr verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**FEHLER \_ UNGÜLTIGES \_ \_ ZIELHAND HANDLE**
</dt> <dd> <dl> <dt>

114 (0x72)
</dt> <dt>



Der interne Zieldateibezeichner ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**FEHLER \_ UNGÜLTIGE \_ KATEGORIE**
</dt> <dd> <dl> <dt>

117 (0x75)
</dt> <dt>



Der vom Anwendungsprogramm vorgenommene IOCTL-Aufruf ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ VERIFY-SCHALTER**
</dt> <dd> <dl> <dt>

118 (0x76)
</dt> <dt>



Der Switchparameterwert verify-on-write ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**FEHLER: \_ \_ FEHLERHAFTE \_ TREIBEREBENE**
</dt> <dd> <dl> <dt>

119 (0x77)
</dt> <dt>



Das System unterstützt den angeforderten Befehl nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**FEHLERAUFRUF \_ \_ NICHT \_ IMPLEMENTIERT**
</dt> <dd> <dl> <dt>

120 (0x78)
</dt> <dt>



Diese Funktion wird auf diesem System nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**FEHLER \_ \_ SEM-TIMEOUT**
</dt> <dd> <dl> <dt>

121 (0x79)
</dt> <dt>



Der Timeoutzeitraum für das Semaphor ist abgelaufen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**FEHLER: \_ NICHT GENÜGEND \_ PUFFER**
</dt> <dd> <dl> <dt>

122 (0x7A)
</dt> <dt>



Der an einen Systemaufruf übergebene Datenbereich ist zu klein.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**FEHLER \_ UNGÜLTIGER \_ NAME**
</dt> <dd> <dl> <dt>

123 (0x7B)
</dt> <dt>



Die Syntax für Dateiname, Verzeichnisname oder Volumebezeichnung ist falsch.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**FEHLER \_ \_ UNGÜLTIGER WERT**
</dt> <dd> <dl> <dt>

124 (0x7C)
</dt> <dt>



Die Systemaufrufebene ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**FEHLER: \_ \_ KEINE \_ VOLUMEBEZEICHNUNG**
</dt> <dd> <dl> <dt>

125 (0x7D)
</dt> <dt>



Der Datenträger verfügt über keine Volumebezeichnung.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**FEHLER \_ MOD \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

126 (0x7E)
</dt> <dt>



Das angegebene Modul wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**\_FEHLERPROC \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

127 (0x7F)
</dt> <dt>



Die angegebene Prozedur konnte nicht gefunden werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR \_ WAIT \_ NO \_ CHILDREN**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Es gibt keine untergeordneten Prozesse, auf die gewartet werden muss.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**FEHLER \_ \_ UNTERGEORDNETER NICHT \_ ABGESCHLOSSEN**
</dt> <dd> <dl> <dt>

129 (0x81)
</dt> <dt>



Die %1-Anwendung kann nicht im Win32-Modus ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**FEHLER BEIM \_ HANDLE FÜR DEN DIREKTEN \_ ZUGRIFF \_**
</dt> <dd> <dl> <dt>

130 (0x82)
</dt> <dt>



Versuchen Sie, ein Dateihandle für eine geöffnete Datenträgerpartition für einen anderen Vorgang als unformatierte Datenträger-E/A zu verwenden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR \_ NEGATIVE \_ SEEK**
</dt> <dd> <dl> <dt>

131 (0x83)
</dt> <dt>



Es wurde versucht, den Dateizeiger vor dem Anfang der Datei zu verschieben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**FEHLERSUCHE \_ \_ AUF \_ GERÄT**
</dt> <dd> <dl> <dt>

132 (0x84)
</dt> <dt>



Der Dateizeiger kann nicht auf dem angegebenen Gerät oder der angegebenen Datei festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**\_FEHLER: \_ \_ JOINZIEL**
</dt> <dd> <dl> <dt>

133 (0x85)
</dt> <dt>



Ein JOIN- oder SUBST-Befehl kann nicht für ein Laufwerk verwendet werden, das zuvor verknüpfte Laufwerke enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**FEHLER \_ IST \_ VERKNÜPFT**
</dt> <dd> <dl> <dt>

134 (0x86)
</dt> <dt>



Es wurde versucht, einen JOIN- oder SUBST-Befehl auf einem Laufwerk zu verwenden, das bereits verknüpft wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR \_ IS \_ SUBSTED**
</dt> <dd> <dl> <dt>

135 (0x87)
</dt> <dt>



Es wurde versucht, einen JOIN- oder SUBST-Befehl auf einem Laufwerk zu verwenden, das bereits ersetzt wurde.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**FEHLER \_ NICHT \_ VERKNÜPFT**
</dt> <dd> <dl> <dt>

136 (0x88)
</dt> <dt>



Das System hat versucht, den JOIN eines nicht verknüpften Laufwerks zu löschen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR \_ NOT \_ SUBSTED**
</dt> <dd> <dl> <dt>

137 (0x89)
</dt> <dt>



Das System hat versucht, die Ersetzung eines Laufwerks zu löschen, das nicht ersetzt wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR \_ JOIN \_ TO \_ JOIN**
</dt> <dd> <dl> <dt>

138 (0x8A)
</dt> <dt>



Das System hat versucht, ein Laufwerk mit einem Verzeichnis auf einem verknüpften Laufwerk zu verbinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR \_ SUBST \_ TO \_ SUBST**
</dt> <dd> <dl> <dt>

139 (0x8B)
</dt> <dt>



Das System hat versucht, ein Laufwerk durch ein Verzeichnis auf einem ersetzten Laufwerk zu ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR \_ JOIN \_ TO \_ SUBST**
</dt> <dd> <dl> <dt>

140 (0x8C)
</dt> <dt>



Das System hat versucht, ein Laufwerk mit einem Verzeichnis auf einem ersetzten Laufwerk zu verbinden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR \_ SUBST \_ TO \_ JOIN**
</dt> <dd> <dl> <dt>

141 (0x8D)
</dt> <dt>



Das System hat versucht, ein Laufwerk einem Verzeichnis auf einem verknüpften Laufwerk zu unterteilen.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**FEHLER \_ BEIM \_ AUSGELASTETEN LAUFWERK**
</dt> <dd> <dl> <dt>

142 (0x8E)
</dt> <dt>



Das System kann derzeit keine JOIN- oder SUBST-Vorgänge ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**FEHLER \_ BEIM GLEICHEN \_ LAUFWERK**
</dt> <dd> <dl> <dt>

143 (0x8F)
</dt> <dt>



Das System kann ein Laufwerk nicht mit einem Verzeichnis auf demselben Laufwerk verbinden oder ersetzen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**FEHLER \_ DIR \_ NOT \_ ROOT**
</dt> <dd> <dl> <dt>

144 (0x90)
</dt> <dt>



Das Verzeichnis ist kein Unterverzeichnis des Stammverzeichnisses.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**FEHLERVERZEICHNIS \_ \_ NICHT \_ LEER**
</dt> <dd> <dl> <dt>

145 (0x91)
</dt> <dt>



Das Verzeichnis ist nicht leer.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**FEHLER: \_ \_ \_ SUBST-PFAD**
</dt> <dd> <dl> <dt>

146 (0x92)
</dt> <dt>



Der angegebene Pfad wird in einem Ersatz verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**\_FEHLER: \_ \_ JOINPFAD**
</dt> <dd> <dl> <dt>

147 (0x93)
</dt> <dt>



Für die Verarbeitung dieses Befehls sind nicht genügend Ressourcen verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**FEHLERPFAD \_ \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

148 (0x94)
</dt> <dt>



Der angegebene Pfad kann derzeit nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**FEHLER: \_ \_ \_ SUBST-ZIEL**
</dt> <dd> <dl> <dt>

149 (0x95)
</dt> <dt>



Es wurde versucht, ein Laufwerk zu verbinden oder zu ersetzen, für das ein Verzeichnis auf dem Laufwerk das Ziel eines vorherigen Ersatzlaufwerks ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_ \_ FEHLERSYSTEMABLAUFVERFOLGUNG**
</dt> <dd> <dl> <dt>

150 (0x96)
</dt> <dt>



Systemablaufverfolgungsinformationen wurden in Ihrer CONFIG.SYS-Datei nicht angegeben, oder die Ablaufverfolgung ist nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**FEHLER: \_ \_ UNGÜLTIGE \_ EREIGNISANZAHL**
</dt> <dd> <dl> <dt>

151 (0x97)
</dt> <dt>



Die Anzahl der angegebenen Semaphorereignisse für DosMuxSemWait ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**FEHLER \_ ZU \_ VIELE \_ MUXWAITERS**
</dt> <dd> <dl> <dt>

152 (0x98)
</dt> <dt>



DosMuxSemWait wurde nicht ausgeführt. Zu viele Semaphoren sind bereits festgelegt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ LISTENFORMAT**
</dt> <dd> <dl> <dt>

153 (0x99)
</dt> <dt>



Die DosMuxSemWait-Liste ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**FEHLERBEZEICHNUNG \_ \_ ZU \_ LANG**
</dt> <dd> <dl> <dt>

154 (0x9A)
</dt> <dt>



Die eingegebene Volumebezeichnung überschreitet den Grenzwert für Bezeichnungszeichen des Zieldateisystems.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**FEHLER \_ ZU \_ VIELE \_ TCBS**
</dt> <dd> <dl> <dt>

155 (0x9B)
</dt> <dt>



Ein anderer Thread kann nicht erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**FEHLERSIGNAL \_ \_ ABGELEHNT**
</dt> <dd> <dl> <dt>

156 (0x9C)
</dt> <dt>



Der Empfängerprozess hat das Signal abgelehnt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**FEHLER \_ VERWORFEN**
</dt> <dd> <dl> <dt>

157 (0x9D)
</dt> <dt>



Das Segment wird bereits verworfen und kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**FEHLER \_ NICHT \_ GESPERRT**
</dt> <dd> <dl> <dt>

158 (0x9E)
</dt> <dt>



Das Segment ist bereits entsperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ THREADID-ADDR**
</dt> <dd> <dl> <dt>

159 (0x9F)
</dt> <dt>



Die Adresse für die Thread-ID ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**FEHLER \_ BEI \_ UNGÜLTIGEN ARGUMENTEN**
</dt> <dd> <dl> <dt>

160 (0xA0)
</dt> <dt>



Mindestens ein Argument ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR \_ BAD \_ PATHNAME**
</dt> <dd> <dl> <dt>

161 (0xA1)
</dt> <dt>



Der angegebene Pfad ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**FEHLERSIGNAL \_ \_ AUSSTEHEND**
</dt> <dd> <dl> <dt>

162 (0xA2)
</dt> <dt>



Ein Signal steht bereits aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**FEHLER \_ \_ MAX. THRDS \_ ERREICHT**
</dt> <dd> <dl> <dt>

164 (0xA4)
</dt> <dt>



Im System können keine weiteren Threads mehr erstellt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_FEHLER: FEHLER BEI DER SPERRE \_**
</dt> <dd> <dl> <dt>

167 (0xA7)
</dt> <dt>



Ein Bereich einer Datei kann nicht gesperrt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUSY"></span><span id="error_busy"></span>**FEHLER \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

170 (0xAA)
</dt> <dt>



Die angeforderte Ressource wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**FEHLER \_ BEI \_ GERÄTEUNTERSTÜTZUNG IN \_ \_ BEARBEITUNG**
</dt> <dd> <dl> <dt>

171 (0xAB)
</dt> <dt>



Die Befehlsunterstützungserkennung des Geräts wird ausgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**FEHLER: \_ \_ ABBRUCHVERLETZUNG**
</dt> <dd> <dl> <dt>

173 (0xAD)
</dt> <dt>



Für den angegebenen Abbruchbereich war keine Sperranforderung ausstehend.


</dt> </dl> </dd> <dt>

<span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR \_ ATOMIC \_ LOCKS NOT SUPPORTED (FEHLER: ATOMIC-SPERREN \_ WERDEN NICHT \_ UNTERSTÜTZT)**
</dt> <dd> <dl> <dt>

174 (0xAE)
</dt> <dt>



Das Dateisystem unterstützt keine atomaren Änderungen am Sperrtyp.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ SEGMENTNUMMER**
</dt> <dd> <dl> <dt>

180 (0xB4)
</dt> <dt>



Das System hat eine Segmentnummer erkannt, die nicht richtig war.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**FEHLER: \_ \_ UNGÜLTIGE ORDINALZAHL**
</dt> <dd> <dl> <dt>

182 (0xB6)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**FEHLER \_ \_ BEREITS VORHANDEN**
</dt> <dd> <dl> <dt>

183 (0xB7)
</dt> <dt>



Eine Datei kann nicht erstellt werden, wenn die Datei bereits vorhanden ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ FLAGNUMMER**
</dt> <dd> <dl> <dt>

186 (0xBA)
</dt> <dt>



Das übergebene Flag ist nicht korrekt.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**FEHLER \_ SEM \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

187 (0xBB)
</dt> <dt>



Der angegebene Systemsemaphorname wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ STARTCODESEG**
</dt> <dd> <dl> <dt>

188 (0xBC)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**FEHLER: \_ \_ UNGÜLTIGE STACKSEG**
</dt> <dd> <dl> <dt>

189 (0xBD)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR \_ INVALID \_ MODULETYPE**
</dt> <dd> <dl> <dt>

190 (0xBE)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ EXE-SIGNATUR**
</dt> <dd> <dl> <dt>

191 (0xBF)
</dt> <dt>



%1 kann nicht im Win32-Modus ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ALS \_ \_ UNGÜLTIG MARKIERTE FEHLER-EXE \_**
</dt> <dd> <dl> <dt>

192 (0xC0)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ EXE-FORMAT**
</dt> <dd> <dl> <dt>

193 (0xC1)
</dt> <dt>



%1 ist keine gültige Win32-Anwendung.


</dt> </dl> </dd> <dt>

<span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**FEHLER \_ BEI ITERIERTEN \_ DATEN \_ ÜBERSCHREITET \_ 64.000**
</dt> <dd> <dl> <dt>

194 (0xC2)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**FEHLER: \_ \_ UNGÜLTIGER MINALLOCSIZE-FEHLER**
</dt> <dd> <dl> <dt>

195 (0xC3)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**FEHLER \_ DYNLINK \_ VON \_ UNGÜLTIGEN \_ RING**
</dt> <dd> <dl> <dt>

196 (0xC4)
</dt> <dt>



Das Betriebssystem kann dieses Anwendungsprogramm nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**FEHLER \_ IOPL \_ NICHT \_ AKTIVIERT**
</dt> <dd> <dl> <dt>

197 (0xC5)
</dt> <dt>



Das Betriebssystem ist derzeit nicht für die Ausführung dieser Anwendung konfiguriert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**FEHLER: \_ UNGÜLTIGE \_ SEGDPL**
</dt> <dd> <dl> <dt>

198 (0xC6)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**FEHLER \_ AUTODATASEG \_ ÜBERSCHREITET \_ 64.000**
</dt> <dd> <dl> <dt>

199 (0xC7)
</dt> <dt>



Das Betriebssystem kann dieses Anwendungsprogramm nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**FEHLER \_ RING2SEG \_ MUSS \_ \_ VERSCHIEBBAR SEIN**
</dt> <dd> <dl> <dt>

200 (0xC8)
</dt> <dt>



Das Codesegment darf nicht größer oder gleich 64 KB sein.


</dt> </dl> </dd> <dt>

<span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**\_FEHLER: \_ RELOC CHAIN \_ XEEDS \_ SEGLIM**
</dt> <dd> <dl> <dt>

201 (0xC9)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**FEHLER \_ INFLOOP \_ IN \_ RELOC \_ CHAIN**
</dt> <dd> <dl> <dt>

202 (0xCA)
</dt> <dt>



Das Betriebssystem kann %1 nicht ausführen.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**FEHLER \_ ENVVAR \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

203 (0xCB)
</dt> <dt>



Das System konnte die eingegebene Umgebungsoption nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**FEHLER: \_ KEIN \_ SIGNAL \_ GESENDET**
</dt> <dd> <dl> <dt>

205 (0xCD)
</dt> <dt>



Kein Prozess in der Befehlsunterstruktur verfügt über einen Signalhandler.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR \_ FILENAME \_ EXCED \_ RANGE**
</dt> <dd> <dl> <dt>

206 (0xCE)
</dt> <dt>



Der Dateiname oder die Erweiterung ist zu lang.


</dt> </dl> </dd> <dt>

<span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**VERWENDETER \_ \_ FEHLERRING2-STAPEL \_ \_**
</dt> <dd> <dl> <dt>

207 (0xCF)
</dt> <dt>



Der Ring 2-Stapel wird verwendet.


</dt> </dl> </dd> <dt>

<span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**\_ \_ FEHLERMETAERWEITERUNG ZU \_ \_ LANG**
</dt> <dd> <dl> <dt>

208 (0xD0)
</dt> <dt>



Die globalen Dateinamenzeichen \* oder ?werden falsch eingegeben, oder es werden zu viele globale Dateinamenzeichen angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**FEHLER: \_ UNGÜLTIGE \_ \_ SIGNALNUMMER**
</dt> <dd> <dl> <dt>

209 (0xD1)
</dt> <dt>



Das gesendete Signal ist nicht richtig.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**\_FEHLERTHREAD \_ 1 \_ INAKTIV**
</dt> <dd> <dl> <dt>

210 (0xD2)
</dt> <dt>



Der Signalhandler kann nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOCKED"></span><span id="error_locked"></span>**FEHLER \_ GESPERRT**
</dt> <dd> <dl> <dt>

212 (0xD4)
</dt> <dt>



Das Segment ist gesperrt und kann nicht neu zugeordnet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**FEHLER \_ BEI ZU \_ \_ VIELEN MODULEN**
</dt> <dd> <dl> <dt>

214 (0xD6)
</dt> <dt>



Zu viele Dynamic Link-Module sind an dieses Programm oder dynamic-link-Modul angefügt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_FEHLERSCHACHTELUNG \_ NICHT \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

215 (0xD7)
</dt> <dt>



Aufrufe von LoadModule können nicht geschachtelt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**FEHLER: \_ \_ NICHT \_ ÜBEREINSTIMMENDER COMPUTERTYP DER EXE-DATEI \_**
</dt> <dd> <dl> <dt>

216 (0xD8)
</dt> <dt>



Diese Version von %1 ist nicht mit der Version von Windows kompatibel, die Sie ausführen. Überprüfen Sie die Systeminformationen Ihres Computers, und wenden Sie sich dann an den Softwareherausgeber.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**\_FEHLER-EXE \_ KANN \_ \_ \_ SIGNIERTE BINÄRDATEI NICHT ÄNDERN**
</dt> <dd> <dl> <dt>

217 (0xD9)
</dt> <dt>



Die Imagedatei %1 ist signiert und kann nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR \_ EXE CANNOT MODIFY STRONG SIGNED BINARY (FEHLER-EXE \_ KANN DIE \_ \_ BINÄRDATEI MIT \_ STARKEM VORZEICHEN NICHT ÄNDERN) \_**
</dt> <dd> <dl> <dt>

218 (0xDA)
</dt> <dt>



Die Imagedatei %1 ist stark signiert und kann nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**FEHLERDATEI \_ \_ AUSGECHECKT \_**
</dt> <dd> <dl> <dt>

220 (0xDC)
</dt> <dt>



Diese Datei wird für die Bearbeitung durch einen anderen Benutzer ausgecheckt oder gesperrt.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**FEHLER \_ BEIM AUSCHECKEN \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

221 (0xDD)
</dt> <dt>



Die Datei muss vor dem Speichern von Änderungen ausgecheckt werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**FEHLER: \_ \_ UNGÜLTIGER \_ DATEITYP**
</dt> <dd> <dl> <dt>

222 (0xDE)
</dt> <dt>



Der dateityp, der gespeichert oder abgerufen wird, wurde blockiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**FEHLERDATEI \_ \_ ZU \_ GROß**
</dt> <dd> <dl> <dt>

223 (0xDF)
</dt> <dt>



Die Dateigröße überschreitet den zulässigen Grenzwert und kann nicht gespeichert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_ \_ FEHLERFORMULARAUTHENTIFIZIERUNG \_ ERFORDERLICH**
</dt> <dd> <dl> <dt>

224 (0xE0)
</dt> <dt>



Zugriff verweigert. Bevor Sie Dateien an diesem Speicherort öffnen, müssen Sie zuerst die Website ihrer Liste der vertrauenswürdigen Websites hinzufügen, zur Website navigieren und die Option zum automatischen Anmelden auswählen.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**FEHLER: \_ \_ VIRUS INFIZIERT**
</dt> <dd> <dl> <dt>

225 (0xE1)
</dt> <dt>



Der Vorgang wurde nicht erfolgreich abgeschlossen, da die Datei einen Virus oder potenziell unerwünschte Software enthält.


</dt> </dl> </dd> <dt>

<span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR \_ VIRUS \_ DELETED**
</dt> <dd> <dl> <dt>

226 (0xE2)
</dt> <dt>



Diese Datei enthält einen Virus oder potenziell unerwünschte Software und kann nicht geöffnet werden. Aufgrund der Art dieses Virus oder potenziell unerwünschter Software wurde die Datei von diesem Speicherort entfernt.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR \_ PIPE \_ LOCAL**
</dt> <dd> <dl> <dt>

229 (0xE5)
</dt> <dt>



Die Pipe ist lokal.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**FEHLER: \_ FEHLERHAFTE \_ PIPE**
</dt> <dd> <dl> <dt>

230 (0xE6)
</dt> <dt>



Der Pipezustand ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**FEHLERPIPE \_ \_ AUSGELASTET**
</dt> <dd> <dl> <dt>

231 (0xE7)
</dt> <dt>



Alle Pipeinstanzen sind ausgelastet.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**FEHLER \_ KEINE \_ DATEN**
</dt> <dd> <dl> <dt>

232 (0xE8)
</dt> <dt>



Die Pipe wird geschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**FEHLERPIPE \_ \_ NICHT \_ VERBUNDEN**
</dt> <dd> <dl> <dt>

233 (0xE9)
</dt> <dt>



Am anderen Ende der Pipe befindet sich kein Prozess.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**\_FEHLER BEI WEITEREN \_ DATEN**
</dt> <dd> <dl> <dt>

234 (0xEA)
</dt> <dt>



Weitere Daten sind verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**FEHLER \_ VC \_ GETRENNT**
</dt> <dd> <dl> <dt>

240 (0xF0)
</dt> <dt>



Die Sitzung wurde abgebrochen.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**FEHLER: \_ UNGÜLTIGER \_ \_ EA-NAME**
</dt> <dd> <dl> <dt>

254 (0xFE)
</dt> <dt>



Der angegebene name des erweiterten Attributs war ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**FEHLER \_ \_ EA-LISTE \_ INKONSISTENT**
</dt> <dd> <dl> <dt>

255 (0xFF)
</dt> <dt>



Die erweiterten Attribute sind inkonsistent.


</dt> </dl> </dd> <dt>

<span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT \_ TIMEOUT**
</dt> <dd> <dl> <dt>

258 (0x102)
</dt> <dt>



Timeout bei Wartevorgang.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**FEHLER: \_ KEINE \_ WEITEREN \_ ELEMENTE**
</dt> <dd> <dl> <dt>

259 (0x103)
</dt> <dt>



Es sind keine weiteren Daten verfügbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**FEHLER \_ KANN NICHT KOPIERT \_ WERDEN**
</dt> <dd> <dl> <dt>

266 (0x10A)
</dt> <dt>



Die Kopierfunktionen können nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR \_ DIRECTORY**
</dt> <dd> <dl> <dt>

267 (0x10B)
</dt> <dt>



Der Verzeichnisname ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**FEHLER, \_ DASS EAS \_ NICHT \_ PASST**
</dt> <dd> <dl> <dt>

275 (0x113)
</dt> <dt>



Die erweiterten Attribute passten nicht in den Puffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**FEHLER \_ \_ EA-DATEI \_ BESCHÄDIGT**
</dt> <dd> <dl> <dt>

276 (0x114)
</dt> <dt>



Die erweiterte Attributdatei im eingebundenen Dateisystem ist beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**FEHLER \_ EA \_ TABLE \_ FULL**
</dt> <dd> <dl> <dt>

277 (0x115)
</dt> <dt>



Die erweiterte Attributtabellendatei ist voll.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**FEHLER: \_ UNGÜLTIGES \_ \_ EA-HANDLE**
</dt> <dd> <dl> <dt>

278 (0x116)
</dt> <dt>



Das angegebene erweiterte Attributhandle ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**FEHLER \_ EAS \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

282 (0x11A)
</dt> <dt>



Das bereitgestellte Dateisystem unterstützt keine erweiterten Attribute.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**FEHLER \_ NICHT \_ BESITZER**
</dt> <dd> <dl> <dt>

288 (0x120)
</dt> <dt>



Versuchen Sie, Mutex frei zu geben, der nicht im Besitz des Aufrufers ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**FEHLER: \_ ZU \_ VIELE \_ BEITRÄGE**
</dt> <dd> <dl> <dt>

298 (0x12A)
</dt> <dt>



Zu viele Beiträge wurden an einem Semaphor vorgenommen.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**FEHLER \_ BEIM \_ TEILKOPIEREN**
</dt> <dd> <dl> <dt>

299 (0x12B)
</dt> <dt>



Nur ein Teil einer ReadProcessMemory- oder WriteProcessMemory-Anforderung wurde abgeschlossen.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**FEHLER \_ OPLOCK \_ NICHT \_ GEWÄHRT**
</dt> <dd> <dl> <dt>

300 (0x12C)
</dt> <dt>



Die Oplockanforderung wird verweigert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**FEHLER: \_ UNGÜLTIGES \_ OPLOCK-PROTOKOLL \_**
</dt> <dd> <dl> <dt>

301 (0x12D)
</dt> <dt>



Vom System wurde eine ungültige Oplockbestätigung empfangen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**\_FEHLERDATENTRÄGER \_ ZU \_ FRAGMENTIERT**
</dt> <dd> <dl> <dt>

302 (0x12E)
</dt> <dt>



Das Volume ist zu fragmentiert, um diesen Vorgang abschließen zu können.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**FEHLER \_ BEIM LÖSCHEN \_ AUSSTEHEND**
</dt> <dd> <dl> <dt>

303 (0x12F)
</dt> <dt>



Die Datei kann nicht geöffnet werden, da sie gerade gelöscht wird.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**FEHLER, \_ DER MIT \_ DER \_ \_ REGISTRIERUNGSEINSTELLUNG "GLOBALER \_ \_ KURZNAME" NICHT KOMPATIBEL \_ IST**
</dt> <dd> <dl> <dt>

304 (0x130)
</dt> <dt>



Kurznameneinstellungen können auf diesem Volume aufgrund der globalen Registrierungseinstellung nicht geändert werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**FEHLER: \_ \_ KURZNAMEN \_ SIND AUF VOLUME \_ NICHT \_ \_ AKTIVIERT**
</dt> <dd> <dl> <dt>

305 (0x131)
</dt> <dt>



Kurznamen sind auf diesem Volume nicht aktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**\_ \_ FEHLERSICHERHEITSSTREAM \_ IST \_ INKONSISTENT**
</dt> <dd> <dl> <dt>

306 (0x132)
</dt> <dt>



Der Sicherheitsstream für das gegebene Volume befindet sich in einem inkonsistenten Zustand. Führen Sie CHKDSK auf dem Volume aus.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**FEHLER \_ UNGÜLTIGER \_ \_ SPERRBEREICH**
</dt> <dd> <dl> <dt>

307 (0x133)
</dt> <dt>



Ein angeforderter Dateisperrvorgang kann aufgrund eines ungültigen Bytebereichs nicht verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_ \_ FEHLERBILDSUBSYSTEM \_ \_ NICHT VORHANDEN**
</dt> <dd> <dl> <dt>

308 (0x134)
</dt> <dt>



Das Subsystem, das zur Unterstützung des Imagetyps erforderlich ist, ist nicht vorhanden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**\_ \_ FEHLERBENACHRICHTIGUNGS-GUID \_ BEREITS \_ DEFINIERT**
</dt> <dd> <dl> <dt>

309 (0x135)
</dt> <dt>



Der angegebenen Datei ist bereits eine Benachrichtigungs-GUID zugeordnet.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**FEHLER \_ \_ UNGÜLTIGER \_ AUSNAHMEHANDLER**
</dt> <dd> <dl> <dt>

310 (0x136)
</dt> <dt>



Eine ungültige Ausnahmehandlerroutine wurde erkannt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**FEHLER \_ BEI \_ DOPPELTEN BERECHTIGUNGEN**
</dt> <dd> <dl> <dt>

311 (0x137)
</dt> <dt>



Für das Token wurden doppelte Berechtigungen angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**FEHLER: \_ KEINE \_ BEREICHE \_ VERARBEITET**
</dt> <dd> <dl> <dt>

312 (0x138)
</dt> <dt>



Es konnten keine Bereiche für den angegebenen Vorgang verarbeitet werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**FEHLER \_ IN \_ \_ \_ SYSTEMDATEI NICHT \_ ZULÄSSIG**
</dt> <dd> <dl> <dt>

313 (0x139)
</dt> <dt>



Der Vorgang ist für eine interne Dateisystemdatei nicht zulässig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**FEHLER: \_ \_ DATENTRÄGERRESSOURCEN \_ SIND ERSCHÖPFT**
</dt> <dd> <dl> <dt>

314 (0x13A)
</dt> <dt>



Die physischen Ressourcen dieses Datenträgers sind erschöpft.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**FEHLER: \_ UNGÜLTIGES \_ TOKEN**
</dt> <dd> <dl> <dt>

315 (0x13B)
</dt> <dt>



Das Token, das die Daten darstellt, ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**\_GERÄTEFUNKTION \_ \_ "FEHLER" WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

316 (0x13C)
</dt> <dt>



Das Gerät unterstützt das Befehlsfeature nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**FEHLER \_ MR MID NICHT \_ \_ \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

317 (0x13D)
</dt> <dt>



Das System kann den Meldungstext für die Meldungsnummer 0x%1 in der Meldungsdatei für %2 nicht finden.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**FEHLERBEREICH \_ \_ NICHT \_ GEFUNDEN**
</dt> <dd> <dl> <dt>

318 (0x13E)
</dt> <dt>



Der angegebene Bereich wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**FEHLER: \_ NICHT DEFINIERTER \_ BEREICH**
</dt> <dd> <dl> <dt>

319 (0x13F)
</dt> <dt>



Die angegebene zentrale Zugriffsrichtlinie ist auf dem Zielcomputer nicht definiert.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**FEHLER: \_ UNGÜLTIGE \_ OBERGRENZE**
</dt> <dd> <dl> <dt>

320 (0x140)
</dt> <dt>



Die aus Active Directory erhaltene zentrale Zugriffsrichtlinie ist ungültig.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**FEHLER \_ GERÄT \_ NICHT ERREICHBAR**
</dt> <dd> <dl> <dt>

321 (0x141)
</dt> <dt>



Das Gerät ist nicht erreichbar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**FEHLER \_ GERÄT \_ KEINE \_ RESSOURCEN**
</dt> <dd> <dl> <dt>

322 (0x142)
</dt> <dt>



Das Zielgerät verfügt nicht über genügend Ressourcen, um den Vorgang abschließen zu können.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**FEHLER \_ BEI \_ DATEN-PRÜFSUMMENFEHLER \_**
</dt> <dd> <dl> <dt>

323 (0x143)
</dt> <dt>



Fehler bei der Prüfsumme der Datenintegrität. Daten im Dateistream sind beschädigt.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**FEHLER BEIM \_ INTERMIXED \_ KERNEL \_ \_ EA-VORGANG**
</dt> <dd> <dl> <dt>

324 (0x144)
</dt> <dt>



Es wurde versucht, sowohl einen KERNEL als auch ein normales erweitertes Attribut (EA) im gleichen Vorgang zu ändern.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**FEHLER: \_ TRIM \_ AUF \_ \_ DATEIEBENE WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

326 (0x146)
</dt> <dt>



Das Gerät unterstützt trim auf Dateiebene nicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_ \_ FEHLERVERSATZAUSRICHTUNGSVERLETZUNG \_**
</dt> <dd> <dl> <dt>

327 (0x147)
</dt> <dt>



Der Befehl hat einen Datenoffset angegeben, der nicht an der Granularität/Ausrichtung des Geräts ausgerichtet ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**FEHLER: \_ \_ UNGÜLTIGES FELD \_ IN DER \_ \_ PARAMETERLISTE**
</dt> <dd> <dl> <dt>

328 (0x148)
</dt> <dt>



Der Befehl hat ein ungültiges Feld in seiner Parameterliste angegeben.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**FEHLERVORGANG \_ \_ WIRD \_ DURCHGEFÜHRT**
</dt> <dd> <dl> <dt>

329 (0x149)
</dt> <dt>



Derzeit wird ein Vorgang mit dem Gerät durchgeführt.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**FEHLER: \_ \_ FEHLERHAFTER \_ GERÄTEPFAD**
</dt> <dd> <dl> <dt>

330 (0x14A)
</dt> <dt>



Es wurde versucht, den Befehl über einen ungültigen Pfad zum Zielgerät zu senden.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**FEHLER \_ ZU \_ VIELE \_ DESKRIPTOREN**
</dt> <dd> <dl> <dt>

331 (0x14B)
</dt> <dt>



Der Befehl hat eine Anzahl von Deskriptoren angegeben, die das vom Gerät unterstützte Maximum überschritten haben.


</dt> </dl> </dd> <dt>

<span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**\_ \_ FEHLERBEREINIGUNGSDATEN \_ DEAKTIVIERT**
</dt> <dd> <dl> <dt>

332 (0x14C)
</dt> <dt>



Die Bereinigung ist für die angegebene Datei deaktiviert.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**FEHLER \_ NICHT \_ REDUNDANTER \_ SPEICHER**
</dt> <dd> <dl> <dt>

333 (0x14D)
</dt> <dt>



Das Speichergerät bietet keine Redundanz.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**FEHLER: \_ \_ RESIDENTE DATEI \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

334 (0x14E)
</dt> <dt>



Ein Vorgang wird für eine residente Datei nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**FEHLER: \_ KOMPRIMIERTE \_ DATEI WIRD NICHT \_ \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

335 (0x14F)
</dt> <dt>



Ein Vorgang wird für eine komprimierte Datei nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**FEHLERVERZEICHNIS \_ \_ WIRD NICHT \_ UNTERSTÜTZT**
</dt> <dd> <dl> <dt>

336 (0x150)
</dt> <dt>



Ein Vorgang wird in einem Verzeichnis nicht unterstützt.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**FEHLER \_ NICHT \_ AUS \_ \_ KOPIERVORGANG GELESEN**
</dt> <dd> <dl> <dt>

337 (0x151)
</dt> <dt>



Die angegebene Kopie der angeforderten Daten konnte nicht gelesen werden.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**FEHLER: \_ \_ NOACTION-NEUSTART FEHLGESCHLAGEN \_**
</dt> <dd> <dl> <dt>

350 (0x15E)
</dt> <dt>



Es wurde keine Aktion ausgeführt, da ein Systemneustart erforderlich ist.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**FEHLER \_ BEIM \_ HERUNTERFAHREN**
</dt> <dd> <dl> <dt>

351 (0x15F)
</dt> <dt>



Fehler beim Herunterfahren.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**FEHLER: \_ NEUSTARTFEHLER \_**
</dt> <dd> <dl> <dt>

352 (0x160)
</dt> <dt>



Fehler beim Neustart.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**FEHLER: \_ MAXIMALE ANZAHL VON SITZUNGEN \_ \_ ERREICHT**
</dt> <dd> <dl> <dt>

353 (0x161)
</dt> <dt>



Die maximale Anzahl von Sitzungen wurde erreicht.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**\_FEHLERTHREADMODUS \_ BEREITS IM \_ \_ HINTERGRUND**
</dt> <dd> <dl> <dt>

400 (0x190)
</dt> <dt>



Der Thread befindet sich bereits im Hintergrundverarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_FEHLERTHREADMODUS \_ NICHT \_ \_ HINTERGRUND**
</dt> <dd> <dl> <dt>

401 (0x191)
</dt> <dt>



Der Thread befindet sich nicht im Hintergrundverarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**\_ \_ FEHLERPROZESSMODUS BEREITS IM \_ \_ HINTERGRUND**
</dt> <dd> <dl> <dt>

402 (0x192)
</dt> <dt>



Der Prozess befindet sich bereits im Hintergrundverarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**\_ \_ FEHLERPROZESSMODUS NICHT \_ \_ HINTERGRUND**
</dt> <dd> <dl> <dt>

403 (0x193)
</dt> <dt>



Der Prozess befindet sich nicht im Hintergrundverarbeitungsmodus.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**FEHLER: \_ UNGÜLTIGE \_ ADRESSE**
</dt> <dd> <dl> <dt>

487 (0x1E7)
</dt> <dt>



Versuchen Sie, auf eine ungültige Adresse zuzugreifen.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>WinError.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systemfehlercodes](system-error-codes.md)
</dt> </dl>

 

 




