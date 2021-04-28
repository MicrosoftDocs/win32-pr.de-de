---
description: 'IMpeg2PsiParser::GetRecordProgramNumber-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: IMpeg2PsiParser::GetRecordProgramNumber-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089138"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>IMpeg2PsiParser::GetRecordProgramNumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetRecordProgramNumber` -Methode ruft die Programmnummer für ein angegebenes Programm ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Gibt den Eintrag im PAT an, der das Programm definiert, indiziert von 0 (null).

</dd> <dt>

*pwVal* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die das Programmnummerfeld \_ vom PAT empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[BEISPIEL FÜR PSI-Parserfilter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




