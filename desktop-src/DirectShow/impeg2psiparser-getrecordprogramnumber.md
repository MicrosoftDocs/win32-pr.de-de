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
ms.openlocfilehash: e42e991fc7e288fc36dafcd167fe21ffb4983baeeb34bbb80e1bf67981e24779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083700"
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

Die -Methode gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[BEISPIEL FÜR PSI-Parserfilter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




