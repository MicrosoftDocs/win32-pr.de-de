---
description: Ruft ein -Objekt aus der Recipients-Auflistung ab.
ms.assetid: 03600d4a-5fd4-45c7-ae91-efdc26c084ee
title: Recipients.Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 82a9e45ee82c42f659d6fa9e60f0b96122ee8d0f701d2d039df6ce995d1c778a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900797"
---
# <a name="recipientsitem-property"></a>Recipients.Item-Eigenschaft

\[Die **Item-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**CmsRecipientCollection-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Item-Eigenschaft** ruft ein Objekt aus der [**Recipients-Auflistung**](recipients.md) ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
Recipients.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variante, die das indizierte Element in der [**Empfängerauflistung**](recipients.md) darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Empfänger**](recipients.md)
</dt> </dl>

 

 
