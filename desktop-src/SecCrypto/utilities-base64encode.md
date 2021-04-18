---
description: Codiert eine Zeichenfolge als Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Utilities. einem base64encode-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366021"
---
# <a name="utilitiesbase64encode-method"></a>Utilities. einem base64encode-Methode

\[Die **einem base64encode** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Die **einem base64encode** -Methode codiert eine Zeichenfolge als Base64.

## <a name="syntax"></a>Syntax


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Srcstring* \[ in\]
</dt> <dd>

Die Zeichenfolge, die als Base64 codiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Base64-codierte Zeichenfolge.

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

 

 




