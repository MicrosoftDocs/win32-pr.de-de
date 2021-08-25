---
description: Stellt einen Block von ASN.1-codierten Daten dar.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: EncodedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ba17056aaf2b038abb519c1eff230f6cccb396edea1ee9c1f96077d572e63fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874860"
---
# <a name="encodeddata-object"></a>EncodedData-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System.Security.Cryptography-Namespace.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **EncodedData-Objekt** stellt einen Block von ASN.1-codierten Daten dar.

## <a name="when-to-use"></a>Verwendung

Das **EncodedData-Objekt** wird von mehreren CAPICOM-Objekteigenschaften zurückgegeben. Wenn dieses Objekt zurückgegeben wird, wird es verwendet, um die folgenden Aufgaben auszuführen:

-   Abrufen einer Zeichenfolgendarstellung der codierten Daten.
-   Abrufen des Decoderobjekts, sofern vorhanden, das den codierten Daten zugeordnet ist.
-   Bestimmen Sie den Typ der codierten Daten.

## <a name="members"></a>Member

Das **EncodedData-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **EncodedData-Objekt** verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**Decoder**](encodeddata-decoder.md) | Erhält ein Decoderobjekt, sofern vorhanden.<br/>             |
| [**Format**](encodeddata-format.md)   | Gibt eine Zeichenfolgendarstellung der codierten Daten zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **EncodedData-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                      | Zugriffstyp          | BESCHREIBUNG                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**Wert**](encodeddata-value.md)<br/> | Schreibgeschützt<br/> | Ruft die codierten Daten ab. Dies ist die Standardeigenschaft.<br/> |



 

## <a name="remarks"></a>Hinweise

Der einzige unterstützte Typ von codierten Daten ist [**CertificatePolicies.**](certificatepolicies.md)

Das **EncodedData-Objekt** kann nicht erstellt werden.

Die folgenden CAPICOM-Objekteigenschaften geben ein **EncodedData-Objekt** zurück:

-   **PublicKey.EncodedKey**
-   **PublicKey.EncodedParameters**
-   **Extension.EncodedData**
-   **Policy.EncodedData**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
