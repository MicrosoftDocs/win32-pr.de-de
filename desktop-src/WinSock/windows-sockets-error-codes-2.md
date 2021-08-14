---
description: Windows Sockets -Fehlercodes (Winsock), die von der WSAGetLastError-Funktion zurückgegeben werden.
ms.assetid: 50b924f3-2c88-443b-8a90-4293fe5c3048
title: Windows Sockets-Fehlercodes (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece53093e7aca31d9d883680005f92ca8b30a76120209affb4dba42d6826d0bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322003"
---
# <a name="windows-sockets-error-codes"></a>Windows Sockets-Fehlercodes

Die meisten Windows Sockets 2-Funktionen geben nicht die spezifische Ursache eines Fehlers zurück, wenn die Funktion zurückgegeben wird. Weitere Informationen finden Sie im Thema [Behandeln von Winsockfehlern.](handling-winsock-errors.md)

Die [**WSAGetLastError-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt den letzten Fehler zurück, der für den aufrufenden Thread aufgetreten ist. Wenn eine bestimmte Windows Sockets-Funktion angibt, dass ein Fehler aufgetreten ist, sollte diese Funktion sofort aufgerufen werden, um den erweiterten Fehlercode für den fehlerhaften Funktionsaufruf abzurufen. Diese Fehlercodes und eine kurze Textbeschreibung, die einem Fehlercode zugeordnet ist, werden in der *Headerdatei Winerror.h* definiert. Die [**FormatMessage-Funktion**](/windows/win32/api/winbase/nf-winbase-formatmessage) kann verwendet werden, um die Meldungszeichenfolge für den zurückgegebenen Fehler abzurufen.

Informationen zum Behandeln von Fehlercodes beim Portieren von Socketanwendungen zu Winsock finden Sie unter [Fehlercodes – errno, h \_ errno und WSAGetLastError.](error-codes-errno-h-errno-and-wsagetlasterror-2.md)

In der folgenden Liste werden die möglichen Fehlercodes beschrieben, die von der [**WSAGetLastError-Funktion**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) zurückgegeben werden. Fehler werden in numerischer Reihenfolge mit dem Namen des Fehlermakros aufgelistet. Einige fehlercodes, die in der *Headerdatei "Winsock2.h"* definiert sind, werden von keiner Funktion zurückgegeben.

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
<td><dl> <dt><span id="Specified_event_object_handle_is_invalid."></span><span id="specified_event_object_handle_is_invalid."></span><span id="SPECIFIED_EVENT_OBJECT_HANDLE_IS_INVALID."></span>Das angegebene Ereignisobjekthandle ist ungültig.</dt> <dd> Eine Anwendung versucht, ein Ereignisobjekt zu verwenden, aber das angegebene Handle ist ungültig.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span><dl> <dt><strong>WSA_NOT_ENOUGH_MEMORY</strong></dt> <dt>8</dt> </dl></td>
<td><dl> <dt><span id="Insufficient_memory_available."></span><span id="insufficient_memory_available."></span><span id="INSUFFICIENT_MEMORY_AVAILABLE."></span>Nicht genügend Arbeitsspeicher verfügbar.</dt> <dd> Eine Anwendung hat eine Windows Sockets-Funktion verwendet, die direkt einer Windows Funktion zugeordnet ist. Die Windows-Funktion gibt an, dass nicht genügend Arbeitsspeicherressourcen erforderlich sind.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_INVALID_PARAMETER"></span><span id="wsa_invalid_parameter"></span><dl> <dt><strong>WSA_INVALID_PARAMETER</strong></dt> <dt>87</dt> </dl></td>
<td><dl> <dt><span id="One_or_more_parameters_are_invalid."></span><span id="one_or_more_parameters_are_invalid."></span><span id="ONE_OR_MORE_PARAMETERS_ARE_INVALID."></span>Mindestens ein Parameter ist ungültig.</dt> <dd> Eine Anwendung hat eine Windows Sockets-Funktion verwendet, die direkt einer Windows Funktion zugeordnet ist. Die Windows-Funktion gibt ein Problem mit einem oder mehreren Parametern an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span><dl> <dt><strong>WSA_OPERATION_ABORTED</strong></dt> <dt>995</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_operation_aborted."></span><span id="overlapped_operation_aborted."></span><span id="OVERLAPPED_OPERATION_ABORTED."></span>Überlappender Vorgang abgebrochen.</dt> <dd> Ein überlappender Vorgang wurde aufgrund des Schließens des Sockets oder der Ausführung des SIO_FLUSH Befehls in <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a>abgebrochen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_IO_INCOMPLETE"></span><span id="wsa_io_incomplete"></span><dl> <dt><strong>WSA_IO_INCOMPLETE</strong></dt> <dt>996</dt> </dl></td>
<td><dl> <dt><span id="Overlapped_I_O_event_object_not_in_signaled_state."></span><span id="overlapped_i_o_event_object_not_in_signaled_state."></span><span id="OVERLAPPED_I_O_EVENT_OBJECT_NOT_IN_SIGNALED_STATE."></span>Überlappende E/A-Ereignisobjekte befinden sich nicht im signalisierten Zustand.</dt> <dd> Die Anwendung hat versucht, den Status eines überlappenden Vorgangs zu bestimmen, der noch nicht abgeschlossen ist. Anwendungen, die <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult"><strong>WSAGetOverlappedResult</strong></a> verwenden (wobei das <em>fWait-Flag</em> auf <strong>FALSE</strong>festgelegt ist) in einem Abrufmodus, um zu bestimmen, wann ein überlappender Vorgang abgeschlossen ist, erhalten diesen Fehlercode, bis der Vorgang abgeschlossen ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_IO_PENDING"></span><span id="wsa_io_pending"></span><dl> <dt><strong>WSA_IO_PENDING</strong></dt> <dt>997</dt> </dl></td>
<td>Überlappende Vorgänge werden später abgeschlossen. <br/> <dl> <dt><span></span></dt> <dd> Die Anwendung hat einen überlappenden Vorgang initiiert, der nicht sofort abgeschlossen werden kann. Eine Abschlussanzeige wird später angegeben, wenn der Vorgang abgeschlossen wurde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINTR"></span><span id="wsaeintr"></span><dl> <dt><strong>WSAEINTR</strong></dt> <dt>10004</dt> </dl></td>
<td><dl> <dt><span id="Interrupted_function_call."></span><span id="interrupted_function_call."></span><span id="INTERRUPTED_FUNCTION_CALL."></span>Unterbrochener Funktionsaufruf.</dt> <dd> Ein Blockierungsvorgang wurde durch einen Aufruf von <a href="/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall">WSACancelBlockingCall</a>unterbrochen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEBADF"></span><span id="wsaebadf"></span><dl> <dt><strong>WSAEBADF</strong></dt> <dt>10009</dt> </dl></td>
<td><dl> <dt><span id="File_handle_is_not_valid."></span><span id="file_handle_is_not_valid."></span><span id="FILE_HANDLE_IS_NOT_VALID."></span>Das Dateihandle ist ungültig.</dt> <dd> Das angegebene Dateihandle ist ungültig. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEACCES"></span><span id="wsaeacces"></span><dl> <dt><strong>WSAEACCES</strong></dt> <dt>10013</dt> </dl></td>
<td><dl> <dt><span id="Permission_denied."></span><span id="permission_denied."></span><span id="PERMISSION_DENIED."></span>Berechtigung verweigert.</dt> <dd> Es wurde versucht, auf eine Weise auf einen Socket zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist. Ein Beispiel ist die Verwendung einer Broadcastadresse für <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto,</strong></a> ohne dass die Broadcastberechtigung mithilfe von <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a>(SO_BROADCAST) festgelegt wird. <br/> Ein weiterer möglicher Grund für den WSAEACCES-Fehler ist, dass beim Aufruf der <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>Bindungsfunktion</strong></a> (auf Windows NT 4.0 mit SP4 und höher) eine andere Anwendung, ein Anderer Dienst oder ein Kernelmodustreiber an dieselbe Adresse mit exklusivem Zugriff gebunden ist. Dieser exklusive Zugriff ist ein neues Feature von Windows NT 4.0 mit SP4 und höher und wird mithilfe der <a href="/windows/desktop/winsock/so-exclusiveaddruse">option SO_EXCLUSIVEADDRUSE</a> implementiert.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEFAULT"></span><span id="wsaefault"></span><dl> <dt><strong>WSAEFAULT</strong></dt> <dt>10014</dt> </dl></td>
<td><dl> <dt><span id="Bad_address."></span><span id="bad_address."></span><span id="BAD_ADDRESS."></span>Ungültige Adresse.</dt> <dd> Das System hat beim Versuch, ein Zeigerargument eines Aufrufs zu verwenden, eine ungültige Zeigeradresse erkannt. Dieser Fehler tritt auf, wenn eine Anwendung einen ungültigen Zeigerwert übergibt oder wenn die Länge des Puffers zu klein ist. Beispiel: Die Länge eines Arguments, bei dem es sich um eine <a href="/windows/desktop/winsock/sockaddr-2"><strong>Sockaddr-Struktur</strong></a> handelt, ist kleiner als die Sizeof(sockaddr).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVAL"></span><span id="wsaeinval"></span><dl> <dt><strong>WSAEINVAL</strong></dt> <dt>10022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_argument."></span><span id="invalid_argument."></span><span id="INVALID_ARGUMENT."></span>Ungültiges Argument.</dt> <dd> Es wurde ein ungültiges Argument angegeben (z. B. das Angeben einer ungültigen Ebene für die <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt-Funktion).</strong></a> In einigen Fällen bezieht sie sich auch auf den aktuellen Zustand des Sockets, z. B. das Aufrufen von <a href="/windows/desktop/api/Winsock2/nf-winsock2-accept"><strong>accept</strong></a> für einen Socket, der nicht lauscht.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMFILE"></span><span id="wsaemfile"></span><dl> <dt><strong>WSAEMFILE</strong></dt> <dt>10024</dt> </dl></td>
<td><dl> <dt><span id="Too_many_open_files."></span><span id="too_many_open_files."></span><span id="TOO_MANY_OPEN_FILES."></span>Zu viele geöffnete Dateien.</dt> <dd> Zu viele geöffnete Sockets. Jede Implementierung kann über eine maximale Anzahl von Sockethandles verfügen, entweder global, pro Prozess oder pro Thread.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span><dl> <dt><strong>WSAEWULEDBLOCK</strong></dt> <dt>10035</dt> </dl></td>
<td><dl> <dt><span id="Resource_temporarily_unavailable."></span><span id="resource_temporarily_unavailable."></span><span id="RESOURCE_TEMPORARILY_UNAVAILABLE."></span>Ressource vorübergehend nicht verfügbar.</dt> <dd> Dieser Fehler wird von Vorgängen für Nichtblockierungssockets zurückgegeben, die nicht sofort abgeschlossen werden können, z. <a href="/windows/desktop/api/winsock/nf-winsock-recv"><strong>B. recv,</strong></a> wenn keine Daten in die Warteschlange eingereiht werden, um aus dem Socket gelesen zu werden. Dies ist ein nicht schwerwiegender Fehler, und der Vorgang sollte später wiederholt werden. Es ist normal, dass WSAEWULEDBLOCK als <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong></strong></a> Ergebnis des Verbindungsaufrufs für einen nicht blockierenden SOCK_STREAM Socket gemeldet wird, da einige Zeit verstreichen muss, bis die Verbindung hergestellt werden kann.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span><dl> <dt><strong>WSAEINPROGRESS</strong></dt> <dt>10036</dt> </dl></td>
<td><dl> <dt><span id="Operation_now_in_progress."></span><span id="operation_now_in_progress."></span><span id="OPERATION_NOW_IN_PROGRESS."></span>Der Vorgang wird jetzt ausgeführt.</dt> <dd> Ein Blockierungsvorgang wird momentan ausgeführt. Windows Sockets lassen nur zu, dass ein einzelner Blockierendvorgang –pro Aufgabe oder Thread – ausstehend ist, und wenn ein anderer Funktionsaufruf erfolgt (unabhängig davon, ob er auf diesen oder einen anderen Socket verweist), schlägt die Funktion mit dem WSAEINPROGRESS-Fehler fehl.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEALREADY"></span><span id="wsaealready"></span><dl> <dt><strong>WSAEALREADY</strong></dt> <dt>10037</dt> </dl></td>
<td><dl> <dt><span id="Operation_already_in_progress."></span><span id="operation_already_in_progress."></span><span id="OPERATION_ALREADY_IN_PROGRESS."></span>Der Vorgang wird bereits ausgeführt.</dt> <dd> Es wurde versucht, einen Vorgang für einen Nichtblockierungssocket mit einem bereits ausgeführten Vorgang durchzuführen, d. h., es wurde ein zweites Mal eine <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Verbindung für</strong></a> einen Socket ohne Blockierung hergestellt, der bereits eine Verbindung herstellt, oder eine asynchrone Anforderung<strong>(WSAAsyncGetXbyY)</strong>abgebrochen, die bereits abgebrochen oder abgeschlossen wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span><dl> <dt><strong>WSAENOTSOCK</strong></dt> <dt>10038</dt> </dl></td>
<td><dl> <dt><span id="Socket_operation_on_nonsocket."></span><span id="socket_operation_on_nonsocket."></span><span id="SOCKET_OPERATION_ON_NONSOCKET."></span>Socketvorgang für Nicht-Ocket.</dt> <dd> Es wurde versucht, einen Vorgang für etwas zu unternehmen, das kein Socket ist. Entweder hat der Sockethandleparameter nicht auf einen gültigen Socket verwiesen, oder für <a href="/windows/desktop/api/Winsock2/nf-winsock2-select"><strong>select</strong></a>war ein Member eines <strong>fd_set</strong> ungültig.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span><dl> <dt><strong>WSAEDESTADDRREQ</strong></dt> <dt>10039</dt> </dl></td>
<td><dl> <dt><span id="Destination_address_required."></span><span id="destination_address_required."></span><span id="DESTINATION_ADDRESS_REQUIRED."></span>Zieladresse erforderlich.</dt> <dd> Eine erforderliche Adresse wurde bei einem Vorgang für einen Socket ausgelassen. Dieser Fehler wird beispielsweise zurückgegeben, wenn <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> mit der Remoteadresse von ADDR_ANY aufgerufen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span><dl> <dt><strong>WSAEMSGSIZE</strong></dt> <dt>10040</dt> </dl></td>
<td><dl> <dt><span id="Message_too_long."></span><span id="message_too_long."></span><span id="MESSAGE_TOO_LONG."></span>Nachricht zu lang.</dt> <dd> Eine nachricht, die an einen Datagrammsocket gesendet wurde, war größer als der interne Nachrichtenpuffer oder ein anderer Netzwerkgrenzwert, oder der Puffer, der zum Empfangen eines Datagramms verwendet wurde, war kleiner als das Datagramm selbst.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span><dl> <dt><strong>WSAEPROTOTYPE</strong></dt> <dt>10041</dt> </dl></td>
<td><dl> <dt><span id="Protocol_wrong_type_for_socket."></span><span id="protocol_wrong_type_for_socket."></span><span id="PROTOCOL_WRONG_TYPE_FOR_SOCKET."></span>Protokoll falscher Typ für Socket.</dt> <dd> Im Socketfunktionsaufruf <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong></strong></a> wurde ein Protokoll angegeben, das die Semantik des angeforderten Sockettyps nicht unterstützt. Beispielsweise kann das ARPA-Internet-UDP-Protokoll nicht mit dem Sockettyp SOCK_STREAM angegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span><dl> <dt><strong>WSAENOPROTOOPT</strong></dt> <dt>10042</dt> </dl></td>
<td><dl> <dt><span id="Bad_protocol_option."></span><span id="bad_protocol_option."></span><span id="BAD_PROTOCOL_OPTION."></span>Ungültige Protokolloption.</dt> <dd> Eine unbekannte, ungültige oder nicht unterstützte Option oder Ebene wurde in einem <a href="/windows/desktop/api/winsock/nf-winsock-getsockopt"><strong>getsockopt-</strong></a> oder <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt-Aufruf</strong></a> angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span><dl> <dt><strong>WSAEPROTONOSUPPORT</strong></dt> <dt>10043</dt> </dl></td>
<td><dl> <dt><span id="Protocol_not_supported."></span><span id="protocol_not_supported."></span><span id="PROTOCOL_NOT_SUPPORTED."></span>Protokoll wird nicht unterstützt.</dt> <dd> Das angeforderte Protokoll wurde nicht im System konfiguriert, oder es ist keine Implementierung dafür vorhanden. Beispielsweise fordert ein <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socketaufruf</strong></a> einen SOCK_DGRAM Socket an, gibt aber ein Streamprotokoll an.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span><dl> <dt><strong>WSAESOCKTNOSUPPORT</strong></dt> <dt>10044</dt> </dl></td>
<td><dl> <dt><span id="Socket_type_not_supported."></span><span id="socket_type_not_supported."></span><span id="SOCKET_TYPE_NOT_SUPPORTED."></span>Sockettyp wird nicht unterstützt.</dt> <dd> In dieser Adressfamilie ist die Unterstützung für den angegebenen Sockettyp nicht vorhanden. Beispielsweise kann der optionale Typ SOCK_RAW in einem <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong>Socketaufruf</strong></a> ausgewählt werden, und die Implementierung unterstützt SOCK_RAW Sockets überhaupt nicht.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span><dl> <dt><strong>WSAEOPNOTSUPP</strong></dt> <dt>10045</dt> </dl></td>
<td><dl> <dt><span id="Operation_not_supported."></span><span id="operation_not_supported."></span><span id="OPERATION_NOT_SUPPORTED."></span>Vorgang wird nicht unterstützt.</dt> <dd> Der versuchte Vorgang wird für den Objekttyp, auf den verwiesen wird, nicht unterstützt. Dies tritt normalerweise auf, wenn ein Socketdeskriptor für einen Socket, der diesen Vorgang nicht unterstützen kann, versucht, eine Verbindung für einen Datagrammsocket zu akzeptieren.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span><dl> <dt><strong>WSAEPFNOSUPPORT</strong></dt> <dt>10046</dt> </dl></td>
<td><dl> <dt><span id="Protocol_family_not_supported."></span><span id="protocol_family_not_supported."></span><span id="PROTOCOL_FAMILY_NOT_SUPPORTED."></span>Protokollfamilie wird nicht unterstützt.</dt> <dd> Die Protokollfamilie wurde nicht im System konfiguriert, oder es ist keine Implementierung dafür vorhanden. Diese Nachricht hat eine etwas andere Bedeutung als WSAEAFNOSUPPORT. In den meisten Fällen ist sie jedoch austauschbar, und alle sockets Windows funktionen, die eine dieser Nachrichten zurückgeben, geben auch WSAEAFNOSUPPORT an.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span><dl> <dt><strong>WSAEAFNOSUPPORT</strong></dt> <dt>10047</dt> </dl></td>
<td><dl> <dt><span id="Address_family_not_supported_by_protocol_family."></span><span id="address_family_not_supported_by_protocol_family."></span><span id="ADDRESS_FAMILY_NOT_SUPPORTED_BY_PROTOCOL_FAMILY."></span>Die Adressfamilie wird von der Protokollfamilie nicht unterstützt.</dt> <dd> Es wurde eine Adresse verwendet, die mit dem angeforderten Protokoll nicht kompatibel ist. Alle Sockets werden mit einer zugeordneten Adressfamilie (d. h. AF_INET für Internetprotokolle) und einem generischen Protokolltyp (d. h. SOCK_STREAM) erstellt. Dieser Fehler wird zurückgegeben, wenn im Socketaufruf explizit ein falsches Protokoll angefordert wird oder wenn eine Adresse der falschen Familie für einen Socket verwendet wird, z. B. in <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto.</strong></a> <a href="/windows/desktop/api/Winsock2/nf-winsock2-socket"><strong></strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span><dl> <dt><strong>WSAEADDRINUSE</strong></dt> <dt>10048</dt> </dl></td>
<td><dl> <dt><span id="Address_already_in_use."></span><span id="address_already_in_use."></span><span id="ADDRESS_ALREADY_IN_USE."></span>Adresse, die bereits verwendet wird.</dt> <dd> In der Regel ist nur eine Verwendung jeder Socketadresse (Protokoll/IP-Adresse/Port) zulässig. Dieser Fehler tritt auf, wenn <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong></strong></a> eine Anwendung versucht, einen Socket an eine IP-Adresse/einen Port zu binden, die bereits für einen vorhandenen Socket oder einen Socket verwendet wurde, der nicht ordnungsgemäß geschlossen wurde oder der noch geschlossen wird. Für Serveranwendungen, die mehrere <strong>Sockets</strong> an dieselbe Portnummer binden müssen, sollten Sie <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> (SO_REUSEADDR) verwenden. Clientanwendungen müssen in der Regel <strong>überhaupt keine Bindung</strong> aufrufen.<a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>Connect</strong></a> wählt automatisch einen nicht verwendeten Port aus. Wenn <strong>bind</strong> mit einer Platzhalteradresse aufgerufen wird (mit ADDR_ANY), kann ein WSAEADDRINUSE-Fehler verzögert werden, bis ein Committed für die spezifische Adresse auftritt. Dies kann später durch einen Aufruf einer anderen Funktion geschehen, einschließlich <strong>connect</strong>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-listen"><strong>listen</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect</strong></a>oder <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span><dl> <dt><strong>WSAEADDRNOTAVAIL</strong></dt> <dt>10049</dt> </dl></td>
<td><dl> <dt><span id="Cannot_assign_requested_address."></span><span id="cannot_assign_requested_address."></span><span id="CANNOT_ASSIGN_REQUESTED_ADDRESS."></span>Die angeforderte Adresse kann nicht zugewiesen werden.</dt> <dd> Die angeforderte Adresse ist im Kontext ungültig. Dies ist normalerweise das Ergebnis eines <a href="/windows/desktop/api/winsock/nf-winsock-bind"><strong>Bindungsversuchs</strong></a> an eine Adresse, die für den lokalen Computer nicht gültig ist. Dies kann auch durch die Verbindung <a href="/windows/desktop/api/Winsock2/nf-winsock2-connect"><strong>,</strong></a> <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a>, <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect"><strong>WSAConnect,</strong></a> <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf"><strong>WSAJoinLeaf</strong></a>oder <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsasendto"><strong>WSASendTo</strong></a> entstehen, wenn die Remoteadresse oder der Remoteport für einen Remotecomputer nicht gültig ist (z. B. Adresse oder Port 0).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span><dl> <dt><strong>WSAENETDOWN</strong></dt> <dt>10050</dt> </dl></td>
<td><dl> <dt><span id="Network_is_down."></span><span id="network_is_down."></span><span id="NETWORK_IS_DOWN."></span>Das Netzwerk ist aus.</dt> <dd> Bei einem Socketvorgang war das Netzwerk inaktiv. Dies kann auf einen schwerwiegenden Fehler des Netzwerksystems (d. h., des Protokollstapels, den die Windows Sockets-DLL durchläuft), der Netzwerkschnittstelle oder des lokalen Netzwerks selbst hinweisen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span><dl> <dt><strong>WSAENETUNREACH</strong></dt> <dt>10051</dt> </dl></td>
<td><dl> <dt><span id="Network_is_unreachable."></span><span id="network_is_unreachable."></span><span id="NETWORK_IS_UNREACHABLE."></span>Das Netzwerk ist nicht erreichbar.</dt> <dd> Es wurde versucht, einen Socketvorgang in ein nicht erreichbares Netzwerk zu unternehmen. Dies bedeutet in der Regel, dass die lokale Software keine Route zum Remotehost kennt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENETRESET"></span><span id="wsaenetreset"></span><dl> <dt><strong>WSAENETRESET</strong></dt> <dt>10052</dt> </dl></td>
<td><dl> <dt><span id="Network_dropped_connection_on_reset."></span><span id="network_dropped_connection_on_reset."></span><span id="NETWORK_DROPPED_CONNECTION_ON_RESET."></span>Netzwerkverbindung beim Zurücksetzen gelöscht.</dt> <dd> Die Verbindung wurde unterbrochen, weil bei der Keep-Alive-Aktivität ein Fehler erkannt wurde, während der Vorgang durchgeführt wurde. Sie kann auch von <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt</strong></a> zurückgegeben werden, <a href="/windows/desktop/winsock/so-keepalive"><strong></strong></a> wenn versucht wird, SO_KEEPALIVE verbindung, die bereits fehlgeschlagen ist, festlegen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span><dl> <dt><strong>WSAECONNABORTED</strong></dt> <dt>10053</dt> </dl></td>
<td><dl> <dt><span id="Software_caused_connection_abort."></span><span id="software_caused_connection_abort."></span><span id="SOFTWARE_CAUSED_CONNECTION_ABORT."></span>Software hat den Verbindungsabbruch verursacht.</dt> <dd> Eine hergestellte Verbindung wurde von der Software auf Ihrem Hostcomputer abgebrochen, möglicherweise aufgrund eines Time outs für die Datenübertragung oder eines Protokollfehlers.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span><dl> <dt><strong>WSAECONNRESET</strong></dt> <dt>10054</dt> </dl></td>
<td><dl> <dt><span id="Connection_reset_by_peer."></span><span id="connection_reset_by_peer."></span><span id="CONNECTION_RESET_BY_PEER."></span>Verbindungszurücksetzung durch Peer.</dt> <dd> An existing connection was forcibly closed by the remote host. Dies führt normalerweise dazu, dass die Peeranwendung auf dem Remotehost plötzlich beendet wird, der Host neu gestartet wird, der Host oder die Remotenetzwerkschnittstelle deaktiviert ist oder der Remotehost ein hard close verwendet (weitere Informationen zur option SO_LINGER auf dem Remotesocket finden Sie unter <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>setsockopt).</strong></a> Dieser Fehler kann auch dazu führen, dass eine Verbindung aufgrund einer Keep-Alive-Aktivität unterbrochen wurde, die einen Fehler erkennt, während ein oder mehrere Vorgänge in Bearbeitung sind. Vorgänge, die in Bearbeitung waren, führen zu einem Fehler mit WSAENETRESET. Bei nachfolgenden Vorgängen kommt es zu einem Fehler mit WSAECONNRESET.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span><dl> <dt><strong>WSAENOBUFS</strong></dt> <dt>10055</dt> </dl></td>
<td><dl> <dt><span id="No_buffer_space_available."></span><span id="no_buffer_space_available."></span><span id="NO_BUFFER_SPACE_AVAILABLE."></span>Kein Pufferspeicherplatz verfügbar.</dt> <dd> Ein Vorgang für einen Socket konnte nicht ausgeführt werden, weil das System nicht über genügend Pufferspeicher oder über eine Warteschlange voll war.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEISCONN"></span><span id="wsaeisconn"></span><dl> <dt><strong>WSAEISCONN</strong></dt> <dt>10056</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_already_connected."></span><span id="socket_is_already_connected."></span><span id="SOCKET_IS_ALREADY_CONNECTED."></span>Der Socket ist bereits verbunden.</dt> <dd> An einem bereits verbundenen Socket wurde eine Verbindungsanforderung gestellt. Einige Implementierungen geben diesen Fehler auch zurück, wenn <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto</strong></a> für einen verbundenen SOCK_DGRAM-Socket aufgerufen wird (bei SOCK_STREAM-Sockets wird der to-Parameter in <strong>sendto</strong> ignoriert), obwohl andere Implementierungen dies als rechtliches Vorkommen behandeln. <em></em><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span><dl> <dt><strong>WSAENOTCONN</strong></dt> <dt>10057</dt> </dl></td>
<td><dl> <dt><span id="Socket_is_not_connected."></span><span id="socket_is_not_connected."></span><span id="SOCKET_IS_NOT_CONNECTED."></span>Der Socket ist nicht verbunden.</dt> <dd> Eine Anforderung zum Senden oder Empfangen von Daten war nicht möglich, da der Socket nicht verbunden ist und (beim Senden an einen Datagrammsocket mit <a href="/windows/desktop/api/winsock/nf-winsock-sendto"><strong>sendto)</strong></a>keine Adresse angegeben wurde. Dieser Fehler kann auch von jedem anderen Vorgangstyp <a href="/windows/desktop/winsock/so-keepalive"><strong></strong></a> zurückgegeben werden, z. B. legt <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt"><strong>dieockopt-Einstellung</strong></a> SO_KEEPALIVE, wenn die Verbindung zurückgesetzt wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span><dl> <dt><strong>WSAESHUTDOWN</strong></dt> <dt>10058</dt> </dl></td>
<td><dl> <dt><span id="Cannot_send_after_socket_shutdown."></span><span id="cannot_send_after_socket_shutdown."></span><span id="CANNOT_SEND_AFTER_SOCKET_SHUTDOWN."></span>Nach dem Herunterfahren des Sockets kann nicht gesendet werden.</dt> <dd> Eine Anforderung zum Senden oder Empfangen von Daten war nicht möglich, da der Socket bereits in dieser Richtung mit einem vorherigen Herunterfahrensaufruf <a href="/windows/desktop/api/winsock/nf-winsock-shutdown"><strong>heruntergefahren</strong></a> wurde. Durch Aufrufen <strong>des Herunterfahrens</strong> wird ein teilielles Schließen eines Sockets angefordert. Dies ist ein Signal, das sendet oder empfängt oder beides eingestellt wurde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span><dl> <dt><strong>WSAETOOMANYREFS</strong></dt> <dt>10059</dt> </dl></td>
<td><dl> <dt><span id="Too_many_references."></span><span id="too_many_references."></span><span id="TOO_MANY_REFERENCES."></span>Zu viele Verweise.</dt> <dd> Zu viele Verweise auf ein Kernelobjekt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span><dl> <dt><strong>WSAETIMEDOUT</strong></dt> <dt>10060</dt> </dl></td>
<td><dl> <dt><span id="Connection_timed_out."></span><span id="connection_timed_out."></span><span id="CONNECTION_TIMED_OUT."></span>Time out der Verbindung.</dt> <dd> Ein Verbindungsversuch ist fehlgeschlagen, weil die verbundene Partei nach einem bestimmten Zeitraum nicht ordnungsgemäß reagiert hat oder die hergestellte Verbindung fehlgeschlagen ist, weil der verbundene Host nicht reagiert hat.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span><dl> <dt><strong>WSAECONNREFUSED</strong></dt> <dt>10061</dt> </dl></td>
<td><dl> <dt><span id="Connection_refused."></span><span id="connection_refused."></span><span id="CONNECTION_REFUSED."></span>Die Verbindung wurde abgelehnt.</dt> <dd> Es konnte keine Verbindung hergestellt werden, da der Zielcomputer dies aktiv abgelehnt hat. Dies ergibt sich in der Regel aus dem Versuch, eine Verbindung mit einem Dienst herzustellen, der auf dem fremder Host inaktiv ist, d.&a; einer, auf dem keine Serveranwendung ausgeführt wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAELOOP"></span><span id="wsaeloop"></span><dl> <dt><strong>WSAELOOP</strong></dt> <dt>10062</dt> </dl></td>
<td><dl> <dt><span id="Cannot_translate_name."></span><span id="cannot_translate_name."></span><span id="CANNOT_TRANSLATE_NAME."></span>Name kann nicht übersetzt werden.</dt> <dd> Ein Name kann nicht übersetzt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span><dl> <dt><strong>WSAENAMETOOLONG</strong></dt> <dt>10063</dt> </dl></td>
<td><dl> <dt><span id="Name_too_long."></span><span id="name_too_long."></span><span id="NAME_TOO_LONG."></span>Der Name ist zu lang.</dt> <dd> Eine Namenskomponente oder ein Name war zu lang.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span><dl> <dt><strong>WSAEHOSTDOWN</strong></dt> <dt>10064</dt> </dl></td>
<td><dl> <dt><span id="Host_is_down."></span><span id="host_is_down."></span><span id="HOST_IS_DOWN."></span>Der Host ist aus.</dt> <dd> Ein Socketvorgang ist fehlgeschlagen, weil der Zielhost ausgefallen ist. Bei einem Socketvorgang ist ein in deader Host aufgetreten. Die Netzwerkaktivität auf dem lokalen Host wurde nicht initiiert. Diese Bedingungen werden wahrscheinlich eher durch den Fehler WSAETIMEDOUT angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span><dl> <dt><strong>WSAEHOSTUNREACH</strong></dt> <dt>10065</dt> </dl></td>
<td><dl> <dt><span id="No_route_to_host."></span><span id="no_route_to_host."></span><span id="NO_ROUTE_TO_HOST."></span>Keine Route zum Host.</dt> <dd> Versuch eines Socketvorgangs für einen nicht erreichbaren Host. Siehe WSAENETUNREACH.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span><dl> <dt><strong>WSAENOTEMPTY</strong></dt> <dt>10066</dt> </dl></td>
<td><dl> <dt><span id="Directory_not_empty."></span><span id="directory_not_empty."></span><span id="DIRECTORY_NOT_EMPTY."></span>Das Verzeichnis ist nicht leer.</dt> <dd> Ein nicht leeres Verzeichnis kann nicht entfernt werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span><dl> <dt><strong>WSAEPROCLIM</strong></dt> <dt>10067</dt> </dl></td>
<td><dl> <dt><span id="Too_many_processes."></span><span id="too_many_processes."></span><span id="TOO_MANY_PROCESSES."></span>Zu viele Prozesse.</dt> <dd> Eine Windows Sockets-Implementierung kann eine Beschränkung für die Anzahl von Anwendungen haben, die sie gleichzeitig verwenden können. <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup kann</strong></a> mit diesem Fehler fehlschlagen, wenn der Grenzwert erreicht wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEUSERS"></span><span id="wsaeusers"></span><dl> <dt><strong>WSIERER</strong></dt> <dt>10068</dt> </dl></td>
<td><dl> <dt><span id="User_quota_exceeded."></span><span id="user_quota_exceeded."></span><span id="USER_QUOTA_EXCEEDED."></span>Das Benutzerkontingent wurde überschritten.</dt> <dd> Das Benutzerkontingent ist nicht mehr erreicht. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDQUOT"></span><span id="wsaedquot"></span><dl> <dt><strong>WSAEDQUOT</strong></dt> <dt>10069</dt> </dl></td>
<td><dl> <dt><span id="Disk_quota_exceeded."></span><span id="disk_quota_exceeded."></span><span id="DISK_QUOTA_EXCEEDED."></span>Datenträgerkontingent überschritten.</dt> <dd> Das Datenträgerkontingent ist nicht mehr verfügbar. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAESTALE"></span><span id="wsaestale"></span><dl> <dt><strong>WSAESTALE</strong></dt> <dt>10070</dt> </dl></td>
<td><dl> <dt><span id="Stale_file_handle_reference."></span><span id="stale_file_handle_reference."></span><span id="STALE_FILE_HANDLE_REFERENCE."></span>Veralteter Dateihandleverweis.</dt> <dd> Der Dateihandpunktverweis ist nicht mehr verfügbar. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEREMOTE"></span><span id="wsaeremote"></span><dl> <dt><strong>WSAEREMOTE</strong></dt> <dt>10071</dt> </dl></td>
<td><dl> <dt><span id="Item_is_remote."></span><span id="item_is_remote."></span><span id="ITEM_IS_REMOTE."></span>Das Element ist remote.</dt> <dd> Das Element ist lokal nicht verfügbar. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span><dl> <dt><strong>WSASYSNOTREADY</strong></dt> <dt>10091</dt> </dl></td>
<td><dl> <dt><span id="Network_subsystem_is_unavailable."></span><span id="network_subsystem_is_unavailable."></span><span id="NETWORK_SUBSYSTEM_IS_UNAVAILABLE."></span>Das Netzwerksubsystem ist nicht verfügbar.</dt> <dd> Dieser Fehler wird von <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup</strong></a> zurückgegeben, wenn die Windows Sockets-Implementierung derzeit nicht funktionieren kann, da das zugrunde liegende System, das zum Bereitstellen von Netzwerkdiensten verwendet wird, derzeit nicht verfügbar ist. Benutzer sollten Dies überprüfen:<br/> </dd> </dl>
<ul>
<li>Die entsprechende Windows Sockets-DLL-Datei befindet sich im aktuellen Pfad.</li>
<li>Sie versuchen nicht, mehrere Sockets-Windows gleichzeitig zu verwenden. Wenn auf Ihrem System mehr als eine Winsock-DLL vorhanden ist, stellen Sie sicher, dass die erste im Pfad für das derzeit geladene Netzwerksubsystem geeignet ist.</li>
<li>In Windows Sockets-Implementierungsdokumentation wird sichergestellt, dass alle erforderlichen Komponenten derzeit ordnungsgemäß installiert und konfiguriert sind.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span><dl> <dt><strong>WSAVERNOTSUPPORTED</strong></dt> <dt>10092</dt> </dl></td>
<td><dl> <dt><span id="Winsock.dll_version_out_of_range."></span><span id="winsock.dll_version_out_of_range."></span><span id="WINSOCK.DLL_VERSION_OUT_OF_RANGE."></span>Winsock.dll version out of range (Version liegt nicht im Bereich).</dt> <dd> Die aktuelle Windows Sockets-Implementierung unterstützt nicht die Windows Sockets-Spezifikationsversion, die von der Anwendung angefordert wird. Vergewissern Sie sich, dass auf keine veralteten Windows Sockets-DLL-Dateien zugegriffen wird.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span><dl> <dt><strong>WSANO INITIALISED</strong></dt> <dt>10093</dt> </dl></td>
<td><dl> <dt><span id="Successful_WSAStartup_not_yet_performed."></span><span id="successful_wsastartup_not_yet_performed."></span><span id="SUCCESSFUL_WSASTARTUP_NOT_YET_PERFORMED."></span>Erfolgreiches WSAStartup wurde noch nicht ausgeführt.</dt> <dd> Entweder hat die Anwendung <a href="/windows/desktop/api/winsock/nf-winsock-wsastartup"><strong>WSAStartup nicht aufgerufen,</strong></a> oder <strong>WSAStartup ist fehlgeschlagen.</strong> Die Anwendung kann auf einen Socket zugreifen, der der aktuelle aktive Task nicht besitzt (d. h. versucht, einen Socket zwischen Tasks gemeinsam zu verwenden), oder <a href="/windows/desktop/api/winsock/nf-winsock-wsacleanup"><strong>WSACleanup</strong></a> wurde zu oft aufgerufen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEDISCON"></span><span id="wsaediscon"></span><dl> <dt><strong>WSAEDISCON</strong></dt> <dt>10101</dt> </dl></td>
<td><dl> <dt><span id="Graceful_shutdown_in_progress."></span><span id="graceful_shutdown_in_progress."></span><span id="GRACEFUL_SHUTDOWN_IN_PROGRESS."></span>Das ordnungsgemäß herunterfahren wird in Bearbeitung.</dt> <dd> Wird von <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecv"><strong>WSARecv und</strong></a> <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom"><strong>WSARecvFrom</strong></a> zurückgegeben, um anzugeben, dass die Remote-Partei eine sequenz zum ordnungsgemäßen Herunterfahren initiiert hat.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAENOMORE"></span><span id="wsaenomore"></span><dl> <dt><strong>WSAENOMORE</strong></dt> <dt>10102</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Keine ergebnisse mehr.</dt> <dd> Von der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext-Funktion</strong></a> können keine ergebnisse mehr zurückgegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span><dl> <dt><strong>WSAECANCELLED</strong></dt> <dt>10103</dt> </dl></td>
<td><dl> <dt><span id="Call_has_been_canceled."></span><span id="call_has_been_canceled."></span><span id="CALL_HAS_BEEN_CANCELED."></span>Der Aufruf wurde abgebrochen.</dt> <dd> Ein Aufruf der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd-Funktion</strong></a> wurde ausgeführt, während dieser Aufruf noch verarbeitet wurde. Der Aufruf wurde abgebrochen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span><dl> <dt><strong>WSAEINVALIDPROCTABLE</strong></dt> <dt>10104</dt> </dl></td>
<td><dl> <dt><span id="Procedure_call_table_is_invalid."></span><span id="procedure_call_table_is_invalid."></span><span id="PROCEDURE_CALL_TABLE_IS_INVALID."></span>Die Prozeduraufruftabelle ist ungültig.</dt> <dd> Die Aufruftabelle der Dienstanbieterprozedur ist ungültig. Ein Dienstanbieter hat eine prozedurentabelle vom Dienstanbieter zurückgegeben, um Ws2_32.dll. Dies wird normalerweise dadurch verursacht, dass mindestens einer der Funktionszeiger <strong>NULL ist.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span><dl> <dt><strong>WSAEINVALIDPROVIDER</strong></dt> <dt>10105</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_is_invalid."></span><span id="service_provider_is_invalid."></span><span id="SERVICE_PROVIDER_IS_INVALID."></span>Der Dienstanbieter ist ungültig.</dt> <dd> Der angeforderte Dienstanbieter ist ungültig. Dieser Fehler wird von den <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo"><strong>Funktionen WSCGetProviderInfo</strong></a> und <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32"><strong>WSCGetProviderInfo32</strong></a> zurückgegeben, wenn der angegebene Protokolleintrag nicht gefunden werden konnte. Dieser Fehler wird auch zurückgegeben, wenn der Dienstanbieter eine andere Versionsnummer als 2.0 zurückgegeben hat.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span><dl> <dt><strong>WSAEPROVIDERFAILEDINIT</strong></dt> <dt>10106</dt> </dl></td>
<td><dl> <dt><span id="Service_provider_failed_to_initialize."></span><span id="service_provider_failed_to_initialize."></span><span id="SERVICE_PROVIDER_FAILED_TO_INITIALIZE."></span>Fehler beim Initialisieren des Dienstanbieters.</dt> <dd> Der angeforderte Dienstanbieter konnte nicht geladen oder initialisiert werden. Dieser Fehler wird zurückgegeben, wenn die DLL eines Dienstanbieters nicht geladen werden konnte<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya"><strong>(LoadLibrary-Fehler)</strong></a> oder die <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup"><strong>WSPStartup-</strong></a> oder <a href="/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup"><strong>NSPStartup-Funktion</strong></a> des Anbieters fehlgeschlagen ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span><dl> <dt><strong>WSASYSCALLFAILURE</strong></dt> <dt>10107</dt> </dl></td>
<td><dl> <dt><span id="System_call_failure."></span><span id="system_call_failure."></span><span id="SYSTEM_CALL_FAILURE."></span>Fehler beim Systemaufruf.</dt> <dd> Ein Systemaufruf, der nie fehlschlagen sollte, ist fehlgeschlagen. Dies ist ein generischer Fehlercode, der unter verschiedenen Bedingungen zurückgegeben wird. <br/> Wird zurückgegeben, wenn ein Systemaufruf, der nie fehlschlagen sollte, fehlschlägt. Beispiel: Ein Aufruf von <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents"><strong>WaitForMultipleEvents</strong></a> schlägt fehl, oder eine der Registrierungsfunktionen versucht nicht, die Protokoll-/Namespacekataloge zu bearbeiten.<br/> Wird zurückgegeben, wenn ein Anbieter SUCCESS nicht zurücksingt und keinen erweiterten Fehlercode enthält. Kann auf einen Implementierungsfehler des Dienstanbieters hinweisen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span><dl> <dt><strong>WSASERVICE_NOT_FOUND</strong></dt> <dt>10108</dt> </dl></td>
<td><dl> <dt><span id="Service_not_found."></span><span id="service_not_found."></span><span id="SERVICE_NOT_FOUND."></span>Der Dienst wurde nicht gefunden.</dt> <dd> Ein solcher Dienst ist nicht bekannt. Der Dienst kann im angegebenen Namensraum nicht gefunden werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span><dl> <dt><strong>WSATYPE_NOT_FOUND</strong></dt> <dt>10109</dt> </dl></td>
<td><dl> <dt><span id="Class_type_not_found."></span><span id="class_type_not_found."></span><span id="CLASS_TYPE_NOT_FOUND."></span>Der Klassentyp wurde nicht gefunden.</dt> <dd> Die angegebene Klasse wurde nicht gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span><dl> <dt><strong>WSA_E_NO_MORE</strong></dt> <dt>10110</dt> </dl></td>
<td><dl> <dt><span id="No_more_results."></span><span id="no_more_results."></span><span id="NO_MORE_RESULTS."></span>Keine ergebnisse mehr.</dt> <dd> Von der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext-Funktion</strong></a> können keine ergebnisse mehr zurückgegeben werden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span><dl> <dt><strong>WSA_E_CANCELLED</strong></dt> <dt>10111</dt> </dl></td>
<td><dl> <dt><span id="Call_was_canceled."></span><span id="call_was_canceled."></span><span id="CALL_WAS_CANCELED."></span>Der Aufruf wurde abgebrochen.</dt> <dd> Ein Aufruf der <a href="/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend"><strong>WSALookupServiceEnd-Funktion</strong></a> wurde ausgeführt, während dieser Aufruf noch verarbeitet wurde. Der Aufruf wurde abgebrochen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSAEREFUSED"></span><span id="wsaerefused"></span><dl> <dt><strong>WSAEREFUSED</strong></dt> <dt>10112</dt> </dl></td>
<td><dl> <dt><span id="Database_query_was_refused."></span><span id="database_query_was_refused."></span><span id="DATABASE_QUERY_WAS_REFUSED."></span>Die Datenbankabfrage wurde abgelehnt.</dt> <dd> Eine Datenbankabfrage ist fehlgeschlagen, weil sie aktiv abgelehnt wurde.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span><dl> <dt><strong>WSAHOST_NOT_FOUND</strong></dt> <dt>11001</dt> </dl></td>
<td><dl> <dt><span id="Host_not_found."></span><span id="host_not_found."></span><span id="HOST_NOT_FOUND."></span>Host nicht gefunden.</dt> <dd> Ein solcher Host ist nicht bekannt. Der Name ist kein offizieller Hostname oder Alias, oder er kann nicht in den abgefragten Datenbanken gefunden werden. Dieser Fehler kann auch für Protokoll- und Dienstabfragen zurückgegeben werden. Dies bedeutet, dass der angegebene Name in der relevanten Datenbank nicht gefunden werden konnte.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span><dl> <dt><strong>WSATRY_AGAIN</strong></dt> <dt>11002</dt> </dl></td>
<td><dl> <dt><span id="Nonauthoritative_host_not_found."></span><span id="nonauthoritative_host_not_found."></span><span id="NONAUTHORITATIVE_HOST_NOT_FOUND."></span>Nicht authentifizierter Host wurde nicht gefunden.</dt> <dd> Dies ist normalerweise ein vorübergehender Fehler während der Hostnamensauflösung und bedeutet, dass der lokale Server keine Antwort von einem autoritativen Server empfangen hat. Ein erneuter Versuch zu einem späteren Zeitpunkt wird möglicherweise erfolgreich durchgeführt.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span><dl> <dt><strong>WSANO_RECOVERY</strong></dt> <dt>11003</dt> </dl></td>
<td><dl> <dt><span id="This_is_a_nonrecoverable_error."></span><span id="this_is_a_nonrecoverable_error."></span><span id="THIS_IS_A_NONRECOVERABLE_ERROR."></span>Dies ist ein nicht behebbarer Fehler.</dt> <dd> Dies weist darauf hin, dass während einer Datenbanksuche ein nicht behebbarer Fehler aufgetreten ist. Dies kann daran liegt, dass die Datenbankdateien (z. B. BSD-kompatible HOSTS-, SERVICES- oder PROTOCOLS-Dateien) nicht gefunden wurden oder dass vom Server eine DNS-Anforderung mit einem schwerwiegenden Fehler zurückgegeben wurde.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSANO_DATA"></span><span id="wsano_data"></span><dl> <dt><strong>WSANO_DATA</strong></dt> <dt>11004</dt> </dl></td>
<td><dl> <dt><span id="Valid_name__no_data_record_of_requested_type."></span><span id="valid_name__no_data_record_of_requested_type."></span><span id="VALID_NAME__NO_DATA_RECORD_OF_REQUESTED_TYPE."></span>Gültiger Name, kein Datensatz des angeforderten Typs.</dt> <dd> Der angeforderte Name ist gültig und wurde in der Datenbank gefunden, verfügt jedoch nicht über die richtigen zugeordneten Daten, für die aufgelöst wird. Das übliche Beispiel hierfür ist ein Übersetzungsversuch zwischen Hostname und Adresse (mit <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname"><strong>gethostbyname</strong></a> oder <a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-wsaasyncgethostbyname"><strong>WSAAsyncGetHostByName),</strong></a>bei dem dns (Domain Name Server) verwendet wird. Ein MX-Eintrag wird zurückgegeben, aber kein A-Eintrag, der angibt, dass der Host selbst vorhanden, aber nicht direkt erreichbar ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span><dl> <dt><strong>WSA_QOS_RECEIVERS</strong></dt> <dt>11005</dt> </dl></td>
<td><dl> <dt><span id="QoS_receivers."></span><span id="qos_receivers."></span><span id="QOS_RECEIVERS."></span>QoS-Empfänger.</dt> <dd> Mindestens eine QoS-Reserve ist eingetroffen.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span><dl> <dt><strong>WSA_QOS_SENDERS</strong></dt> <dt>11006</dt> </dl></td>
<td><dl> <dt><span id="QoS_senders."></span><span id="qos_senders."></span><span id="QOS_SENDERS."></span>QoS-Absender.</dt> <dd> Mindestens ein QoS-Sendepfad ist eingetroffen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span><dl> <dt><strong>WSA_QOS_NO_SENDERS</strong></dt> <dt>11007</dt> </dl></td>
<td><dl> <dt><span id="No_QoS_senders."></span><span id="no_qos_senders."></span><span id="NO_QOS_SENDERS."></span>Keine QoS-Absender.</dt> <dd> Es gibt keine QoS-Absender.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span><dl> <dt><strong>WSA_QOS_NO_RECEIVERS</strong></dt> <dt>11008</dt> </dl></td>
<td><dl> <dt><span id="QoS_no_receivers."></span><span id="qos_no_receivers."></span><span id="QOS_NO_RECEIVERS."></span>QoS keine Empfänger.</dt> <dd> Es gibt keine QoS-Empfänger.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span><dl> <dt><strong>WSA_QOS_REQUEST_CONFIRMED</strong></dt> <dt>11009</dt> </dl></td>
<td><dl> <dt><span id="QoS_request_confirmed."></span><span id="qos_request_confirmed."></span><span id="QOS_REQUEST_CONFIRMED."></span>QoS-Anforderung bestätigt.</dt> <dd> Die Anforderung der QoS-Reserve wurde bestätigt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span><dl> <dt><strong>WSA_QOS_ADMISSION_FAILURE</strong></dt> <dt>11010</dt> </dl></td>
<td><dl> <dt><span id="QoS_admission_error."></span><span id="qos_admission_error."></span><span id="QOS_ADMISSION_ERROR."></span>QoS-Zugangsfehler.</dt> <dd> Aufgrund fehlender Ressourcen ist ein QoS-Fehler aufgetreten.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span><dl> <dt><strong>WSA_QOS_POLICY_FAILURE</strong></dt> <dt>11011</dt> </dl></td>
<td><dl> <dt><span id="QoS_policy_failure."></span><span id="qos_policy_failure."></span><span id="QOS_POLICY_FAILURE."></span>QoS-Richtlinienfehler.</dt> <dd> Die QoS-Anforderung wurde abgelehnt, da das Richtliniensystem die angeforderte Ressource nicht innerhalb der vorhandenen Richtlinie zuordnen konnte. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span><dl> <dt><strong>WSA_QOS_BAD_STYLE</strong></dt> <dt>11012</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_style."></span><span id="qos_bad_style."></span><span id="QOS_BAD_STYLE."></span>Ungültiger QoS-Stil.</dt> <dd> Ein unbekannter oder widersprüchlicher QoS-Stil wurde gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span><dl> <dt><strong>WSA_QOS_BAD_OBJECT</strong></dt> <dt>11013</dt> </dl></td>
<td><dl> <dt><span id="QoS_bad_object."></span><span id="qos_bad_object."></span><span id="QOS_BAD_OBJECT."></span>Ungültiges QoS-Objekt.</dt> <dd> Bei einem Teil der Filterspezifikation oder des anbieterspezifischen Puffers ist im Allgemeinen ein Problem aufgetreten.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span><dl> <dt><strong>WSA_QOS_TRAFFIC_CTRL_ERROR</strong></dt> <dt>11014</dt> </dl></td>
<td><dl> <dt><span id="QoS_traffic_control_error."></span><span id="qos_traffic_control_error."></span><span id="QOS_TRAFFIC_CONTROL_ERROR."></span>QoS-Datenverkehrssteuerungsfehler.</dt> <dd> Fehler bei der zugrunde liegenden TRAFFIC CONTROL-API (TC), da die generische QoS-Anforderung für die lokale Erzwingung durch die TC-API konvertiert wurde. Dies kann auf einen Fehler aufgrund von nicht genügend Arbeitsspeicher oder auf einen internen QoS-Anbieterfehler zurückzuführen sein. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span><dl> <dt><strong>WSA_QOS_GENERIC_ERROR</strong></dt> <dt>11015</dt> </dl></td>
<td><dl> <dt><span id="QoS_generic_error."></span><span id="qos_generic_error."></span><span id="QOS_GENERIC_ERROR."></span>Generischer QoS-Fehler.</dt> <dd> Ein allgemeiner QoS-Fehler.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span><dl> <dt><strong>WSA_QOS_ESERVICETYPE</strong></dt> <dt>11016</dt> </dl></td>
<td><dl> <dt><span id="QoS_service_type_error."></span><span id="qos_service_type_error."></span><span id="QOS_SERVICE_TYPE_ERROR."></span>QoS-Diensttypfehler.</dt> <dd> In der QoS-Flowspec wurde ein ungültiger oder unbekannter Diensttyp gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span><dl> <dt><strong>WSA_QOS_EFLOWSPEC</strong></dt> <dt>11017</dt> </dl></td>
<td><dl> <dt><span id="QoS_flowspec_error."></span><span id="qos_flowspec_error."></span><span id="QOS_FLOWSPEC_ERROR."></span>QoS flowspec-Fehler.</dt> <dd> In der <a href="/windows/win32/api/winsock2/ns-winsock2-qos"><strong>QOS-Struktur</strong></a> wurde eine ungültige oder inkonsistente Flowspec gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span><dl> <dt><strong>WSA_QOS_EPROVSPECBUF</strong></dt> <dt>11018</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider_buffer."></span><span id="invalid_qos_provider_buffer."></span><span id="INVALID_QOS_PROVIDER_BUFFER."></span>Ungültiger QoS-Anbieterpuffer.</dt> <dd> Ein ungültiger QoS-anbieterspezifischer Puffer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span><dl> <dt><strong>WSA_QOS_EFILTERSTYLE</strong></dt> <dt>11019</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_style."></span><span id="invalid_qos_filter_style."></span><span id="INVALID_QOS_FILTER_STYLE."></span>Ungültiger QoS-Filterstil.</dt> <dd> Ein ungültiger QoS-Filterstil wurde verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span><dl> <dt><strong>WSA_QOS_EFILTERTYPE</strong></dt> <dt>11020</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_filter_type."></span><span id="invalid_qos_filter_type."></span><span id="INVALID_QOS_FILTER_TYPE."></span>Ungültiger QoS-Filtertyp.</dt> <dd> Ein ungültiger QoS-Filtertyp wurde verwendet.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span><dl> <dt><strong>WSA_QOS_EFILTERCOUNT</strong></dt> <dt>11021</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_filter_count."></span><span id="incorrect_qos_filter_count."></span><span id="INCORRECT_QOS_FILTER_COUNT."></span>Falsche QoS-Filteranzahl.</dt> <dd> In FLOWDESCRIPTOR wurde eine falsche Anzahl von QoS-FILTERSPECs angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span><dl> <dt><strong>WSA_QOS_EOBJLENGTH</strong></dt> <dt>11022</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_object_length."></span><span id="invalid_qos_object_length."></span><span id="INVALID_QOS_OBJECT_LENGTH."></span>Ungültige QoS-Objektlänge.</dt> <dd> Ein Objekt mit einem ungültigen ObjectLength-Feld wurde im QoS-anbieterspezifischen Puffer angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span><dl> <dt><strong>WSA_QOS_EFLOWCOUNT</strong></dt> <dt>11023</dt> </dl></td>
<td><dl> <dt><span id="Incorrect_QoS_flow_count."></span><span id="incorrect_qos_flow_count."></span><span id="INCORRECT_QOS_FLOW_COUNT."></span>Falsche QoS-Flussanzahl.</dt> <dd> In der QoS-Struktur wurde eine falsche Anzahl von Flussdeskriptoren angegeben.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span><dl> <dt><strong>WSA_QOS_EUNKOWNPSOBJ</strong></dt> <dt>11024</dt> </dl></td>
<td><dl> <dt><span id="Unrecognized_QoS_object."></span><span id="unrecognized_qos_object."></span><span id="UNRECOGNIZED_QOS_OBJECT."></span>Unbekanntes QoS-Objekt.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde ein nicht erkanntes Objekt gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span><dl> <dt><strong>WSA_QOS_EPOLICYOBJ</strong></dt> <dt>11025</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_policy_object."></span><span id="invalid_qos_policy_object."></span><span id="INVALID_QOS_POLICY_OBJECT."></span>Ungültiges QoS-Richtlinienobjekt.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde ein ungültiges Richtlinienobjekt gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span><dl> <dt><strong>WSA_QOS_EFLOWDESC</strong></dt> <dt>11026</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_flow_descriptor."></span><span id="invalid_qos_flow_descriptor."></span><span id="INVALID_QOS_FLOW_DESCRIPTOR."></span>Ungültiger QoS-Flussdeskriptor.</dt> <dd> In der Flowdeskriptorliste wurde ein ungültiger QoS-Flowdeskriptor gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span><dl> <dt><strong>WSA_QOS_EPSFLOWSPEC</strong></dt> <dt>11027</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_flowspec."></span><span id="invalid_qos_provider-specific_flowspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FLOWSPEC."></span>Ungültige QoS-Anbieterspezifische Flowspec.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde eine ungültige oder inkonsistente Flowspec gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span><dl> <dt><strong>WSA_QOS_EPSFILTERSPEC</strong></dt> <dt>11028</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_provider-specific_filterspec."></span><span id="invalid_qos_provider-specific_filterspec."></span><span id="INVALID_QOS_PROVIDER-SPECIFIC_FILTERSPEC."></span>Ungültige QoS-Anbieterspezifische Filterspezifikation.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde eine ungültige FILTERSPEC gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span><dl> <dt><strong>WSA_QOS_ESDMODEOBJ</strong></dt> <dt>11029</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shape_discard_mode_object."></span><span id="invalid_qos_shape_discard_mode_object."></span><span id="INVALID_QOS_SHAPE_DISCARD_MODE_OBJECT."></span>Ungültiges QoS-Shape-Objekt im Verwerfungsmodus.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde ein ungültiges Objekt für den Formverwerfungsmodus gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span><dl> <dt><strong>WSA_QOS_ESHAPERATEOBJ</strong></dt> <dt>11030</dt> </dl></td>
<td><dl> <dt><span id="Invalid_QoS_shaping_rate_object."></span><span id="invalid_qos_shaping_rate_object."></span><span id="INVALID_QOS_SHAPING_RATE_OBJECT."></span>Ungültiges QoS-Strukturierungsratenobjekt.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde ein ungültiges Strukturierungsratenobjekt gefunden.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span><dl> <dt><strong>WSA_QOS_RESERVED_PETYPE</strong></dt> <dt>11031</dt> </dl></td>
<td><dl> <dt><span id="Reserved_policy_QoS_element_type."></span><span id="reserved_policy_qos_element_type."></span><span id="RESERVED_POLICY_QOS_ELEMENT_TYPE."></span>QoS-Elementtyp für reservierte Richtlinien.</dt> <dd> Im QoS-Anbieterspezifischen Puffer wurde ein reserviertes Richtlinienelement gefunden.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winsock2.h; </dt> <dt>Winerror.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehlercodes: errno, h \_ errno und WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Behandeln von Winsock-Fehlern](handling-winsock-errors.md)
</dt> <dt>

[**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
