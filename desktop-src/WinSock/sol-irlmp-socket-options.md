---
description: In der folgenden Tabelle werden die Optionen für die \_ Optionen von Sol-unlmp beschrieben, die für Sockets gelten, die für die UNDA-Adressfamilie (Infrarot Data Association) \_ und für das Infrarot Link Management Protocol (unlmp) erstellt wurden.
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: SOL_IRLMP Socketoptionen (AF \_ irren. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090193aec00eaebd87494afefbafc7b1450fdb44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356037"
---
# <a name="sol_irlmp-socket-options"></a>Optionen für das Sol- \_ irilmp-Socket

In der folgenden Tabelle werden die Optionen für die Optionen von **Sol- \_ unlmp** beschrieben, die für Sockets gelten, die für die UNDA-Adressfamilie (Infrarot Data Association) \_ und für das Infrarot Link Management Protocol (unlmp) erstellt wurden. Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**Optionen für das Sol- \_ irilmp-Socket**</dt> <dd> <dl> <dt> 

| Option                 | Herunterladen | Set | Optval-Typ     | BESCHREIBUNG                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| unlmp-Ermittlungs \_ \_ Modus |     |     |                 |                                                                        |
| unlmp- \_ enumdevices     | ja |     | **DEVICELIST**  | Gibt eine Liste von UNDA-Geräte-IDs für IR-fähige Geräte innerhalb des Bereichs zurück. |
| unlmp- \_ exklusiver \_ Modus |     |     | DWORD (Boolean) | Legt den Socket für die Umgehung der tinytp-Schicht für die direkte Kommunikation mit "unlmp" fest |
| unlmp \_ IAS- \_ Abfrage      | ja |     | **IAS- \_ Abfrage**  | Fragt IAS nach einem angegebenen Dienst-und Klassennamen für seine Attribute ab.      |
| unlmp \_ IAS- \_ Satz        |     | ja | **IAS- \_ Satz**    | Legt einen Attribut Wert für einen angegebenen Klassennamen und ein Attribut in IAS fest. |
| unlmp- \_ Modus "unlpt" \_     |     | ja | DWORD (Boolean) | Ermöglicht die Kommunikation mit IR-fähigen Druckern.                        |
| Parameter für "unlmp" \_      |     |     |                 |                                                                        |
| unlmp \_ Send \_ PDU \_ len  | ja |     | DWORD           | Ruft die maximale PDU-Länge ab, die für die Verwendung des unlmp \_ 9wire-Modus erforderlich ist \_ .   |
| unlmp- \_ Sharp- \_ Modus     |     | ja |                 |                                                                        |
| unlmp- \_ tinytp- \_ Modus    |     | ja |                 |                                                                        |
| Modus "unlmp \_ 9wire" \_     | ja | ja | DWORD (Boolean) | Versetzt den irren-Socket in den uncomm-Modus.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Windows-Unterstützung für Sol- \_ Optionen**</dt> <dd> <dl> <dt> 

| Option                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows Me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| unlmp-Ermittlungs \_ \_ Modus<br/> |           |                     |               |                     |            |              | x                      |                |
| unlmp- \_ enumdevices<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| unlmp- \_ exklusiver \_ Modus<br/> |           |                     |               |                     |            |              |                        |                |
| unlmp \_ IAS- \_ Abfrage<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| unlmp \_ IAS- \_ Satz<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| unlmp- \_ Modus "unlpt" \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| Parameter für "unlmp" \_<br/>      |           |                     |               |                     |            |              | x                      |                |
| unlmp \_ Send \_ PDU \_ len<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| unlmp- \_ Sharp- \_ Modus<br/>     |           |                     |               |                     |            |              |                        |                |
| unlmp- \_ tinytp- \_ Modus<br/>    |           |                     |               |                     |            |              | x                      |                |
| Modus "unlmp \_ 9wire" \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Optionen für den **Sol- \_ irilmp** -Socket und die von diesen Socketoptionen verwendeten Strukturen werden in der Header Datei " *AF \_ irren. h* " definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>AF \_ irren. h</dt> </dl> |



 

 




