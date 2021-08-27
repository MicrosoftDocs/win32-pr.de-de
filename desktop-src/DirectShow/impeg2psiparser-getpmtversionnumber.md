---
description: 'IMpeg2PsiParser::GetPmtVersionNumber-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: IMpeg2PsiParser::GetPmtVersionNumber-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: fe193e07cb32b1048d6075786c381c03370d3297f9eb771238cd7ae499076e5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107710"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>IMpeg2PsiParser::GetPmtVersionNumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetPmtVersionNumber` -Methode ruft das Versionsnummerfeld \_ aus einem angegebenen PMT ab. Die Versionsnummer wird erhöht, wenn sich die Definition des Programms ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wProgramNumber* \[ In\]
</dt> <dd>

Gibt das \_ Programmnummerfeld des Programms an, wie im PAT angegeben.

</dd> <dt>

*pPmtVersion* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die das Versionsnummerfeld \_ empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie **die GetRecordProgramNumber-Methode,** um die Programmnummer zu erhalten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[BEISPIEL FÜR PSI-Parserfilter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




