---
description: Gibt den verwendeten Codierungstyp an.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: CAPICOM_ENCODING_TYPE-Enumeration (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356054"
---
# <a name="capicom_encoding_type-enumeration"></a>CAPICOM \_ Encoding \_ Type-Enumeration

Der **CAPICOM- \_ Codierungstyp \_** Enumerationstyp gibt den verwendeten Codierungstyp an.

## <a name="members"></a>Member



| Member                      | BESCHREIBUNG                                                                                                                                                                                 | Wert      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ Codieren \_ Any**    | Daten werden als Base64-codierte Zeichenfolge oder reine binäre Sequenz gespeichert. Dieser Codierungstyp wird nur für Eingabedaten verwendet, die einen unbekannten Codierungstyp aufweisen. Eingeführt in CAPICOM 2,0.<br/> | 0xFFFFFFFF |
| **CAPICOM \_ Codieren \_ Base64** | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                        | 0          |
| **CAPICOM- \_ Codierung ( \_ Binär)** | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Bemerkungen

Dieser Enumerationstyp wird von den folgenden CAPICOM-Methoden und-Eigenschaften verwendet:

-   [**Certificate. Export**](certificate-export.md) -Methode
-   [**Encoddata. Value**](encodeddata-value.md) -Eigenschaft
-   [**Verschlüsselteddata. verschlüsseln**](encrypteddata-encrypt.md) -Methode
-   [**EnvelopedData. verschlüsseln**](envelopeddata-encrypt.md) -Methode
-   [**ExtendedProperty. Value**](extendedproperty-value.md) -Eigenschaft
-   [**SignedData. Sign**](signeddata-sign.md) -Methode
-   [**SignedData. cosign**](signeddata-cosign.md) -Methode
-   [**Store. Export**](store-export.md) -Methode
-   [**Utilities. getrandom**](utilities-getrandom.md) -Methode

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




