---
description: Ruft das Signer-Objekt ab, das den indizierten Signierer darstellt.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Signers.Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33630586282b745da94a442c13a0e85574c5f2e06fc04ab909e4ebf59fc2707b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898407"
---
# <a name="signersitem-property"></a>Signers.Item-Eigenschaft

\[Die **Item-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten. Weitere Informationen finden Sie in der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Item-Eigenschaft** ruft das [**Signer-Objekt**](signer.md) ab, das den indizierten Signierer darstellt. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Das [**Signer-Objekt,**](signer.md) das den indizierten Signierer darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Unterzeichner**](signers.md)
</dt> </dl>

 

 
