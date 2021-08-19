---
description: Gibt den verwendeten Codierungstyp an.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: CAPICOM_ENCODING_TYPE -Enumeration (Capicom.h)
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
ms.openlocfilehash: 1ec9a9ea1de4e3f501c94394ec9038d39c9b881c1e2bb1f41322d4f08c2db922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772485"
---
# <a name="capicom_encoding_type-enumeration"></a>CAPICOM \_ ENCODING \_ TYPE-Enumeration

Der **CAPICOM \_ ENCODING \_ TYPE-Enumerationstyp** gibt den verwendeten Codierungstyp an.

## <a name="members"></a>Member



| Member                      | Beschreibung                                                                                                                                                                                 | Wert      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ ENCODE \_ ANY**    | Daten werden als Base64-codierte Zeichenfolge oder als reine binäre Sequenz gespeichert. Dieser Codierungstyp wird nur für Eingabedaten verwendet, die einen unbekannten Codierungstyp haben. Eingeführt in CAPICOM 2.0.<br/> | 0xffffffff |
| **\_CAPICOM-CODIERUNG \_ BASE64** | Daten werden als Base64-codierte Zeichenfolge gespeichert.<br/>                                                                                                                                        | 0          |
| **CAPICOM \_ ENCODE \_ BINARY** | Daten werden als reine binäre Sequenz gespeichert.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Hinweise

Dieser Enumerationstyp wird von den folgenden CAPICOM-Methoden und -Eigenschaften verwendet:

-   [**Certificate.Export-Methode**](certificate-export.md)
-   [**EncodedData.Value-Eigenschaft**](encodeddata-value.md)
-   [**EncryptedData.Encrypt-Methode**](encrypteddata-encrypt.md)
-   [**EnvelopedData.Encrypt-Methode**](envelopeddata-encrypt.md)
-   [**ExtendedProperty.Value-Eigenschaft**](extendedproperty-value.md)
-   [**SignedData.Sign-Methode**](signeddata-sign.md)
-   [**SignedData.CoSign-Methode**](signeddata-cosign.md)
-   [**Store. Exportmethode**](store-export.md)
-   [**Utilities.GetRandom-Methode**](utilities-getrandom.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




