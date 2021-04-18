---
description: Decodiert eine Zeichenfolge aus base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Utilities. Base64Decode-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364708"
---
# <a name="utilitiesbase64decode-method"></a>Utilities. Base64Decode-Methode

\[Die **Base64Decode** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Die **Base64Decode** -Methode decodiert eine Zeichenfolge aus base64.

## <a name="syntax"></a>Syntax


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Encodstring* \[ in\]
</dt> <dd>

Die zu decodierende base64-codierte Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die decodierte Zeichenfolge.

## <a name="remarks"></a>Bemerkungen

Base64-Codierung ist das Schema, mit dem Binärdaten übertragen werden. Base64 verarbeitet Daten als 24-Bit-Gruppen und ordnet diese Daten vier codierten Zeichen zu. Base64-Codierung wird manchmal als 3-zu-4-Codierung bezeichnet. Jede 6 Bits der 24-Bit-Gruppe wird als Index in einer Mapping-Tabelle (dem Base64-Alphabet) zum Abrufen eines Zeichens für die codierten Daten verwendet. Die codierten Daten weisen Zeilenlängen auf, die auf 76 Zeichen beschränkt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Versorgungsunternehmen**](utilities.md)
</dt> </dl>

 

 




