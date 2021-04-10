---
description: Internet Schemas, die von WinHTTP unterstützt werden.
ms.assetid: 31e45879-807e-4dd5-9f99-94a46011e55e
title: INTERNET_SCHEME (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7b73dcc13b2623e3a6f28d2d49d1965464070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867792"
---
# <a name="internet_scheme"></a>Internet \_ Schema

Internet Schemas, die von WinHTTP unterstützt werden.

<dl> <dt>

<span id="INTERNET_SCHEME_HTTP"></span><span id="internet_scheme_http"></span>**Internet- \_ Schema \_ http**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Ein HTTP-Internet Schema.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_HTTPS"></span><span id="internet_scheme_https"></span>**Internet \_ Schema \_ https**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Ein HTTPS-Internet Schema (SSL).


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_FTP"></span><span id="internet_scheme_ftp"></span>**Internet- \_ Schema- \_ FTP**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Ein FTP-Internet Schema. Dieses Schema wird nur für die Verwendung in [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) und [**winhttpgetproxyforurlex**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)unterstützt.


</dt> </dl> </dd> <dt>

<span id="INTERNET_SCHEME_SOCKS"></span><span id="internet_scheme_socks"></span>**Internet- \_ Schema- \_ SOCKS**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Ein SOCKS-Internet-Schema. Dieses Schema wird nur für die Verwendung im [**\_ \_ Ergebnis \_ Eintrag des WinHTTP-Proxys**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)unterstützt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]<br/>   |
| Header<br/>                   | <dl> <dt>WinHTTP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eintrag für WinHTTP- \_ Proxy \_ Ergebnis \_**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> </dl>

 

 




