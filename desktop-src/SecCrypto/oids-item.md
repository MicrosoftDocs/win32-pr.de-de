---
description: Ruft ein OID-Objekt aus der Auflistung ab. Dies ist die Standardeigenschaft.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: OIDs.Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 94d4cad88ab0a41d9293407166993ec7d967d6c1caeca13a6fe6ea84005cbb2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979526"
---
# <a name="oidsitem-property"></a>OIDs.Item-Eigenschaft

\[Die **Item-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Item-Eigenschaft** ruft ein [**OID-Objekt**](oid.md) aus der Auflistung ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Das [**OID-Objekt**](oid.md) am angegebenen Index oder das **OID-Objekt** mit dem angegebenen gepunkteten Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OIDs**](oids.md)
</dt> </dl>

 

 
