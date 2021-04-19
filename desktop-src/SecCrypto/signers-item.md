---
description: Ruft das Signatur Geber Objekt ab, das den indizierten Signatur Geber darstellt.
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: Signers. Item (Eigenschaft)
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
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362169"
---
# <a name="signersitem-property"></a>Signers. Item (Eigenschaft)

\[Die **Item** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen eine Auflistung von CmsSigner-Objekten. Weitere Informationen finden Sie unter der [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Item** -Eigenschaft ruft das [**Signatur**](signer.md) Geber Objekt ab, das den indizierten Signatur Geber darstellt. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Das [**Signatur**](signer.md) Geber Objekt, das den indizierten Signatur Geber darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signatur Geber**](signers.md)
</dt> </dl>

 

 
