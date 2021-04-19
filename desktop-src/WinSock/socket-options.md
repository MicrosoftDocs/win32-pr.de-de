---
description: Navigationsseite für Socketoptionen für Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Socketoptionen
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348994"
---
# <a name="socket-options"></a>Socketoptionen

In diesem Abschnitt werden die Winsock-Socketoptionen für verschiedene Editionen von Windows-Betriebssystemen beschrieben. Verwenden Sie die Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , um die Socketoptionen zu erhalten und festzulegen. Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

Einige Socketoptionen erfordern eine ausführlichere Erläuterung, als diese Tabellen vermitteln können. Diese Optionen enthalten Links zu weiteren Seiten.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**ipproto \_ -IP**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf IPv4-Ebene anwendbar sind. Weitere Informationen finden Sie unter [**ipproto \_ IP Socket Options**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**Ipproto \_ IPv6**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf IPv6-Ebene anwendbar sind. Weitere Informationen finden Sie unter [**ipproto \_ IPv6-Socketoptionen**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**ipproto \_ RM**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf zuverlässiger Multicast Ebene anwendbar sind. Weitere Informationen finden Sie unter [**ipproto \_ RM Socket Options**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**ipproto- \_ TCP**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf TCP-Ebene anwendbar sind. Weitere Informationen finden Sie unter [**ipproto \_ TCP Socket Options**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**ipproto- \_ UDP**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf UDP-Ebene anwendbar sind. Weitere Informationen finden Sie unter [**ipproto \_ UDP Socket Options**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**nsproto- \_ IPX**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf IPX-Ebene anwendbar sind. Weitere Informationen finden [**Sie unter nsproto \_ IPX Socket Options**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**Sol \_ AppleTalk**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf der AppleTalk-Ebene anwendbar sind. Weitere Informationen finden Sie in den [**Optionen für den Sol \_ AppleTalk-Socket**](sol-appletalk-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**Sol- \_ irilmp**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf der Protokollebene der Infrarot-Verbindungs Verwaltung anwendbar sind Weitere Informationen finden Sie unter den [**Optionen für den Sol- \_ irilmp-Socket**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**Sol- \_ Socket**
</dt> <dd> <dl> <dt>



Socketoptionen, die auf Socketebene anwendbar sind. Weitere Informationen finden Sie unter den [**Optionen für den Sol- \_ socketsocket**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle \_ \* Socketoptionen gelten gleichermaßen für IPv4 und IPv6 (mit Ausnahme von \_ Broadcast, da Broadcast nicht in IPv6 implementiert ist).

 

 



