---
title: Bits-Rückgabewerte
description: Die Datei "bitsmsg. h" enthält die folgenden Rückgabewert Konstanten.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- Fehler Bits
- Fehler Bits, Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948987"
---
# <a name="bits-return-values"></a>Bits-Rückgabewerte

Die Datei "bitsmsg. h" enthält die folgenden Rückgabewert Konstanten. Die Konstanten stellen Rückgabewerte dar, die von Bits generiert werden, und http-Rückgabewerte, die Bits erfasst. Alle anderen Rückgabewerte, die Sie empfangen können, sind com-, RPC-oder konvertierte Windows-Rückgabewerte (Bits verwendet das [HRESULT \_ aus \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) -Makro, um die Windows-Rückgabewerte in HRESULT-Werte zu konvertieren).

Beachten Sie, dass die Datei "bitsmsg. h" zusätzliche Rückgabewerte enthält, die unten nicht aufgeführt sind.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG \_ S \_ partiell \_ vollständig (0x00200017)
</dt> <dd>

Eine Teilmenge der Auftragsdateien wurde erfolgreich übertragen, bevor die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufgerufen wurde. Die, die nicht fertig waren, wurden gelöscht.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ können \_ \_ Dateien nicht löschen \_ (0x0020001a)
</dt> <dd>

Es können nicht alle temporären Dateien gelöscht werden, die dem Auftrag zugeordnet sind.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>\_ \_ Durch Richtlinie überschriebene BG S \_ \_ (0x00200055)
</dt> <dd>

Die Konfigurationseinstellung wurde erfolgreich gespeichert, aber die Einstellung wird nicht verwendet, da eine konfigurierte Gruppenrichtlinie Einstellung die Einstellung überschreibt.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ nicht \_ gefunden (0x80200001)
</dt> <dd>

Der angeforderte Auftrag wurde nicht gefunden.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG \_ E \_ ungültiger \_ Zustand (0x80200002)
</dt> <dd>

Die angeforderte Aktion ist im aktuellen Auftragszustand unzulässig.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ empty (0x80200003)
</dt> <dd>

Der Auftrag muss eine oder mehrere Dateien enthalten, bevor Sie den Auftrag fortsetzen können.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG- \_ E- \_ Datei \_ nicht \_ verfügbar (0x80200004)
</dt> <dd>

Die Dateiinformationen sind nicht verfügbar, da der Fehler keiner lokalen oder Remote Datei zugeordnet ist.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>Das BG \_ E- \_ Protokoll ist \_ nicht \_ verfügbar (0x80200005).
</dt> <dd>

Protokollinformationen sind nicht verfügbar, da der Fehler dem angegebenen Übertragungsprotokoll nicht zugeordnet ist.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E \_ \_ -Ziel gesperrt (0x8020000d)
</dt> <dd>

Das im lokalen Dateinamen angegebene Ziel Dateisystem-Volume ist gesperrt.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG \_ E- \_ Volume \_ geändert (0x8020000E)
</dt> <dd>

Das im lokalen Dateinamen angegebene Ziel Volume wurde geändert. Die ursprüngliche Diskette wurde z. b. durch eine andere Diskette ersetzt.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG \_ E- \_ Fehler \_ Informationen nicht \_ verfügbar (0x8020000f)
</dt> <dd>

Fehlerinformationen sind nur verfügbar, wenn der Status des Auftrags "BG- \_ Auftragsstatus" lautet \_ \_ . Die Fehlerinformationen sind nicht verfügbar, nachdem Bits mit der Übertragung der Auftragsdaten begonnen hat oder der Client beendet wurde.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ \_ (Netzwerk getrennt) (0x80200010)
</dt> <dd>

Der Netzwerkadapter ist inaktiv oder nicht getrennt. Alle Aufträge werden in den Status " \_ \_ vorübergehender Status des BG-Auftragsstatus" versetzt \_ \_ .

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E \_ fehlende \_ Datei \_ Größe (0x80200011)
</dt> <dd>

