---
description: In der folgenden Tabelle werden SOL \_ APPLETALK-Socketoptionen beschrieben, die für Sockets gelten, die für die AppleTalk-Adressfamilie (AF \_ APPLETALK) erstellt wurden.
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: SOL_APPLETALK Socketoptionen (Atalkwsh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 5ea45b4007a3bd36d2cfbceda5b7ec4f2cff20d9bb2387fb2d184710a8a4492c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740007"
---
# <a name="sol_appletalk-socket-options"></a>SOL \_ APPLETALK Socket-Optionen

In der folgenden Tabelle werden **SOL \_ APPLETALK-Socketoptionen** beschrieben, die für Sockets gelten, die für die AppleTalk-Adressfamilie (AF \_ APPLETALK) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**SOL \_ APPLETALK Socket-Optionen**</dt> <dd> <dl> <dt> 

| Option                          | Herunterladen | Set | Optval-Typ                          | Beschreibung                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESTÄTIGEN SIE DEN \_ \_ NAMEN.               | Ja |     | **WSH \_ \_ NBP-TUPEL**                  | Bestätigt, dass ein angegebener AppleTalk-Name an die angegebene Adresse gebunden ist.                                                                                                                                  |
| SO \_ DEREGISTER \_ NAME            |     | Ja | **\_WSH-REGISTERNAME \_**              | Deregistrierung des Namens im Netzwerk.                                                                                                                                                               |
| ALSO \_ GETLOCALZONES               | Ja |     | **\_WSH-LOOKUPZONEN \_**               | Gibt eine Liste von Zonennamen zurück, die dem angegebenen Adapternamen bekannt sind.                                                                                                                                        |
| ALSO \_ GETMYZONE                   | Ja |     | Char \[\]                            | Gibt die Standardzone im Netzwerk zurück.                                                                                                                                                             |
| ALSO \_ GETNETINFO                  | Ja |     | **WSH \_ LOOKUP \_ NETDEF \_ ON \_ ADAPTER** | Gibt die Werte zurück, für die ein Seeding für das Netzwerk und die Standardzone verwendet wird. Der *optlen-Parameter* muss mindestens ein Byte größer als die **WSH \_ LOOKUP \_ NETDEF \_ ON \_ ADAPTER-Struktur** sein.  |
| ALSO \_ GETZONELIST                 | Ja |     | **\_WSH-LOOKUPZONEN \_**               | Gibt Zonennamen aus der Internetzonenliste zurück. Der *optlen-Parameter* muss mindestens ein Byte größer als die **WSH \_ LOOKUP \_ ZONES-Struktur** sein.                                       |
| ALSO \_ LOOKUP \_ MYZONE              | Ja |     |                                      | Identisch mit SO \_ GETMYZONE                                                                                                                                                                                |
| \_ \_ LOOKUPNAME                | Ja |     | **\_WSH-LOOKUPNAME \_**                | Sucht einen angegebenen NBP-Namen und gibt die übereinstimmenden Tupel namens und NBP-Informationen zurück. Der *optlen-Parameter* muss mindestens ein Byte größer als die WSH \_ LOOKUP \_ NAME-Struktur sein. |
| SUCHEN \_ SIE \_ ALSO NETDEF AUF \_ \_ ADAPTER. | Ja |     | **WSH \_ LOOKUP \_ NETDEF \_ ON \_ ADAPTER** | Identisch mit SO \_ GETNETINFO.                                                                                                                                                                              |
| SO \_ LOOKUP \_ ZONES               | Ja |     | **\_WSH-LOOKUPZONEN \_**               | Identisch mit SO \_ GETZONELIST.                                                                                                                                                                             |
| LOOKUP \_ ZONES ON ADAPTER (LOOKUPZONEN \_ AUF \_ \_ ADAPTER)  | Ja |     | **\_WSH-LOOKUPZONEN \_**               | Identisch mit SO \_ GETLOCALZONES.                                                                                                                                                                           |
| SO \_ \_ ERHALTEN SIE DEN \_ \_ SERVERSTATUS VON PAP    | Ja |     | **WSH \_ PAP \_ GET \_ SERVER \_ STATUS**    | Gibt den PAP-Status von einem bestimmten Server zurück.                                                                                                                                                           |
| SO \_ LESEN VON PAP \_ PRIME \_            |     | Ja | Char \[\]                            | Mit diesem Aufruf wird ein Lesevorgangs für eine PAP-Verbindung gestartet, damit der Absender mit dem Senden der Daten beginnen kann.                                                                                                                 |
| SO \_ WIRD DER SERVERSTATUS VON PAP \_ \_ \_ FESTGELEGT.    |     | Ja | Char \[\]                            | Legt den Status fest, der gesendet werden soll, wenn ein anderer Client den Status anfordert.                                                                                                                                     |
| ALSO \_ \_ REGISTERNAME              |     | Ja | **\_WSH-REGISTERNAME \_**              | Registriert den angegebenen Namen im AppleTalk-Netzwerk.                                                                                                                                                    |
| ENTFERNEN SIE ALSO \_ \_ NAME.                |     | Ja | **\_WSH-REGISTERNAME \_**              | Identisch mit SO \_ DEREGISTER \_ NAME                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows Unterstützung für SOL \_ APPLETALK-Optionen**</dt> <dd> <dl> <dt> 

| Option                          | Windows Vista und höher | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| BESTÄTIGEN SIE DEN \_ \_ NAMEN.               |                         | x                   | x          | x            | x           |               |
| SO \_ DEREGISTER \_ NAME            |                         | x                   | x          | x            | x           |               |
| ALSO \_ GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| SO \_ GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| SO \_ GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| SO \_ GETZONELIST                 |                         | x                   | x          | x            | x           |               |
| SUCHEN \_ SIE ALSO NACH \_ MYZONE.              |                         | x                   | x          | x            | x           |               |
| \_SUCHNAME \_                |                         | x                   | x          | x            | x           |               |
| SUCHEN \_ SIE ALSO \_ NETDEF AUF DEM \_ \_ ADAPTER. |                         | x                   | x          | x            | x           |               |
| SUCHEN \_ VON ZONEN \_               |                         | x                   | x          | x            | x           |               |
| SUCHEN \_ VON ZONEN AUF DEM \_ \_ \_ ADAPTER  |                         | x                   | x          | x            | x           |               |
| DAHER \_ ERHALTEN SIE DEN \_ \_ SERVERSTATUS VON \_ PAP.    |                         | x                   | x          | x            | x           |               |
| DAHER \_ LESEN VON PAP \_ PRIME \_            |                         | x                   | x          | x            | x           |               |
| DAHER \_ WIRD DER SERVERSTATUS VON PAP \_ \_ \_ FESTGELEGT.    |                         | x                   | x          | x            | x           |               |
| SO \_ REGISTRIEREN SIE DEN \_ NAMEN              |                         | x                   | x          | x            | x           |               |
| ENTFERNEN \_ SIE DAHER DEN \_ NAMEN.                |                         | x                   | x          | x            | x           |               |



 

Die **SOL \_ APPLETALK-Optionen** werden nur in den Serverversionen von Windows 2000 und Windows NT 4.0 unterstützt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die **SOL \_ APPLETALK-Socketoptionen** und die von diesen Socketoptionen verwendeten Strukturen werden in der *Headerdatei Atalkwsh.h* definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Atalkwsh.h</dt> </dl> |



 

 




