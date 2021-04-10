---
title: RAS-Dienst Datentypen (RAS. h)
description: Die folgenden Datentypen werden von der RAS-Dienst-API verwendet.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956434"
---
# <a name="remote-access-service-data-types"></a>RAS-Dienst Datentypen

Die folgenden Datentypen werden von der RAS-Dienst-API verwendet.


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

**RASIPV4ADDR**
</dt> <dd>

Ein [**in \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) , das eine IPv4-Adresse enthält.

> [!Note]  
> Unterstützt in Windows Vista oder höheren Versionen von Windows.

 

</dd> <dt>

**RASIPV6ADDR**
</dt> <dd>

Eine [**IN6 \_ addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) , die eine IPv6-Adresse enthält.

> [!Note]  
> Unterstützt in Windows Vista oder höheren Versionen von Windows.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



 