Der Server hat die Dateigröße nicht zurückgegeben. Bits überträgt nur statischen Inhalt und erfordert, dass der HTTP-Server den Content-Length-Header zurückgibt. Die Übertragungs Anforderung schlägt fehl, wenn die URL auf dynamischen Inhalt verweist.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG \_ E \_ unzureichende \_ http- \_ Unterstützung (0x80200012)
</dt> <dd>

Das HTTP/1.1-Protokoll wird vom Server nicht unterstützt.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG \_ E \_ unzureichende \_ Bereichs \_ Unterstützung (0x80200013)
</dt> <dd>

Der Content-Range-Header wird vom Server nicht unterstützt. Normalerweise erhalten Sie diesen Fehler, wenn Sie versuchen, dynamischen Inhalt herunterzuladen. Dieser Fehler kann auch ausgegeben werden, wenn ein zwischen Proxy den Content-Range-Header oder den Content-Length-Header entfernt.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ nicht \_ unterstützt (0x80200014)
</dt> <dd>

Die Remote Verwendung von Bits wird nicht unterstützt. Weitere Informationen finden Sie unter [Benutzer und Netzwerkverbindungen](users-and-network-connections.md).

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ neue \_ Besitzer \_ diff- \_ Zuordnung (0x80200015)
</dt> <dd>

Die Zuordnung des Netzwerklaufwerks für die lokale Datei ist für den aktuellen Besitzer anders als für den vorherigen Besitzer.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ New \_ Owner \_ No \_ file \_ Access (0x80200016)
</dt> <dd>

Der neue Besitzer verfügt nicht über ausreichende Berechtigungen für die temporären Auftragsdateien.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG \_ E- \_ Proxy \_ Liste \_ zu \_ groß (0x80200018)
</dt> <dd>

Die Liste der HTTP-Proxys ist zu lang. Die Liste darf 32 KB nicht überschreiten.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG \_ E \_ Proxy \_ Umgehungs \_ Liste \_ zu \_ groß (0x80200019)
</dt> <dd>

Die Liste der HTTP-Proxy Umgehungen ist zu lang. Die Liste darf 32 KB nicht überschreiten.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ zu \_ viele \_ Dateien (0x8020001c)
</dt> <dd>

Sie können einem Uploadauftrag nicht mehr als eine Datei hinzufügen.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_Lokale BG \_ E \_ \_ -Datei geändert (0x8020001d)
</dt> <dd>

Der Inhalt der lokalen Datei wurde geändert, nachdem der Übertragungsvorgang begonnen hat. Der Inhalt der lokalen Datei kann nicht geändert werden, nachdem der Übertragungsvorgang bei einem Upload-oder Upload-Reply-Auftrag gestartet wurde.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ zu \_ groß (0x80200020)
</dt> <dd>

Die Größe der Uploaddatei überschreitet die auf dem Server angegebene maximal zulässige Uploadgröße.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG \_ E \_ Zeichenfolge \_ zu \_ lang (0x80200021)
</dt> <dd>

Die angegebene Zeichenfolge ist zu lang.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>Nicht übereinstimmende BG \_ E- \_ Client \_ Server \_ Protokoll \_ (0x80200022)
</dt> <dd>

Der Client und der Server konnten kein Protokoll aushandeln, das für den Uploadauftrag verwendet werden kann.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG \_ E \_ Server \_ Execute \_ aktiviert (0x80200023)
</dt> <dd>

Skripterstellung oder Ausführungs Berechtigungen werden für das virtuelle IIS-Verzeichnis aktiviert, das dem Auftrag zugeordnet ist. Zum Hochladen von Dateien in das virtuelle Verzeichnis deaktivieren Sie die Skripterstellung und Ausführungs Berechtigungen für das virtuelle Verzeichnis.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ username \_ zu \_ groß (0x80200025)
</dt> <dd>

