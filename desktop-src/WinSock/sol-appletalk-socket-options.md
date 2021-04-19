---
description: In der folgenden Tabelle werden die \_ Optionen von Sol AppleTalk Socket beschrieben, die für Sockets gelten, die für die AppleTalk-Adressfamilie (AF \_ AppleTalk) erstellt wurden.
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: SOL_APPLETALK Socketoptionen (atalkwsh. h)
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
ms.openlocfilehash: 146cfa02706cc9a2669cf21ba6d9eac0ac74ee4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367775"
---
# <a name="sol_appletalk-socket-options"></a>Optionen für den Sol \_ AppleTalk-Socket

In der folgenden Tabelle werden die Optionen von **Sol \_ AppleTalk** Socket beschrieben, die für Sockets gelten, die für die AppleTalk-Adressfamilie (AF \_ AppleTalk) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Optionen für den Sol \_ AppleTalk-Socket**</dt> <dd> <dl> <dt> 

| Option                          | Herunterladen | Set | Optval-Typ                          | BESCHREIBUNG                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bestätigen Sie den \_ \_ Namen.               | ja |     | **WSH \_ NBP- \_ Tupel**                  | Bestätigt, dass ein bestimmter AppleTalk-Name an die angegebene Adresse gebunden ist.                                                                                                                                  |
| \_Name des deregiters \_            |     | ja | **WSH- \_ Register \_ Name**              | Hebt die Registrierung des Namens aus dem Netzwerk auf.                                                                                                                                                               |
| also \_ getlocalzones               | ja |     | **WSH- \_ \_ Lookupzonen**               | Gibt eine Liste der Zonen Namen zurück, die dem angegebenen Adapter Namen bekannt sind.                                                                                                                                        |
| SO \_ getmyzone                   | ja |     | Char \[\]                            | Gibt die Standard Zone im Netzwerk zurück.                                                                                                                                                             |
| " \_ getnetinfo"                  | ja |     | **WSH- \_ Suche \_ Netdef \_ auf \_ Adapter** | Gibt die Seeding Werte für das Netzwerk und die Standard Zone zurück. Der *optlen* -Parameter muss mindestens ein Byte betragen, das größer als die Größe der **WSH- \_ Suche \_ Netdef \_ in der \_ Adapter** Struktur ist.  |
| SO \_ getzonelist                 | ja |     | **WSH- \_ \_ Lookupzonen**               | Gibt Zonen Namen aus der Liste der Internet Zonen zurück. Der *optlen* -Parameter muss mindestens ein Byte betragen, das größer als die Größe der **WSH- \_ Lookupzonen \_** -Struktur ist.                                       |
| \_Suche nach \_ MyZone              | ja |     |                                      | Identisch mit " \_ getmyzone"                                                                                                                                                                                |
| \_Such \_ Name                | ja |     | **WSH- \_ Such \_ Name**                | Sucht einen angegebenen NBP-Namen und gibt die übereinstimmenden Tupel namens und NBP-Informationen zurück. Der *optlen* -Parameter muss mindestens ein Byte betragen, das größer als die Größe der WSH- \_ Such \_ namens Struktur ist. |
| \_Suchen Sie daher \_ Netdef \_ auf dem \_ Adapter. | ja |     | **WSH- \_ Suche \_ Netdef \_ auf \_ Adapter** | Identisch mit " \_ getnetinfo".                                                                                                                                                                              |
| \_Such \_ Zonen               | ja |     | **WSH- \_ \_ Lookupzonen**               | Identisch mit " \_ getzonelist".                                                                                                                                                                             |
| \_Such \_ Zonen auf dem \_ \_ Adapter  | ja |     | **WSH- \_ \_ Lookupzonen**               | Identisch mit " \_ getlocalzones".                                                                                                                                                                           |
| \_PAP \_ get \_ Server \_ Status    | ja |     | **WSH \_ PAP \_ - \_ Server \_ Status**    | Gibt den PAP-Status von einem bestimmten Server zurück.                                                                                                                                                           |
| \_PAP \_ Prim \_ Lesevorgang            |     | ja | Char \[\]                            | Dieser Befehl PRIMES einen Lesevorgang für eine PAP-Verbindung, damit der Absender mit dem Senden der Daten beginnen kann.                                                                                                                 |
| der \_ \_ \_ Server Status von \_ PAP    |     | ja | Char \[\]                            | Legt den Status fest, der gesendet werden soll, wenn ein anderer Client den Status anfordert                                                                                                                                     |
| \_Register \_ Name              |     | ja | **WSH- \_ Register \_ Name**              | Registriert den angegebenen Namen im AppleTalk-Netzwerk.                                                                                                                                                    |
| Entfernen Sie den \_ \_ Namen.                |     | ja | **WSH- \_ Register \_ Name**              | Identisch mit dem \_ Namen des deregitennamens \_                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows-Unterstützung für Sol \_ AppleTalk-Optionen**</dt> <dd> <dl> <dt> 

| Option                          | Windows Vista und höher | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9X/ME |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| bestätigen Sie den \_ \_ Namen.               |                         | x                   | x          | x            | x           |               |
| \_Name des deregiters \_            |                         | x                   | x          | x            | x           |               |
| also \_ getlocalzones               |                         | x                   | x          | x            | x           |               |
| SO \_ getmyzone                   |                         | x                   | x          | x            | x           |               |
| " \_ getnetinfo"                  |                         | x                   | x          | x            | x           |               |
| SO \_ getzonelist                 |                         | x                   | x          | x            | x           |               |
| \_Suche nach \_ MyZone              |                         | x                   | x          | x            | x           |               |
| \_Such \_ Name                |                         | x                   | x          | x            | x           |               |
| \_Suchen Sie daher \_ Netdef \_ auf dem \_ Adapter. |                         | x                   | x          | x            | x           |               |
| \_Such \_ Zonen               |                         | x                   | x          | x            | x           |               |
| \_Such \_ Zonen auf dem \_ \_ Adapter  |                         | x                   | x          | x            | x           |               |
| \_PAP \_ get \_ Server \_ Status    |                         | x                   | x          | x            | x           |               |
| \_PAP \_ Prim \_ Lesevorgang            |                         | x                   | x          | x            | x           |               |
| der \_ \_ \_ Server Status von \_ PAP    |                         | x                   | x          | x            | x           |               |
| \_Register \_ Name              |                         | x                   | x          | x            | x           |               |
| Entfernen Sie den \_ \_ Namen.                |                         | x                   | x          | x            | x           |               |



 

Die Optionen " **Sol \_ AppleTalk** " werden nur auf den Serverversionen von Windows 2000 und Windows NT 4,0 unterstützt.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Optionen für den **Sol \_ AppleTalk** -Socket und die von diesen Socketoptionen verwendeten Strukturen werden in der Datei " *atalkwsh. h* " definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Atalkwsh. h</dt> </dl> |



 

 




