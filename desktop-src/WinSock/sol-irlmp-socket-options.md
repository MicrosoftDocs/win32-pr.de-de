---
description: In der folgenden Tabelle werden \_ SOL-IRLMP-Socketoptionen beschrieben, die für Sockets gelten, die für die adressfamilie Infrared Data Association (IrDA) \_ (AF IRDA) und das InfraRed Link Management Protocol (IRLMP) erstellt wurden.
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: SOL_IRLMP Socketoptionen (Af \_ irda.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2be68bc658cd7d55ff72a77b6ec87568c37d6d786d0a5e654e9276378b837c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860730"
---
# <a name="sol_irlmp-socket-options"></a>SOL \_ IRLMP-Socketoptionen

In der folgenden Tabelle werden **\_ SOL-IRLMP-Socketoptionen** beschrieben, die für Sockets gelten, die für die adressfamilie Infrared Data Association (IrDA) \_ (AF IRDA) und das InfraRed Link Management Protocol (IRLMP) erstellt wurden. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**SOL \_ IRLMP-Socketoptionen**</dt> <dd> <dl> <dt> 

| Option                 | Herunterladen | Set | Optval-Typ     | BESCHREIBUNG                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| \_ \_ IRLMP-ERMITTLUNGSMODUS |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | Ja |     | **DEVICELIST**  | Gibt eine Liste der IrDA-Geräte-IDs für IR-fähige Geräte innerhalb des Bereichs zurück. |
| \_EXKLUSIVER \_ IRLMP-MODUS |     |     | DWORD (boolesch) | Legt den Socket so fest, dass die TinyTP-Ebene umgangen wird, um direkt mit IrLMP zu kommunizieren. |
| IRLMP– \_ \_ IAS-ABFRAGE      | Ja |     | **IAS \_ QUERY**  | Fragt IAS für einen bestimmten Dienst- und Klassennamen nach seinen Attributen ab.      |
| IRLMP \_ IAS \_ SET        |     | Ja | **IAS \_ SET**    | Legt einen Attributwert für einen angegebenen Klassennamen und ein Attribut in IAS fest. |
| \_IRLMP-IRLPT-MODUS \_     |     | Ja | DWORD (boolesch) | Ermöglicht die Kommunikation mit IR-fähigen Druckern.                        |
| \_IRLMP-PARAMETER      |     |     |                 |                                                                        |
| IRLMP \_ SEND \_ PDU \_ LEN  | Ja |     | DWORD           | Ruft die maximale PDU-Länge ab, die für die Verwendung von IRLMP \_ 9WIRE MODE erforderlich \_ ist.   |
| IRLMP \_ \_ SHARP-MODUS     |     | Ja |                 |                                                                        |
| IRLMP \_ \_ TINYTP-MODUS    |     | Ja |                 |                                                                        |
| IRLMP \_ \_ 9WIRE-MODUS     | Ja | Ja | DWORD (boolesch) | Versetzt den IrDA-Socket in den IrCOMM-Modus.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Windows Unterstützung für \_ SOL-IRLMP-Optionen**</dt> <dd> <dl> <dt> 

| Option                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows Me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| \_ \_ IRLMP-ERMITTLUNGSMODUS<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_EXKLUSIVER \_ IRLMP-MODUS<br/> |           |                     |               |                     |            |              |                        |                |
| IRLMP– \_ \_ IAS-ABFRAGE<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IAS \_ SET<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_IRLMP-IRLPT-MODUS \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| \_IRLMP-PARAMETER<br/>      |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ SEND \_ PDU \_ LEN<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| IRLMP \_ \_ SHARP-MODUS<br/>     |           |                     |               |                     |            |              |                        |                |
| IRLMP \_ \_ TINYTP-MODUS<br/>    |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ \_ 9WIRE-MODUS<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ SOL-IRLMP-Socketoptionen** und die von diesen Socketoptionen verwendeten Strukturen werden in der *Af \_ irda.h-Headerdatei* definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Af \_ irda.h</dt> </dl> |



 

 




