---
title: Protokollsequenzkonst constants
description: Microsoft RPC unterstützt die folgenden Protokollsequenzen.
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
ms.openlocfilehash: 72c28486bfa3981870ac331ae83f0cbb532bba4d27c44062ce902823e4e3c259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927132"
---
# <a name="protocol-sequence-constants"></a>Protokollsequenzkonst constants

Microsoft RPC unterstützt die folgenden Protokollsequenzen.



| Konstante/Wert                                                                                                                                                                                                                                                                                 | Beschreibung                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ nb \_ tcp**</dt> <dt>Connection-oriented NetBIOS over Transmission Control Protocol (TCP)</dt> </dl>          | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ nb \_ ipx**</dt> <dt>Connection-oriented NetBIOS over Internet Packet Exchange (IPX)</dt> </dl>               | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ nb \_ nb**</dt> <dt>Connection-oriented NetBIOS Enhanced Benutzeroberfläche (NetBEUI)</dt> </dl>                    | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**ncacn \_ ip \_ tcp**</dt> <dt>Connection-oriented Transmission Control Protocol/Internet Protocol (TCP/IP)</dt> </dl>  | Nur Client: MS-DOS, Windows 3. *x* und Apple Macintosh Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>**ncacn \_ np**</dt> <dt>Verbindungsorientierte Named Pipes</dt> </dl>                                                            | Nur Client: MS-DOS, Windows 3. *x*, Windows 95 Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ spx**</dt> <dt>Connection-oriented Sequenced Packet Exchange (SPX)</dt> </dl>                                     | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_ nsp**</dt> <dt>Verbindungsorientierter DECnet-Transport</dt> </dl>                                    | Nur Client: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ bei \_ dsp**</dt> <dt>Connection-oriented AppleTalk DSP</dt> </dl>                                             | Client: Apple Macintosh Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>**ncacn \_ vns \_ spp**</dt> <dt>Connection-oriented Vines scalable parallel processing (SPP)-Transport</dt> </dl>     | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**ncadg \_ ip \_ udp**</dt> <dt>Datagram (verbindungslos) User Datagram Protocol/Internet Protocol (UDP/IP)</dt> </dl>   | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_ ipx**</dt> <dt>Datagram (verbindungslos) IPX</dt> </dl>                                                           | Nur Client: MS-DOS, Windows 3. *x* Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ mq**</dt> <dt>Datagram (verbindungslos) über den Microsoft Message Queue Server (MSMQ)</dt> </dl>                   | Nur Client: Windows Me/98/95 Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4.0 mit SP3 und höher<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**ncacn \_ http**</dt> <dt>Connection-oriented TCP/IP using Microsoft Internet Information Server as HTTP proxy</dt> </dl> | Nur Client: Windows Me/98/95 Client and Server: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**Aufruf der lokalen ncalrpc-Prozedur**</dt> <dt></dt> </dl>                                                                           | Client und Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Hinweise

Der [**ncalrpc-Transport**](/windows/desktop/Midl/ncalrpc) unterstützt nur die RPC \_ C \_ AUTHN \_ WINNT-Authentifizierung. Weitere Informationen finden Sie unter [Security](security.md) and [Authentication-Service Constants](authentication-service-constants.md).

Microsoft RPC unterstützt [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) nur in Clientanwendungen, nicht in Serveranwendungen.

 

