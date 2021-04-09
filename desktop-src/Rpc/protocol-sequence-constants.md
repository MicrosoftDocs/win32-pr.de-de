---
title: Protokoll Sequenz Konstanten
description: Microsoft RPC unterstützt die folgenden Protokoll Sequenzen.
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e2dd716cdd969040f5315ef05200912acc54878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039436"
---
# <a name="protocol-sequence-constants"></a>Protokoll Sequenz Konstanten

Microsoft RPC unterstützt die folgenden Protokoll Sequenzen.



| Konstante/Wert                                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ NB \_ TCP**</dt> <dt>-Verbindungs orientiertes NetBIOS über Transmission Control Protocol (TCP)</dt> </dl>          | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ NB \_ IPX**</dt> <dt>-Verbindungs orientiertes NetBIOS über Internet Paket Austausch (IPX)</dt> </dl>               | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ NB \_ NB**</dt> <dt>Verbindungs orientierte NetBIOS-erweiterte Benutzeroberfläche (NetBEUI)</dt> </dl>                    | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**ncacn \_ IP \_ TCP**</dt> <dt>-Verbindungs orientiertes Übertragungs Steuerungs Protokoll/Internet Protokoll (TCP/IP)</dt> </dl>  | Nur Client: MS-DOS, Windows 3. *x*, und Apple Macintosh-Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>**ncacn \_ NP**</dt> <dt>-Verbindungs orientierte benannte Pipes</dt> </dl>                                                            | Nur Client: MS-DOS, Windows 3. *x*, Windows 95 Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_**</dt> - <dt>Verbindungs orientierter sequenzierter Paket Austausch (SPX)</dt> </dl>                                     | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ NSP**</dt> <dt>-Verbindungs orientierter dnet-Transport</dt> </dl>                                    | Nur Client: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ beim \_ DSP**</dt> <dt>-Verbindungs orientierten AppleTalk DSP</dt> </dl>                                             | Client: Apple Macintosh-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>**ncacn \_ VNS- \_ spp**</dt> <dt>-Verbindungs orientierter, skalierbarer paralleler Verarbeitungs Transport (SPP)</dt> </dl>     | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ -IP- \_ UDP-**</dt> <dt>Datagramm (verbindungsloses) User Datagram Protocol/Internet Protocol (UDP/IP)</dt> </dl>   | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_ IPX**</dt> <dt>Datagram (verbindungslose) IPX</dt> </dl>                                                           | Nur Client: MS-DOS, Windows 3. *x* -Client und-Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ MQ**</dt> <dt>Datagram (verbindungslose) über den Microsoft Message Queue Server (MSMQ)</dt> </dl>                   | Nur Client: Windows Me/98/95 Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4,0 mit SP3 und höher<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**ncacn \_ http**</dt> <dt>-Verbindungs orientiertes TCP/IP mithilfe von Microsoft Internet Information Server als HTTP-Proxy</dt> </dl> | Nur Client: Windows Me/98/95 Client und Server: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> lokaler <dt>**Ncalrpc**</dt> - <dt>Prozedur Aufruf</dt> </dl>                                                                           | Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Bemerkungen

Der [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) -Transport unterstützt nur die RPC- \_ C- \_ authn- \_ Winnt-Authentifizierung. Weitere Informationen finden Sie unter [Sicherheit](security.md) und [Authentifizierung-Dienst Konstanten](authentication-service-constants.md).

Microsoft RPC unterstützt [**rpcbindingcopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) nur in Client Anwendungen, nicht in Server Anwendungen.

 

