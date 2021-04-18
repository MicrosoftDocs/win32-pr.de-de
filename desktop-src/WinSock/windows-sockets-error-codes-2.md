---
description: Windows Sockets (Winsock)-Fehlercodes, die von der WSAGetLastError-Funktion zurückgegeben werden.
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: Windows Sockets-Fehler Codes (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c251d63872c05623a6d1c9e3820edd2d8f670e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372676"
---
# <a name="windows-sockets-error-codes"></a>Windows Sockets-Fehler Codes

Die meisten Windows Sockets 2-Funktionen geben nicht die genaue Ursache eines Fehlers zurück, wenn die Funktion zurückgibt. Weitere Informationen finden Sie im Thema [Behandeln von Winsock-Fehlern](handling-winsock-errors.md) .

Die [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion gibt den letzten Fehler zurück, der für den aufrufenden Thread aufgetreten ist. Wenn eine bestimmte Windows Sockets-Funktion anzeigt, dass ein Fehler aufgetreten ist, sollte diese Funktion sofort aufgerufen werden, um den erweiterten Fehlercode für den fehlgeschlagenen Funktionsaufruf abzurufen. Diese Fehlercodes und eine kurze Textbeschreibung, die einem Fehlercode zugeordnet ist, werden in der Header Datei " *Winerror. h* " definiert. Die [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion kann zum Abrufen der Meldungs Zeichenfolge für den zurückgegebenen Fehler verwendet werden.

Informationen zum Behandeln von Fehlercodes beim Portieren von Socketanwendungen in Winsock finden Sie unter [Error Codes-errno, h \_ errno und WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md).

In der folgenden Liste werden die möglichen Fehlercodes beschrieben, die von der [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) -Funktion zurückgegeben werden. Fehler werden in numerischer Reihenfolge mit dem Fehler Makronamen aufgelistet. Einige Fehlercodes, die in der Header Datei " *Winsock2. h* " definiert sind, werden nicht von einer Funktion zurückgegeben.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode/-wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="WSA_INVALID_HANDLE"></span><span id="wsa_invalid_handle"></span><dl> <dt><strong>WSA_INVALID_HANDLE</strong></dt> <dt>6</dt> </dl></td>
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>Das angegebene Ereignis Objekt Handle ist ungültig.</dt> <dd> Eine Anwendung versucht, ein Ereignis Objekt zu verwenden, aber das angegebene Handle ist ungültig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>Nicht genügend Arbeitsspeicher verfügbar.</dt> <dd> Eine Anwendung hat eine Windows Sockets-Funktion verwendet, die direkt einer Windows-Funktion zugeordnet ist. Mit der Windows-Funktion werden fehlende erforderliche Speicherressourcen angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>Mindestens ein Parameter ist ungültig.</dt> <dd> Eine Anwendung hat eine Windows Sockets-Funktion verwendet, die direkt einer Windows-Funktion zugeordnet ist. Mit der Windows-Funktion wird ein Problem mit einem oder mehreren Parametern angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>Der überlappende Vorgang wurde abgebrochen.</dt> <dd> Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls "SIO_FLUSH" in <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a>abgebrochen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>Das überlappende e/a-Ereignis Objekt befindet sich nicht im signalisierten Zustand.</dt> <dd> Die Anwendung hat versucht, den Status eines überlappenden Vorgangs zu ermitteln, der noch nicht abgeschlossen ist. Anwendungen, die <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>wsagetverlappedresult</strong></a> verwenden (wobei das <em>fwait</em> -Flag auf <strong>false</strong>festgelegt ist), um zu bestimmen, wann ein überlappende Vorgang abgeschlossen wurde, erhalten Sie diesen Fehlercode, bis der Vorgang abgeschlossen ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>Überlappende Vorgänge werden zu einem späteren Zeitpunkt durchgeführt. <br/> <dl> <dt><span></span></dt> <dd> Die Anwendung hat einen überlappenden Vorgang initiiert, der nicht sofort abgeschlossen werden kann. Ein Abschluss Hinweis wird später angegeben, wenn der Vorgang abgeschlossen wurde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>Wsaabtr</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>Unterbrochener Funktionsaufrufe.</dt> <dd> Ein Blockierungs Vorgang wurde durch einen <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">wsacancelblockingstatement</a>-Aufrufvorgang unterbrochen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>Wsaebadf</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>Das Datei Handle ist ungültig.</dt> <dd> Das angegebene Datei Handle ist ungültig. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>WSAEACCES</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>Die Berechtigung wurde verweigert.</dt> <dd> Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Ein Beispiel hierfür ist die Verwendung einer Broadcast Adresse für <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> , ohne dass Broadcast Berechtigungen mithilfe von <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a>(SO_BROADCAST) festgelegt werden. <br/> Ein weiterer möglicher Grund für den WSAEACCES-Fehler besteht darin, dass beim Aufrufen der <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>Bind</strong></a> -Funktion (unter Windows NT 4,0 mit SP4 und höher) ein anderer Anwendungs-, Dienst-oder Kernelmodustreiber an dieselbe Adresse mit exklusivem Zugriff gebunden ist. Ein solcher exklusiver Zugriff ist ein neues Feature von Windows NT 4,0 mit SP4 und höher und wird mithilfe der Option <a href="/windows/desktop/winsock/so-exclusiveaddruse">SO_EXCLUSIVEADDRUSE</a> implementiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>Wsaefault</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>Ungültige Adresse.</dt> <dd> Das System hat bei dem Versuch, ein Zeigerargument eines Aufrufes zu verwenden, eine ungültige Zeiger Adresse erkannt. Dieser Fehler tritt auf, wenn eine Anwendung einen ungültigen Zeiger Wert übergibt oder wenn die Länge des Puffers zu klein ist. Wenn beispielsweise die Länge eines Arguments, das eine <a href="/windows/desktop/winsock/sockaddr-2"><strong>sockaddr</strong></a> -Struktur ist, kleiner ist als sizeof (sockaddr).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>Wsaabval</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>Ungültiges Argument.</dt> <dd> Es wurde ein ungültiges Argument angegeben (z. b. die Angabe einer ungültigen Ebene für die <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> -Funktion). In einigen Fällen bezieht sie sich auch auf den aktuellen Status des Sockets – beispielsweise das Aufrufen von <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>Accept</strong></a> für einen Socket, der nicht lauscht.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>Wsaemfile</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>Zu viele geöffnete Dateien.</dt> <dd> Zu viele geöffnete Sockets. Jede Implementierung kann über eine maximale Anzahl von Sockethandles verfügen, die entweder global, pro Prozess oder pro Thread verfügbar ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>WSAEWOULDBLOCK</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>Die Ressource ist vorübergehend nicht verfügbar.</dt> <dd> Dieser Fehler wird von Vorgängen an nicht blockierenden Sockets zurückgegeben, die nicht sofort abgeschlossen werden können, z. b. <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>empfangener</strong></a> , wenn keine Daten in die Warteschlange eingereiht werden, die vom Socket gelesen werden Dies ist ein nicht schwerwiegender Fehler, und der Vorgang sollte später wiederholt werden. Es ist normal, dass WSAEWOULDBLOCK als Ergebnis des Aufrufs von <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> auf einem nicht blockierenden SOCK_STREAM Socket gemeldet wird, da eine gewisse Zeit ververgehen muss, damit die Verbindung hergestellt werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>Wsaeingabe Progress</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>Der Vorgang wird jetzt ausgeführt.</dt> <dd> Ein Blockierungsvorgang wird momentan ausgeführt. Windows Sockets ermöglicht nur die ausstehende Ausführung eines einzelnen blockierenden Vorgangs – pro Aufgabe oder Thread –, und wenn ein anderer Funktions Aufruftyp (unabhängig davon, ob er auf diesen oder einen anderen Socket verweist) ausgeführt wird, schlägt die Funktion mit dem Fehler "WSAEINPROGRESS" fehl.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>Wsaebereits</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>Der Vorgang wird bereits ausgeführt.</dt> <dd> Es wurde versucht, einen Vorgang für einen nicht blockierenden Socket auszuführen, bei dem bereits ein Vorgang ausgeführt wird, d. –. das Aufrufen von <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> ein zweites Mal auf einem nicht blockierenden Socket, der bereits eine Verbindung herstellt, oder das Abbrechen einer asynchronen Anforderung (<strong>WSAAsyncGetXbyY</strong>), die bereits abgebrochen oder abgeschlossen wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>Wsaeinotsock</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Socketvorgang für nonsocket.</dt> <dd> Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist. Der Sockethandle-Parameter hat nicht auf einen gültigen Socket verwiesen, oder für <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>Select</strong></a>war ein Member einer <strong>fd_set</strong> ungültig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>WSAEDESTADDRREQ</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>Die Zieladresse ist erforderlich.</dt> <dd> Eine erforderliche Adresse wurde bei einem Vorgang für einen Socket ausgelassen. Dieser Fehler wird z. b. zurückgegeben, wenn <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a> mit der Remote Adresse ADDR_ANY aufgerufen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>Wsaemsgsize</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>Die Nachricht ist zu lang.</dt> <dd> Eine Nachricht, die auf einem Datagrammsocket gesendet wurde, war größer als der interne Nachrichten Puffer oder ein anderes Netzwerk Limit, oder der Puffer, der zum Empfangen eines Datagramms verwendet wurde, war kleiner als das Datagramm selbst.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>WSAEPROTOTYPE</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>Falscher Protokoll Datentyp für Socket.</dt> <dd> Im <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socket</strong></a> -Funktions Aufrufwert wurde ein Protokoll angegeben, das die Semantik des angeforderten Sockettyps nicht unterstützt. Beispielsweise kann das ARPA Internet UDP-Protokoll nicht mit einem socketyp SOCK_STREAM angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>Wsaumoproumopt</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>Ungültige Protokoll Option.</dt> <dd> Eine unbekannte, ungültige oder nicht unterstützte Option oder Ebene wurde in einem <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>getsockopt</strong></a> -oder <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> -Befehl angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>Wsaeprotonosupport</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>Das Protokoll wird nicht unterstützt.</dt> <dd> Das angeforderte Protokoll wurde nicht im System konfiguriert, oder es ist keine Implementierung vorhanden. Ein <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socketbefehl</strong></a> fordert z. b. einen SOCK_DGRAM Socket an, gibt jedoch ein streamprotokoll an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>Wsaesocktnosupport</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>Sockettyp wird nicht unterstützt.</dt> <dd> In dieser Adressfamilie ist die Unterstützung für den angegebenen Sockettyp nicht vorhanden. Beispielsweise kann der optionale Typ SOCK_RAW in einem <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socketbefehl</strong></a> ausgewählt werden, und die Implementierung unterstützt SOCK_RAW Sockets überhaupt nicht.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>WSAEOPNOTSUPP</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>Der Vorgang wird nicht unterstützt.</dt> <dd> Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt. Dies tritt normalerweise auf, wenn ein socketdeskriptor für einen Socket, der diesen Vorgang nicht unterstützt, versucht, eine Verbindung für einen Datagramm-Socket zu akzeptieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>Wsaepf NoSupport</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>Die Protokollfamilie wird nicht unterstützt.</dt> <dd> Die Protokollfamilie wurde nicht im System konfiguriert, oder es ist keine Implementierung vorhanden. Diese Meldung hat eine etwas andere Bedeutung als WSAEAFNOSUPPORT. Allerdings ist es in den meisten Fällen austauschbar, und alle Windows Sockets-Funktionen, die eine dieser Nachrichten zurückgeben, geben auch WSAEAFNOSUPPORT an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>WSAEAFNOSUPPORT</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>Die Adressfamilie wird von der Protokollfamilie nicht unterstützt.</dt> <dd> Es wurde eine Adresse verwendet, die nicht mit dem angeforderten Protokoll kompatibel ist. Alle Sockets werden mit einer zugeordneten Adressfamilie (d. h. AF_INET für Internet Protokolle) und einem generischen Protokolltyp (SOCK_STREAM) erstellt. Dieser Fehler wird zurückgegeben, wenn im <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>socketbefehl</strong></a> ein falsches Protokoll explizit angefordert wird, oder wenn eine Adresse der falschen Familie für einen Socket verwendet wird, z. b. in <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>WSAEADDRINUSE</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>Die Adresse wird bereits verwendet.</dt> <dd> In der Regel ist nur eine Verwendung der einzelnen Socketadressen (Protokoll/IP-Adresse/Port) zulässig. Dieser Fehler tritt auf, wenn eine Anwendung versucht, einen Socket an eine IP-Adresse/einen Port zu <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>binden</strong></a> , die bereits für einen vorhandenen Socket verwendet wurde, oder einen Socket, der nicht ordnungsgemäß geschlossen wurde, oder einen Socket, der noch gerade geschlossen wird. Für Server Anwendungen, die mehrere Sockets an dieselbe Portnummer <strong>binden</strong> müssen, empfiehlt sich die Verwendung von <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> (SO_REUSEADDR). Client Anwendungen müssen in der Regel keine <strong>Bindung</strong> abrufen –<a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> wählt automatisch einen nicht verwendeten Port aus. Wenn <strong>Bind</strong> mit einer Platzhalter Adresse (einschließlich ADDR_ANY) aufgerufen wird, kann ein WSAEADDRINUSE-Fehler so lange verzögert werden, bis für die jeweilige Adresse ein Commit ausgeführt wird. Dies kann zu einem späteren Zeitpunkt mit einem Rückruf einer anderen Funktion auftreten, einschließlich <strong>Connect</strong>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>lauschen</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>wsaconnetct</strong></a>oder <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>wsajoinleaf</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>Wsaeaddrnotavail</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>Angeforderte Adresse kann nicht zugewiesen werden.</dt> <dd> Die angeforderte Adresse ist im Kontext nicht gültig. Dies führt normalerweise zu einem Versuch, eine <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>Bindung</strong></a> an eine Adresse herzustellen, die für den lokalen Computer nicht gültig ist. Dies kann auch aus <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a>, <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>wsaconnetct</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>wsajoinleaf</strong></a>oder <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>WSASendTo</strong></a> resultieren, wenn die Remote Adresse oder der Port für einen Remote Computer ungültig ist (z. b. Adresse oder Port 0).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>Wsaaufetdown</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>Netzwerk ist nicht im Netzwerk.</dt> <dd> Bei einem Socketvorgang war das Netzwerk inaktiv. Dies kann auf einen schwerwiegenden Fehler des Netzwerksystems (d. h., des Protokollstapels, den die Windows Sockets-DLL durchläuft), der Netzwerkschnittstelle oder des lokalen Netzwerks selbst hinweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>Wsaumetunreach</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>Das Netzwerk ist nicht erreichbar.</dt> <dd> Es wurde versucht, ein Socketvorgang in ein nicht erreichbares Netzwerk auszuführen. Dies bedeutet in der Regel, dass die lokale Software keine Route zum Erreichen des Remote Hosts kennt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>Wsaenetreset</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>Beim Zurücksetzen wurde eine Netzwerkverbindung getrennt.</dt> <dd> Die Verbindung wurde unterbrochen, weil eine Keep-Alive-Aktivität einen Fehler erkannt hat, während der Vorgang ausgeführt wurde. Sie kann auch von <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> zurückgegeben werden, wenn versucht wird, <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> für eine Verbindung festzulegen, bei der bereits ein Fehler aufgetreten ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>WSAECONNABORTED</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>Software hat Verbindungsabbruch verursacht.</dt> <dd> Eine etablierte Verbindung wurde von der Software auf Ihrem Host Computer abgebrochen, möglicherweise aufgrund eines Timeout-oder Protokoll Fehlers der Datenübertragung.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>WSAECONNRESET</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>Die Verbindung wurde vom Peer zurückgesetzt.</dt> <dd> An existing connection was forcibly closed by the remote host. Dies führt normalerweise dazu, dass die Peer Anwendung auf dem Remote Host plötzlich beendet wird, der Host neu gestartet wird, die Host-oder Remote Netzwerkschnittstelle deaktiviert ist oder der Remote Host eine feste Schließung verwendet (Weitere Informationen zur SO_LINGER Option für den Remotesocket finden Sie unter <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> ). Dieser Fehler kann auch auftreten, wenn eine Verbindung unterbrochen wurde, weil eine Keep-Alive-Aktivität einen Fehler erkannt hat, während mindestens ein Vorgang ausgeführt wird. Ausgeführte Vorgänge schlagen mit wsaenetreset fehl. Nachfolgende Vorgänge schlagen mit WSAECONNRESET fehl.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>WSAENOBUFS</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>Es ist kein Pufferspeicher verfügbar.</dt> <dd> Ein Vorgang für einen Socket konnte nicht durchgeführt werden, da das System nicht genügend Pufferspeicher hatte oder weil eine Warteschlange voll war.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>Wsaeisconn</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>Der Socket ist bereits verbunden.</dt> <dd> Eine Verbindungsanforderung wurde an einem bereits verbundenen Socket vorgenommen. Einige Implementierungen geben diesen Fehler auch dann zurück <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>, wenn SendTo</strong></a> für einen verbundenen SOCK_DGRAM Socket aufgerufen wird (bei SOCK_STREAM Sockets wird der <em>to</em> -Parameter in <strong>SendTo</strong> ignoriert), obwohl andere Implementierungen dies als ein rechtliches vorkommen behandeln.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>Wsaumotconn</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>Der Socket ist nicht verbunden.</dt> <dd> Eine Anforderung zum Senden oder empfangen von Daten wurde nicht zugelassen, da der Socket nicht verbunden ist und (beim Senden eines Datagramm-Sockets mit <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>SendTo</strong></a>) keine Adresse angegeben wurde. Dieser Fehler kann auch von einem anderen Vorgangstyp zurückgegeben werden – z. b. <a href="/windows/desktop/winsock/so-keepalive"><strong>SO_KEEPALIVE</strong></a> <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> -Einstellung, wenn die Verbindung zurückgesetzt wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>WSAESHUTDOWN</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>Nach dem Beenden des Sockets kann nicht gesendet werden.</dt> <dd> Eine Anforderung zum Senden oder empfangen von Daten wurde nicht zugelassen, da der Socket in dieser Richtung bereits mit einem vorherigen <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>Shutdown</strong></a> -Befehl heruntergefahren wurde. Durch den Aufruf von <strong>Shutdown</strong> wird eine teilweise Schließung eines Sockets angefordert, bei der es sich um ein Signal handelt, dass das Senden oder empfangen oder beides eingestellt wurde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>Wsaetoomanyrefs</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>Zu viele Verweise.</dt> <dd> Zu viele Verweise auf ein Kernel Objekt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>WSAETIMEDOUT</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>Verbindungs Timeout.</dt> <dd> Ein Verbindungsversuch ist fehlgeschlagen, weil die verbundene Partei nach einem bestimmten Zeitraum nicht ordnungsgemäß reagiert hat, oder die festgelegte Verbindung konnte nicht hergestellt werden, da der verbundene Host nicht reagiert hat.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>Wsaeconnabgelehnte</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>Die Verbindung wurde verweigert.</dt> <dd> Es konnte keine Verbindung hergestellt werden, da diese vom Zielcomputer aktiv verweigert wurde. Dies führt normalerweise zu einem Versuch, eine Verbindung mit einem Dienst herzustellen, der auf dem fremden Host inaktiv ist, d. –. einer, auf dem keine Serveranwendung ausgeführt wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>Wsaeloop</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>Der Name kann nicht übersetzt werden.</dt> <dd> Ein Name kann nicht übersetzt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>Wsaenametoolong</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>Der Name ist zu lang.</dt> <dd> Eine namens Komponente oder ein Name war zu lang.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>Wsaehostdown</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>Der Host ist nicht herunter.</dt> <dd> Ein Socketvorgang ist fehlgeschlagen, da der Zielhost ausgefallen ist. Bei einem Socketvorgang ist ein toter Host aufgetreten. Die Netzwerkaktivität auf dem lokalen Host wurde nicht initiiert. Diese Bedingungen werden wahrscheinlich durch den Fehler "WSAETIMEDOUT" angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>Wsaehostunreach</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>Keine Route zum Host.</dt> <dd> Versuch eines Socketvorgangs für einen nicht erreichbaren Host. Weitere Informationen finden Sie unter wsaumetunreach.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>Wsaenotempty</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>Das Verzeichnis ist nicht leer.</dt> <dd> Ein nicht leeres Verzeichnis kann nicht entfernt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>Wsaeproclim</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>Zu viele Prozesse.</dt> <dd> Eine Windows Sockets-Implementierung kann eine Beschränkung für die Anzahl der Anwendungen aufweisen, die Sie gleichzeitig verwenden können. <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> schlägt möglicherweise mit diesem Fehler fehl, wenn der Grenzwert erreicht wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>Wsaeusers</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>Das Benutzer Kontingent wurde überschritten.</dt> <dd> Das Benutzer Kontingent ist abgelaufen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>Wsaedquot</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>Datenträger Kontingent überschritten.</dt> <dd> Nicht genügend Datenträger Kontingent. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>Wsaestale</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>Veralteter Datei Handle-Verweis.</dt> <dd> Der Datei Handle-Verweis ist nicht mehr verfügbar. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>Wsaeremote</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>Das Element ist Remote.</dt> <dd> Das Element ist nicht lokal verfügbar. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>Wsasysnotready</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>Netzwerk Subsystem ist nicht verfügbar.</dt> <dd> Dieser Fehler wird von <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> zurückgegeben, wenn die Windows Sockets-Implementierung zurzeit nicht funktionsfähig ist, da das zugrunde liegende System, das zur Bereitstellung von Netzwerkdiensten verwendet wird, derzeit nicht verfügbar ist Benutzer sollten Folgendes überprüfen:<br/> </dd> </dl>
<ul>
<li>Die entsprechende Windows Sockets-DLL-Datei befindet sich im aktuellen Pfad.</li>
<li>Sie versuchen nicht, mehr als eine Windows Sockets-Implementierung gleichzeitig zu verwenden. Wenn auf Ihrem System mehr als eine Winsock-DLL vorhanden ist, stellen Sie sicher, dass die erste im Pfad für das derzeit geladene Netzwerk Subsystem geeignet ist.</li>
<li>In der Dokumentation zur Windows Sockets-Implementierung wird sichergestellt, dass alle erforderlichen Komponenten zurzeit installiert und ordnungsgemäß konfiguriert sind.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>Wsavernotsupported</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span>Winsock.dll Version außerhalb des gültigen Bereichs.</dt> <dd> Die aktuelle Windows Sockets-Implementierung unterstützt nicht die von der Anwendung angeforderte Windows Sockets-Spezifikations Version. Vergewissern Sie sich, dass auf keine veralteten Windows Sockets-DLL-Dateien zugegriffen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>Wsanotinitialisierte</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>Der WSAStartup-Vorgang wurde noch nicht ausgeführt.</dt> <dd> Die Anwendung hat nicht <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> oder <strong>WSAStartup</strong> als fehlerhaft bezeichnet. Die Anwendung greift möglicherweise auf einen Socket zu, der von der aktuellen aktiven Aufgabe nicht übernommen wird (d. h. es wird versucht, einen Socket zwischen Tasks freizugeben), oder <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>WSACleanup</strong></a> wurde zu oft aufgerufen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>Wsaediscon</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>Ordnungsgemäßes Herunterfahren wird ausgeführt.</dt> <dd> Wird von <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>WSARecv</strong></a> und <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>WSARecvFrom</strong></a> zurückgegeben, um anzugeben, dass die Remote Partei eine ordnungsgemäße Herunterfahr Sequenz initiiert hat.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>Wsaeromore</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Keine weiteren Ergebnisse.</dt> <dd> Von der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> -Funktion können keine weiteren Ergebnisse zurückgegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>Wsaecancelled</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>Der-Rückruf wurde abgebrochen.</dt> <dd> Es wurde ein Aufrufen der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> -Funktion durchgeführt, während dieser Rückruf noch verarbeitet wurde. Der-Rückruf wurde abgebrochen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>Wsaeinvalidproctable</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>Die Prozedur aufruftabelle ist ungültig.</dt> <dd> Die aufruftabelle der Dienstanbieter Prozedur ist ungültig. Ein Dienstanbieter hat eine falsche Prozedur Tabelle zum Ws2_32.dll zurückgegeben. Dies wird normalerweise dadurch verursacht, dass mindestens ein Funktionszeiger <strong>null</strong>ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>Wsaeinvalidprovider</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>Der Dienstanbieter ist ungültig.</dt> <dd> Der angeforderte Dienstanbieter ist ungültig. Dieser Fehler wird von den <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>wscgetproviderinfo</strong></a> -und <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> -Funktionen zurückgegeben, wenn der angegebene Protokolleintrag nicht gefunden wurde. Dieser Fehler wird auch zurückgegeben, wenn der Dienstanbieter eine andere Versionsnummer als 2,0 zurückgegeben hat.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>Wsaeproviderfailedinit</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>Der Dienstanbieter konnte nicht initialisiert werden.</dt> <dd> Der angeforderte Dienstanbieter konnte nicht geladen oder initialisiert werden. Dieser Fehler wird zurückgegeben, wenn die dll eines Dienstanbieters nicht geladen werden konnte (Fehler bei<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>LoadLibrary</strong></a> ) oder die <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>WSPStartup</strong></a> -oder <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>NSPStartup</strong></a> -Funktion des Anbieters fehlgeschlagen ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>WSASYSCALLFAILURE</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>Fehler beim System Rückruf.</dt> <dd> Ein System-Befehl, der nie einen Fehler verursacht, ist fehlgeschlagen. Dies ist ein generischer Fehlercode, der unter verschiedenen Bedingungen zurückgegeben wird. <br/> Wird zurückgegeben, wenn ein Systemaufrufe, der niemals fehlschlagen soll, fehlschlägt. Wenn z. b. ein Rückruf von <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>waitformultipleevents</strong></a> fehlschlägt oder eine der Registrierungsfunktionen nicht versucht, die Protokoll-/Namespace Kataloge zu manipulieren.<br/> Wird zurückgegeben, wenn ein Anbieter keinen Erfolg zurückgibt und keinen erweiterten Fehlercode bereitstellt. Kann einen Fehler bei der Implementierung eines Dienstanbieters angeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>Der Dienst wurde nicht gefunden.</dt> <dd> Dieser Dienst ist nicht bekannt. Der Dienst wurde im angegebenen Namespace nicht gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>Der Klassentyp wurde nicht gefunden.</dt> <dd> Die angegebene Klasse wurde nicht gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Keine weiteren Ergebnisse.</dt> <dd> Von der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> -Funktion können keine weiteren Ergebnisse zurückgegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>Der-Rückruf wurde abgebrochen.</dt> <dd> Es wurde ein Aufrufen der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd</strong></a> -Funktion durchgeführt, während dieser Rückruf noch verarbeitet wurde. Der-Rückruf wurde abgebrochen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>Wsaerefused</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>Die Datenbankabfrage wurde abgelehnt.</dt> <dd> Eine Datenbankabfrage ist fehlgeschlagen, da Sie aktiv abgelehnt wurde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>Der Host wurde nicht gefunden.</dt> <dd> Ein solcher Host ist nicht bekannt. Der Name ist kein offizieller Hostname oder Alias, oder er kann nicht in den abgefragten Datenbanken gefunden werden. Dieser Fehler kann auch bei Protokoll-und Dienst Abfragen zurückgegeben werden und bedeutet, dass der angegebene Name in der relevanten Datenbank nicht gefunden wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>Nicht autorisierender Host nicht gefunden.</dt> <dd> Dies ist normalerweise ein temporärer Fehler bei der Host Namensauflösung und bedeutet, dass der lokale Server keine Antwort von einem autorisierenden Server empfangen hat. Ein erneuter Versuch zu einem späteren Zeitpunkt wird möglicherweise erfolgreich durchgeführt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>Dies ist ein nicht BEHEB barer Fehler.</dt> <dd> Dies weist darauf hin, dass während einer Datenbanksuche ein nicht BEHEB barer Fehler aufgetreten ist. Dies liegt möglicherweise daran, dass die Datenbankdateien (z. b. BSD-kompatible Hosts, Dienste oder Protokolldateien) nicht gefunden wurden oder eine DNS-Anforderung mit einem schweren Fehler vom Server zurückgegeben wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>Gültiger Name, kein Datensatz des angeforderten Typs.</dt> <dd> Der angeforderte Name ist gültig und wurde in der Datenbank gefunden, aber er verfügt nicht über die richtigen zugeordneten Daten, für die er aufgelöst wurde. Das übliche Beispiel hierfür ist ein Hostname-zu-Adresse-Übersetzungs Versuch (mit <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> oder <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>wsaasyncgethostbyname</strong></a>), der das DNS (Domain Name Server) verwendet. Ein MX-Datensatz wird zurückgegeben, aber kein Datensatz – gibt an, dass der Host selbst vorhanden ist, aber nicht direkt erreichbar ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>QoS-Empfänger.</dt> <dd> Mindestens eine QoS-Reserve ist eingetroffen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>QoS-Absender.</dt> <dd> Mindestens ein QoS-sendepfad ist eingetroffen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>Keine QoS-Absender.</dt> <dd> Es sind keine QoS-Sender vorhanden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>QoS keine Empfänger.</dt> <dd> Es sind keine QoS-Empfänger vorhanden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>Die QoS-Anforderung wurde bestätigt.</dt> <dd> Die QoS-Reserve Anforderung wurde bestätigt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>QoS-Eintritts Fehler.</dt> <dd> QoS-Fehler aufgrund fehlender Ressourcen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>QoS-Richtlinien Fehler.</dt> <dd> Die QoS-Anforderung wurde zurückgewiesen, weil das Richtlinien System die angeforderte Ressource nicht innerhalb der vorhandenen Richtlinie zuordnen konnte. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>Ungültiger QoS-Stil.</dt> <dd> Ein unbekannter oder in Konflikt stehender QoS-Stil wurde gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>Ungültiges QoS-Objekt.</dt> <dd> Es wurde ein Problem mit einem Teil der FILTERSPEC oder dem anbieterspezifischen Puffer im allgemeinen aufgetreten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>QoS-Datenverkehrs Steuerungs Fehler.</dt> <dd> Ein Fehler mit der zugrunde liegenden Datenverkehrs Steuerungs-API (TC), da die generische QoS-Anforderung für die lokale Durchsetzung durch die TC-API konvertiert wurde. Dies kann auf einen Fehler aufgrund von ungenügenden Arbeitsspeicher oder auf einen internen QoS-Anbieter Fehler zurückzuführen sein. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>Allgemeiner QOS-Fehler.</dt> <dd> Ein allgemeiner QoS-Fehler.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>Fehler beim QoS-Diensttyp.</dt> <dd> In der QoS-Flowspec wurde ein ungültiger oder unbekannter Diensttyp gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>QoS-Flowspec-Fehler.</dt> <dd> In der <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>QoS</strong></a> -Struktur wurde eine ungültige oder inkonsistente Flowspec gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>Ungültiger QoS-Anbieter Puffer.</dt> <dd> Ein ungültiger QoS-Anbieter spezifischer Puffer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>Ungültiger QoS-Filter Stil.</dt> <dd> Es wurde ein ungültiger QoS-Filter Stil verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>Ungültiger QoS-Filtertyp.</dt> <dd> Es wurde ein ungültiger QoS-Filtertyp verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>Falsche Anzahl von QoS-filtern.</dt> <dd> Im FLOWDESCRIPTOR wurde eine falsche Anzahl von QoS-FILTERSPECs angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>Ungültige QoS-Objekt Länge.</dt> <dd> Im anbieterspezifischen QoS-Puffer wurde ein Objekt mit einem ungültigen objectlength-Feld angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>Falsche Anzahl von QoS-Flows.</dt> <dd> In der QoS-Struktur wurde eine falsche Anzahl von Fluss Deskriptoren angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>Unbekanntes QoS-Objekt.</dt> <dd> Ein unbekanntes Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>Ungültiges QoS-Richtlinien Objekt.</dt> <dd> Ein ungültiges Richtlinien Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>Ungültiger QoS-Fluss Deskriptor.</dt> <dd> In der Liste der flowdeskriptoren wurde ein ungültiger QoS-Datenfluss Deskriptor gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>Ungültige Fluss Spezifikation für QoS-Anbieter.</dt> <dd> Im anbieterspezifischen QoS-Puffer wurde eine ungültige oder inkonsistente Flowspec gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>Ungültige QoS-anbieterspezifische FILTERSPEC.</dt> <dd> Im QoS-anbieterspezifischen Puffer wurde eine ungültige FILTERSPEC gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>Ungültiges Objekt der QoS-Form Verwerfungs Modus.</dt> <dd> Ein ungültiges Shape-Verwerfungs Modus-Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>Ungültiges QoS-Strukturierungs Raten-Objekt.</dt> <dd> Ein ungültiges Strukturierungs Raten Objekt wurde im QoS-anbieterspezifischen Puffer gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>Der QoS-Elementtyp der reservierten Richtlinie.</dt> <dd> Ein reserviertes Policy-Element wurde im QoS-anbieterspezifischen Puffer gefunden.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winsock2. h; </dt> <dt>Winerror. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler Codes: errno, h \_ errno und WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[**Format Message**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
