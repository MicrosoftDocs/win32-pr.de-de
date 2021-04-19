---
description: Stellt einen Block von ASN. 1-codierten Daten dar.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Encoddata-Objekt
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
ms.openlocfilehash: d05fce31ad4ef08bf9f573c0158a683bdbeba739
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367130"
---
# <a name="encodeddata-object"></a>Encoddata-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**AsnEncodedData-Klasse**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) im [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **encoddata** -Objekt stellt einen Block von ASN. 1-codierten Daten dar.

## <a name="when-to-use"></a>Verwendung

Das **encoddata** -Objekt wird von mehreren CAPICOM-Objekteigenschaften zurückgegeben. Wenn Sie zurückgegeben wird, wird dieses Objekt verwendet, um die folgenden Aufgaben auszuführen:

-   Eine Zeichen folgen Darstellung der codierten Daten abrufen.
-   Rufen Sie ggf. das Decoder-Objekt ab, das den codierten Daten zugeordnet ist.
-   Bestimmen Sie den Typ der codierten Daten.

## <a name="members"></a>Member

Das **encoddata** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **encodeddata** -Objekt verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**Decoder**](encodeddata-decoder.md) | Ruft ein Decoder-Objekt ab, sofern vorhanden.<br/>             |
| [**Ges**](encodeddata-format.md)   | Gibt eine Zeichen folgen Darstellung der codierten Daten zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **encoddata** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                      | Zugriffstyp          | BESCHREIBUNG                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**Wert**](encodeddata-value.md)<br/> | Schreibgeschützt<br/> | Ruft die codierten Daten ab. Dies ist die Standard Eigenschaft.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der einzige unterstützte Typ von codierten Daten ist [**certificatepolicies**](certificatepolicies.md).

Das **encoddata** -Objekt kann nicht erstellt werden.

Die folgenden CAPICOM-Objekteigenschaften geben ein **encoddata** -Objekt zurück:

-   **PublicKey. encodecodkey**
-   **PublicKey. EncodedParameters**
-   **Erweiterung. encodeddata**
-   **Policy. encoddata**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
