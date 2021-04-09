---
description: Stellt ein Handle für eine OCSP-Antwort dar, die einer Serverzertifikat Kette zugeordnet ist.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867415"
---
# <a name="hcert_server_ocsp_response"></a>hcert- \_ Server- \_ OCSP- \_ Antwort

Der Datentyp der **\_ \_ OCSP- \_ Antwort des hcert-Servers** stellt ein Handle für eine OCSP-Antwort dar, die einer Server Zertifikat Kette zugeordnet ist.

Dieser Typ wird von den folgenden APIs verwendet.

-   [**Certoptserverocspresponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [**Certadresssserverocspresponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [**Certcloseserverocspresponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [**Certgetserverocspresponsecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 




