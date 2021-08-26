---
title: RAS-Dienstdatentypen (Ras.h)
description: Die folgenden Datentypen werden von der RAS-Dienst-API verwendet.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26df8b8336b9b96ec338a79ed846519fb8a0ca019e6dd5996b9ac17087faa371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028250"
---
# <a name="remote-access-service-data-types"></a>Datentypen des RAS-Diensts

Die folgenden Datentypen werden von der RAS-Dienst-API verwendet.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

Ein [**\_ in-Addr,**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) der eine IPv4-Adresse enthält.

> [!Note]  
> Wird in Windows Vista oder höher von Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Ein [**\_ In6-Addr,**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) der eine IPv6-Adresse enthält.

> [!Note]  
> Wird in Windows Vista oder höher von Windows.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Ras.h</dt> </dl> |



 

