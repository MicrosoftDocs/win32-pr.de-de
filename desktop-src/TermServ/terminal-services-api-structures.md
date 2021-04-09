---
title: Remotedesktopdienste API-Strukturen
description: Listet Strukturen auf, die mit der Remotedesktopdienste-API verwendet werden.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101690"
---
# <a name="remote-desktop-services-api-structures"></a>Remotedesktopdienste API-Strukturen

Die folgenden Strukturen werden mit der Remotedesktopdienste-API verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Channel \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Enthält den Namen und die Optionen eines Remotedesktopdienste virtuellen Kanals.

</dd> <dt>

[**Kanal \_ Einstiegs \_ Punkte**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Enthält Zeiger auf die Funktionen, die von einer Client seitigen dll aufgerufen werden, um auf virtuelle Kanäle zuzugreifen.

</dd> <dt>

[**Channel- \_ PDU- \_ Header**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Enthält Informationen zu einem Datenblock, der vom Server Ende eines virtuellen Kanals empfangen wird.

</dd> <dt>

[**Lschräypack**](lskeypack.md)
</dt> <dd>

Enthält Informationen zu einem bestimmten Remotedesktopdienste Licensing Key Pack.

</dd> <dt>

[**Lslicense**](lslicense.md)
</dt> <dd>

Enthält Informationen zu einer bestimmten Remotedesktopdienste Lizenz.

</dd> <dt>

[**WTSClient**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Enthält Informationen zu einem Remotedesktopverbindung-Client (RDC).

</dd> <dt>

[**WT configinfo**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Enthält Informationen zu einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**Wtsinfo**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Enthält Informationen zu einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**Wtsinfoex**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Enthält eine Union der [**wtsinfoex- \_ Ebene**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) , die erweiterte Informationen zu einer Remotedesktopdienste Sitzung enthält.

</dd> <dt>

[**Wtsinfoex \_ Level1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Enthält erweiterte Informationen zu einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**Wout-listenerconfig**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Enthält Informationen zu einem Remotedesktopdienste Listener.

</dd> <dt>

[**wtssbx \_ -IP- \_ Adresse**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Enthält Informationen über die IP-Adresse einer Netzwerkressource.

</dd> <dt>

[**wtssbx- \_ Computer \_ Verbindungs \_ Informationen**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Enthält Informationen zu einem Computer, der Remote Verbindungen akzeptiert.

</dd> <dt>

[**wtssbx- \_ Computer \_ Informationen**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Enthält Informationen über einen Computer und seinen aktuellen Zustand.

</dd> <dt>

[**wtssbx- \_ Sitzungs \_ Informationen**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Enthält Informationen zu Sitzungen, die für Remotedesktopverbindung Broker (RD-Verbindungsbroker) verfügbar sind.

</dd> <dt>

[**wtssession- \_ Benachrichtigung**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Enthält Informationen über die Sitzungs Änderungs Benachrichtigung. Ein Dienst empfängt diese Struktur in seiner [*handlerex*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Funktion als Reaktion auf ein Sitzungs Änderungs Ereignis.

</dd> <dt>

[**Wtsuserconfig**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Enthält Konfigurationsinformationen für einen Benutzer auf einem Domänen Controller oder Remotedesktop-Sitzungshost Server (RD-Sitzungshost).

</dd> <dt>

[**WTS- \_ Client \_ Adresse**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Enthält die Client Netzwerkadresse einer Remotedesktopdienste Sitzung.

</dd> <dt>

[**Anzeige des WTS- \_ Clients \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Enthält Informationen zur Anzeige eines-Remotedesktopverbindung (RDC)-Clients.

</dd> <dt>

[**Informationen zum WTS- \_ Prozess \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Enthält Informationen zu einem Prozess, der auf einem RD-Sitzungshost Server ausgeführt wird.

</dd> <dt>

[**Informationen zum WTS- \_ Prozess \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Enthält erweiterte Informationen zu einem Prozess, der auf einem RD-Sitzungshost Server ausgeführt wird.

</dd> <dt>

[**WTS- \_ Produkt \_ Informationen**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Die Details der Produktlizenz, die benötigt wird, um eine Verbindung mit einem Terminal Server herzustellen.

</dd> <dt>

[**Informationen zum WTS- \_ Server \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Enthält Informationen zu einem bestimmten Remotedesktopdienste Server.

</dd> <dt>

[**WTS- \_ Sitzungs \_ Adresse**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Enthält die virtuelle IP-Adresse, die einer Sitzung zugewiesen ist.

</dd> <dt>

[**Informationen zur WTS- \_ Sitzung \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Enthält Informationen über eine Client Sitzung auf einem RD-Sitzungshost-Server.

</dd> <dt>

[**Informationen zur WTS- \_ Sitzung \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Enthält erweiterte Informationen über eine Client Sitzung auf einem RD-Sitzungshost Server oder Remotedesktop-Virtualisierungshost-Server (RD-Virtualisierungshost).

</dd> </dl>

 

 