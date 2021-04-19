---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'IMpeg2PsiParser:: getrecordprogramnumber-Methode'
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
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346807"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>IMpeg2PsiParser:: getrecordprogramnumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die- `GetRecordProgramNumber` Methode ruft die Programmnummer für ein angegebenes Programm ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Gibt den Eintrag in Pat an, der das Programm definiert, das von 0 (null) indiziert wird.

</dd> <dt>

*pwval* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die das Programm \_ Nummern Feld von Pat empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[Beispiel für PSI-Parser-Filter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




