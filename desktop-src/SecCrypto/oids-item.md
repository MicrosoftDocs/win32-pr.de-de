---
description: Ruft ein Oid-Objekt aus der Auflistung ab. Dies ist die Standard Eigenschaft.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: OIDs. Item (Eigenschaft)
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
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360306"
---
# <a name="oidsitem-property"></a>OIDs. Item (Eigenschaft)

\[Die **Item** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**OidCollection-Klasse**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Item** -Eigenschaft ruft ein [**OID**](oid.md) -Objekt aus der Auflistung ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Das [**OID**](oid.md) -Objekt am angegebenen Index oder das **OID** -Objekt mit dem angegebenen gepunkteten Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**OIDs**](oids.md)
</dt> </dl>

 

 
