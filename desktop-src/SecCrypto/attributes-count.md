---
description: Ruft die Anzahl der Attribut Objekte in der Auflistung ab.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attribute. Count-Eigenschaft
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
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361542"
---
# <a name="attributescount-property"></a>Attribute. Count-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**cryptographitortributeobjectcollection-Klasse**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography**](/previous-versions/windows/) -Namespace.\]

Die **count** -Eigenschaft ruft die Anzahl der [**Attribut**](attribute.md) Objekte in der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**Attribut**](attribute.md) Objekte in der Auflistung. Jedes **Attribut** Objekt stellt ein einzelnes Attribut in der Auflistung dar.

## <a name="remarks"></a>Bemerkungen

Die **count** -Eigenschaft kann verwendet werden, um das letzte [**Attribut**](attribute.md) Objekt in der Auflistung anzugeben, wenn ein bestimmtes **Attribut** Objekt mithilfe der [**Attribute. Item**](attributes-item.md) -Eigenschaft abgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 