Der Benutzername darf nicht länger als 300 Zeichen sein.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E \_ Kennwort \_ zu \_ groß (0x80200026)
</dt> <dd>

Das Kennwort darf nicht länger als 65535 Zeichen sein.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG \_ E \_ Ungültiges Authentifizierungs \_ \_ Ziel (0x80200027)
</dt> <dd>

Das angegebene Authentifizierungs Ziel ist ungültig.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG \_ E \_ Ungültiges Authentifizierungs \_ \_ Schema (0x80200028)
</dt> <dd>

Das angegebene Authentifizierungsschema ist ungültig.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E \_ ungültiger \_ Bereich (0x8020002b)
</dt> <dd>

Der angegebene Byte Bereich ist ungültig. Der Byte Bereich muss in der angegebenen Remote Datei vorhanden sein.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG \_ E über \_ Lapp Ende \_ Bereiche (0x8020002c)
</dt> <dd>

Die Liste der Byte Bereiche enthält überlappende oder doppelte Bereiche, die nicht unterstützt werden.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ \_ von \_ Richtlinie blockiert (0x8020003E)
</dt> <dd>

Gruppenrichtlinie Einstellungen verhindern, dass Hintergrund Aufträge zu diesem Zeitpunkt ausgeführt werden. Weitere Informationen finden Sie in der [MaxInternetBandwidth](group-policies.md) -Richtlinie.

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E \_ ungültige \_ Proxy \_ Informationen (0x8020003f)
</dt> <dd>

Laufzeitfehler, der angibt, dass die Proxy Liste oder Proxy Umgehungs Liste, die Sie mithilfe der [**ibackgroundcopyjob:: setproxysettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) -Methode angegeben haben, ungültig ist.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E \_ ungültige \_ Anmelde Informationen (0x80200040)
</dt> <dd>

Das Format der angegebenen Sicherheits Anmelde Informationen ist ungültig.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG \_ E- \_ Datensatz \_ gelöscht (0x80200042)
</dt> <dd>

Der Cache Daten Satz wurde gelöscht. Der Versuch, ihn zu aktualisieren, wurde abgebrochen.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG \_ E \_ UPnP- \_ Fehler (0x80200045)
</dt> <dd>

Ein Universal Plug & Play (UPnP)-Fehler ist aufgetreten. Überprüfen Sie Ihr Internet Gateway-Gerät.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E \_ Peer Caching \_ deaktiviert (0x80200047)
</dt> <dd>

Peer-Caching ist deaktiviert.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ busycacherecord (0x80200048)
</dt> <dd>

Der Cache Daten Satz wird verwendet und kann nicht geändert oder gelöscht werden. Versuchen Sie es nach einigen Sekunden erneut.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ zu \_ viele \_ Aufträge \_ pro \_ Benutzer (0x80200049)
</dt> <dd>

Die Auftrags Anzahl für den Benutzer hat den Auftrags Grenzwert pro Benutzer überschritten, der durch die Einstellung "maxjobsperGruppenrichtlinie User" festgelegt wurde.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ zu \_ viele \_ Aufträge \_ pro \_ Computer (0x80200050)
</dt> <dd>

Die Auftrags Anzahl für den Computer hat den Auftrags Grenzwert pro Computer überschritten, der durch die Einstellung maxjobspermachine Gruppenrichtlinie festgelegt wurde.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ zu \_ viele \_ Dateien \_ im \_ Auftrag (0x80200051)
</dt> <dd>

Die Dateianzahl für den Auftrag hat das von der Einstellung maxfilesperjob Gruppenrichtlinie festgelegte Limit für die pro-Auftragsdatei überschritten.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ zu \_ viele \_ Bereiche \_ in der \_ Datei (0x80200052)
</dt> <dd>

Die Bereichs Anzahl für die Datei hat den Grenzwert pro Datei Bereich überschritten, der durch die Einstellung "maxrangesperGruppenrichtlinie file" festgelegt wurde.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG \_ E- \_ Validierung \_ fehlgeschlagen (0x80200053)
</dt> <dd>

