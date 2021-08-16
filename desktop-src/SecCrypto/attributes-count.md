---
description: Ruft die Anzahl der Attribute-Objekte in der Auflistung ab.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attributes.Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d7b1f2213fc6de3ec08a9c9b568222f5dd54a6de6f9bdb3adb27e052e8c088e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773505"
---
# <a name="attributescount-property"></a>Attributes.Count-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**CryptographicAttributeObjectCollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography-Namespace.**](/previous-versions/windows/)\]

Die **Count-Eigenschaft** ruft die Anzahl der [**Attribute-Objekte**](attribute.md) in der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**Attribute-Objekte**](attribute.md) in der Auflistung. Jedes **Attributobjekt** stellt ein einzelnes Attribut in der Auflistung dar.

## <a name="remarks"></a>Hinweise

Die **Count-Eigenschaft** kann verwendet werden, um das letzte [**Attribute-Objekt**](attribute.md) in der Auflistung anzugeben, wenn ein bestimmtes **Attributobjekt** mithilfe der [**Attributes.Item-Eigenschaft**](attributes-item.md) abgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 
