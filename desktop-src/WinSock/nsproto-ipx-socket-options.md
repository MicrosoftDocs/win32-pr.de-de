---
description: In den folgenden Tabellen werden nsproto \_ -IPX-Socketoptionen beschrieben, die für Sockets gelten, die für die IPX/SPX-Adressfamilie (AF \_ IPX) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen getsockopt und setsockopt.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: NSPROTO_IPX Socketoptionen (wsnwlink. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e1fabed1963c3549d2d5a34fb432cac795e07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365755"
---
# <a name="nsproto_ipx-socket-options"></a>Nsproto- \_ IPX-Socketoptionen

In den folgenden Tabellen werden **nsproto- \_ IPX** -Socketoptionen beschrieben, die für Sockets gelten, die für die IPX/SPX-Adressfamilie (AF \_ IPX) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**Nsproto- \_ IPX-Socketoptionen**</dt> <dd> <dl> <dt> 

| Option                      | Herunterladen | Set | Optval-Typ                  | BESCHREIBUNG                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPX- \_ Adresse                | ja |     | **IPX- \_ Adress \_ Daten**       | Gibt Informationen über den spezifischen Adapter zurück, auf dem IPX aktiviert ist.                                                                                                                                                                                                          |
| Benachrichtigung zur IPX- \_ Adresse \_        | ja |     | **IPX- \_ Adress \_ Daten**       | Benachrichtigt asynchron, wenn der Status eines IPX-Adapters geändert wird.                                                                                                                                                                                                              |
| IPX- \_ DSType                 | ja | ja | DWORD                        | Ruft den Wert des Datastream-Felds im SPX-Header ab, mit dem Pakete gesendet werden sollen, oder legt diesen fest.                                                                                                                                                                                          |
| Erweiterte IPX- \_ \_ Adresse      |     | ja | DWORD (Boolean)              | Aktiviert die erweiterte Adressierungs Option für IPX-Pakete.                                                                                                                                                                                                                          |
| IPX- \_ filterptype            | ja | ja | DWORD                        | Ruft den aktuellen IPX-Empfangs Filter-Pakettyp ab oder legt ihn fest. Nur IPX-Pakete mit einem Pakettyp, der dem im optval-Parameter angegebenen Wert entspricht, werden zurückgegeben. Pakete mit einem Pakettyp, der nicht entspricht, werden verworfen. Dies gilt nur für einen Datagramm-Socket. |
| IPX \_ getnetinfo             | ja |     | **IPX- \_ netnum- \_ Daten**        | Gibt Informationen zu einer bestimmten IPX-Netzwerk Nummer zurück. Der netnum-Member der **IPX \_ netnum- \_ Daten** Struktur muss auf die IPX-Netzwerk Nummer festgelegt werden, die zurückgegeben werden soll.                                                                                                     |
| IPX \_ getnetinfo- \_ Norip      | ja |     | **IPX- \_ netnum- \_ Daten**        | Gibt Informationen zu einer bestimmten IPX-Netzwerk Nummer zurück, ohne eine RIP-Anforderung zu senden. Der netnum-Member der **IPX \_ netnum- \_ Daten** Struktur muss auf die IPX-Netzwerk Nummer festgelegt werden, die zurückgegeben werden soll.                                                                       |
| IPX- \_ unmittelnachweis        |     | ja | DWORD (Boolean)              | Wenn der Wert auf **true** festgelegt ist, wird das Senden von ACKs für eine SPX-Verbindung nicht verzögert.                                                                                                                                                                                                             |
| Maximaler IPX- \_ \_ Adapter ( \_ num)      | ja |     | DWORD                        | Gibt die Anzahl der vorhandenen IPX-fähigen Adapter zurück.                                                                                                                                                                                                                             |
| IPX \_ MaxSize                | ja |     | DWORD                        | Gibt die maximale IPX-Datagramm-Größe in Bytes zurück, die gesendet werden können.                                                                                                                                                                                                                |
| IPX- \_ pType                  | ja | ja | DWORD                        | Ruft den Pakettyp ab oder legt ihn fest. Der im optval-Parameter angegebene Wert wird für jedes von diesem Socket gesendete IPX-Paket als Pakettyp festgelegt.                                                                                                                             |
| IPX- \_ Empfangs \_ Broadcast     |     | ja | DWORD (Boolean)              | Wenn der Wert auf **true** festgelegt ist, werden Broadcast-IPX-Pakete                                                                                                                                                                                                                              |
| IPX- \_ recvhdr                |     | ja | DWORD (Boolean)              | Wenn diese Einstellung auf **true** festgelegt ist, werden IPX-Protokoll Header mit Daten empfangen.                                                                                                                                                                                                                     |
| IPX \_ reripnetnumber         | ja |     | **IPX- \_ netnum- \_ Daten**        | Gibt Informationen zu einer angegebenen IPX-Netzwerk Nummer mithilfe einer neuen RIP-Anforderung zurück. Der netnum-Member der **IPX \_ netnum- \_ Daten** Struktur muss auf die IPX-Netzwerk Nummer festgelegt werden, die zurückgegeben werden soll.                                                                            |
| IPX- \_ spxgetconnectionstatus | ja |     | **IPX- \_ SPX-Statusdaten \_** | Gibt Informationen zu einer verbundenen SPX-Socketstatistik zurück.                                                                                                                                                                                                                |
| IPX \_ stopfilterptype        |     | ja | DWORD                        | Entfernt den Filter und beendet die Filterung des im optval-Parameter angegebenen Pakettyps.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Windows-Unterstützung für nsproto \_ IPX-Optionen**</dt> <dd> <dl> <dt> 

| Option                      | Windows Vista und höher | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9X/ME |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| IPX- \_ Adresse                |                         | x                   | x          | x            | x           | x             |
| Benachrichtigung zur IPX- \_ Adresse \_        |                         | x                   | x          | x            | x           | x             |
| IPX- \_ DSType                 |                         | x                   | x          | x            | x           | x             |
| Erweiterte IPX- \_ \_ Adresse      |                         | x                   | x          | x            | x           | x             |
| IPX- \_ filterptype            |                         | x                   | x          | x            | x           | x             |
| IPX \_ getnetinfo             |                         | x                   | x          | x            | x           | x             |
| IPX \_ getnetinfo- \_ Norip      |                         | x                   | x          | x            | x           | x             |
| IPX- \_ unmittelnachweis        |                         | x                   | x          | x            | x           | x             |
| Maximaler IPX- \_ \_ Adapter ( \_ num)      |                         | x                   | x          | x            | x           | x             |
| IPX \_ MaxSize                |                         | x                   | x          | x            | x           | x             |
| IPX- \_ pType                  |                         | x                   | x          | x            | x           | x             |
| IPX- \_ Empfangs \_ Broadcast     |                         | x                   | x          | x            | x           | x             |
| IPX- \_ recvhdr                |                         | x                   | x          | x            | x           | x             |
| IPX \_ reripnetnumber         |                         | x                   | x          | x            | x           | x             |
| IPX- \_ spxgetconnectionstatus |                         | x                   | x          | x            | x           | x             |
| IPX \_ stopfilterptype        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

Die folgenden **nsproto- \_ IPX** -Socketoptionen wurden in Windows Sockets 2 Protocol-Specific Anhang definiert, aber nicht durch das Windows IPX/SPX-Protokoll implementiert.

*Ebene* **=** **Nsproto \_ IPX**



| Option           | type | Standard                         | Bedeutung                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPX- \_ Prüfsumme    | Bool | aus                             | Wenn festgelegt, führt IPX eine Prüfsumme für ausgehende Pakete aus und überprüft die Prüfsumme eingehender Pakete.                                                          |
| IPX- \_ txpktsize   | INT  | Mediengröße auf maximal 1466 | Legt die maximale Größe des sendedatagramms fest. Diese Größe enthält nicht den IPX-Header oder beliebige Medien Header, die ebenfalls verwendet werden können. Kann auf die Mediengröße erweitert werden.    |
| IPX- \_ rxpktsize   | INT  | Mediengröße auf maximal 1466 | Legt die maximale Größe des Empfangs Datagramms fest. Diese Größe enthält nicht den IPX-Header oder beliebige Medien Header, die ebenfalls verwendet werden können. Kann auf die Mediengröße erweitert werden. |
| IPX- \_ txmediasize | INT  | Primäres Board                   | Gibt die Größe des Sende Mediums zurück, die eine obere Grenze für die Datagramm-Größe festlegt.                                                                                       |
| IPX- \_ rxmediasize | INT  | Primäres Board                   | Gibt die Größe des Empfangs Mediums zurück, die eine obere Grenze für die Datagramm-Größe festlegt.                                                                                    |
| IPX- \_ primär     | Bool | Primär                         | Schränkt den Datenverkehr auf das primäre Netzwerk Board ein.                                                                                                               |



 

Die folgenden **nsproto \_ SPX** -Socketoptionen wurden in Windows Sockets 2 Protocol-Specific Anhang definiert, aber nicht unter Windows durch das Windows IPX/SPX-Protokoll implementiert.

*Ebene* **=** **Nsproto \_ SPX**



| Option           | type | Standard                         | Bedeutung                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SPX- \_ Prüfsumme    | Bool | aus                             | Wenn festgelegt, führt IPX eine Prüfsumme für ausgehende Pakete aus und überprüft die Prüfsumme eingehender Pakete. Nicht auf allen Plattformen unterstützt.                          |
| SPX- \_ txpktsize   | INT  | Mediengröße auf maximal 1466 | Legt die maximale Größe des sendedatagramms fest. Diese Größe enthält nicht den SPX-Header oder beliebige Medien Header, die ebenfalls verwendet werden können. Kann auf die Mediengröße erweitert werden.    |
| SPX \_ rxpktsize   | INT  | Mediengröße auf maximal 1466 | Legt die maximale Größe des Empfangs Datagramms fest. Diese Größe enthält nicht den SPX-Header oder beliebige Medien Header, die ebenfalls verwendet werden können. Kann auf die Mediengröße erweitert werden. |
| SPX- \_ txmediasize | INT  | Primäres Board                   | Gibt die Größe des Sende Mediums minus SPX und die Medien Header zurück. Dadurch wird eine obere Grenze für die Größe des Nachrichten Segmentierungs Pakets festgelegt.                                       |
| SPX- \_ rxmediasize | INT  | Primäres Board                   | Gibt die Größe des Empfangs Mediums minus SPX und die Medien Header zurück. Dadurch wird eine obere Grenze für die Empfangs Paketgröße festgelegt.                                                 |
| SPX- \_ rawspx      | Bool | aus                             | Wenn festgelegt, wird der IPX/SPX-Protokoll Header mit den Daten übermittelt.                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Die **nsproto- \_ IPX** -Socketoptionen und die von diesen Socketoptionen verwendeten Strukturen werden in der Header Datei " *wsnwlink. h* " definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wsnwlink. h</dt> </dl> |



 

 




