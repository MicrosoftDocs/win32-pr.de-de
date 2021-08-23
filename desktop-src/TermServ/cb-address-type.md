---
title: CB_ADDRESS_TYPE -Enumeration (Cbclient.h)
description: Gibt den Adresstyp an.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- CB_ADDRESS_TYPE enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50903baa9fe85685ef3390ee3d545dd7defff5288d0960d6a2d7ec6ebe2276ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001698"
---
# <a name="cb_address_type-enumeration"></a>CB \_ ADDRESS \_ TYPE-Enumeration

Gibt den Adresstyp an.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB \_ ADDR \_ UNDEFINED**
</dt> <dd>

Der Adresstyp ist nicht definiert.

</dd> <dt>

<span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB \_ ADDR \_ IPv4**
</dt> <dd>

Die Adresse ist eine IPv4-Adresse.

</dd> <dt>

<span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB \_ ADDR \_ IPv6**
</dt> <dd>

Die Adresse ist eine IPv6-Adresse.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



 

 