Die Anwendung hat Daten von einer Website angefordert, aber die Antwort war nicht gültig. Ausführliche Informationen finden Sie unter Verwenden von Ereignisanzeige zum Anzeigen des Betriebs Protokolls für die Anwendungsprotokolle von \\ Microsoft \\ Windows \\ BITS-Client \\ .

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG \_ E \_ maxdownload \_ Timeout (0x80200054)
</dt> <dd>

Beim Herunterladen des Auftrags durch Bits ist ein Timeout aufgetreten. Der Download konnte nicht innerhalb der maximalen Downloadzeit, die für den Auftrag festgelegt wurde, oder in der Gruppenrichtlinie Einstellung maxdownloadtime ausgeführt werden.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG \_ E \_ http- \_ Fehler \_ 400 (0x80190190)
</dt> <dd>

Der Server konnte die Übertragungs Anforderung nicht verarbeiten, da die Syntax des Remote Dateinamens ungültig ist.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG \_ E \_ http- \_ Fehler \_ 401 (0x80190191)
</dt> <dd>

Der Benutzer verfügt nicht über die Berechtigung für den Zugriff auf die Remote Datei. Für die angeforderte Ressource ist eine Benutzerauthentifizierung erforderlich.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG \_ E \_ http- \_ Fehler \_ 404 (0x80190194)
</dt> <dd>

Die angeforderte URL ist auf dem Server nicht vorhanden.

In IIS 7 kann dieser Fehler darauf hindeuten.

-   Diese Bits-Uploads sind im virtuellen Verzeichnis (vdir) auf dem Server nicht aktiviert.
-   Die Uploadgröße überschreitet die maximale uploadgrenze (Weitere Informationen finden Sie in der IIS-Erweiterungs Eigenschaft [**bitmaximumuploadsize**](bits-iis-extension-properties.md) ).

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG \_ E \_ http- \_ Fehler \_ 407 (0x80190197)
</dt> <dd>

Der Benutzer verfügt nicht über die Berechtigung zum Zugriff auf den Proxy. Für den Proxy ist eine Benutzerauthentifizierung erforderlich.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG \_ E \_ http- \_ Fehler \_ 414 (0x8019019E)
</dt> <dd>

Der Server kann die Übertragungs Anforderung nicht verarbeiten. Der Uniform Resource Identifier (URI) im Remote Dateinamen ist länger als der Server interpretieren kann.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG \_ E \_ http- \_ Fehler \_ 501 (0x801901f 5)
</dt> <dd>

Der Server unterstützt die erforderliche Funktionalität zum erfüllen der Anforderung nicht. In IIS 6 gibt dieser Fehler an, dass BITS-Uploads auf dem virtuellen Verzeichnis (vdir) auf dem Server nicht aktiviert sind.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG \_ E \_ http- \_ Fehler \_ 503 (0x801901f)
</dt> <dd>

Der Dienst ist vorübergehend überlastet und kann die Anforderung nicht verarbeiten. Fortsetzen des Auftrags zu einem späteren Zeitpunkt.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG \_ E \_ http- \_ Fehler \_ 504 (0x801901f)
</dt> <dd>

Timeout bei der Übertragungs Anforderung beim Warten auf ein Gateway. Fortsetzen des Auftrags zu einem späteren Zeitpunkt.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG \_ E \_ http- \_ Fehler \_ 505 (0x801901f)
</dt> <dd>

Die im Remote Dateinamen angegebene HTTP-Protokollversion wird vom Server nicht unterstützt.

</dd> </dl>

Die Header Datei "bitsmsg. h" enthält zusätzliche http-Rückgabewerte, die nicht oben aufgeführt sind und von Bits intern verwendet werden. Weitere Informationen zu diesen und anderen HTTP-Rückgabe Werten, die Sie empfangen können, finden Sie in der Spezifikation von RFC 2616 von der Internet Engineering Task Force unter [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 