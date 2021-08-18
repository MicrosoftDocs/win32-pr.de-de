---
title: Remotedesktopdienste API-Strukturen
description: Listet Strukturen auf, die mit der Remotedesktopdienste-API verwendet werden.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000100"
---
# <a name="remote-desktop-services-api-structures"></a>Remotedesktopdienste API-Strukturen

Die folgenden Strukturen werden mit der Remotedesktopdienste-API verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**\_KANAL-DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Enthält den Namen und die Optionen eines virtuellen Remotedesktopdienste Kanals.

</dd> <dt>

[**\_ \_ KANALEINSTIEGSPUNKTE**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Enthält Zeiger auf die Funktionen, die von einer clientseitigen DLL für den Zugriff auf virtuelle Kanäle aufgerufen werden.

</dd> <dt>

[**\_CHANNEL-PDU-HEADER \_**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Enthält Informationen zu einem Datenblock, der vom Serverende eines virtuellen Kanals empfangen wird.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Enthält Informationen zu einem bestimmten Remotedesktopdienste-Schlüsselpaket.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Enthält Informationen zu einem Remotedesktopverbindung Client (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Enthält Informationen zu einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Enthält Informationen zu einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Enthält eine [**WTSINFOEX \_ LEVEL-Union,**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) die erweiterte Informationen zu einer Remotedesktopdienste enthält.

</dd> <dt>

[**WTSINFOEX \_ LEVEL1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Enthält erweiterte Informationen zu einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Enthält Informationen zu einem Remotedesktopdienste Listener.

</dd> <dt>

[**WTSSBX-IP-ADRESSE \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Enthält Informationen zur IP-Adresse einer Netzwerkressource.

</dd> <dt>

[**WTSSBX \_ MACHINE \_ CONNECT \_ INFO**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Enthält Informationen zu einem Computer, der Remoteverbindungen akzeptiert.

</dd> <dt>

[**\_WTSSBX-COMPUTERINFORMATIONEN \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Enthält Informationen zu einem Computer und seinem aktuellen Zustand.

</dd> <dt>

[**WTSSBX-SITZUNGSINFORMATIONEN \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Enthält Informationen zu Sitzungen, die für Remotedesktopverbindung Broker (RD-Verbindungsbroker) verfügbar sind.

</dd> <dt>

[**\_WTSSESSION-BENACHRICHTIGUNG**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Stellt Informationen zur Sitzungsänderungsbenachrichtigung zur Verfügung. Ein Dienst empfängt diese Struktur in seiner [*HandlerEx-Funktion*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) als Reaktion auf ein Sitzungsänderungsereignis.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Enthält Konfigurationsinformationen für einen Benutzer auf einem Domänencontroller oder Remotedesktop-Sitzungshost -Server (RD-Sitzungshost Server).

</dd> <dt>

[**\_WTS \_CLIENTADRESSE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Enthält die Clientnetzwerkadresse einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**\_WTS \_CLIENTANZEIGE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Enthält Informationen zur Anzeige eines Remotedesktopverbindung -Clients (RDC).

</dd> <dt>

[**\_WTS \_PROZESSINFORMATIONEN**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Enthält Informationen zu einem Prozess, der auf einem RD-Sitzungshost wird.

</dd> <dt>

[**\_WTS PROZESSINFORMATIONEN \_ \_ ( EX)**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Enthält erweiterte Informationen zu einem Prozess, der auf einem RD-Sitzungshost wird.

</dd> <dt>

[**\_WTS \_PRODUKTINFORMATIONEN**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Die Details der Produktlizenz, die zum Herstellen einer Verbindung mit einem Terminalserver erforderlich ist.

</dd> <dt>

[**\_WTS \_SERVERINFORMATIONEN**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Enthält Informationen zu einem bestimmten Remotedesktopdienste Server.

</dd> <dt>

[**\_WTS \_SITZUNGSADRESSE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Enthält die virtuelle IP-Adresse, die einer Sitzung zugewiesen ist.

</dd> <dt>

[**\_WTS \_SITZUNGSINFORMATIONEN**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Enthält Informationen zu einer Clientsitzung auf einem RD-Sitzungshost Server.

</dd> <dt>

[**\_WTS \_SITZUNGSINFORMATIONEN \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Enthält erweiterte Informationen zu einer Clientsitzung auf einem RD-Sitzungshost- oder Remotedesktop Virtualization Host-Server (RD-Virtualisierungshost).

</dd> </dl>

 

 