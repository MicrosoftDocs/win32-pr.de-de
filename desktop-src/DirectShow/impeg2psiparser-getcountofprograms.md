---
description: 'IMpeg2PsiParser::GetCountOfPrograms-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: IMpeg2PsiParser::GetCountOfPrograms-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119428"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>IMpeg2PsiParser::GetCountOfPrograms-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetCountOfPrograms` -Methode ruft die Anzahl der Programme im Transportstream ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNumOfPrograms* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der Programme empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Wert zurück. Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[BEISPIEL FÜR PSI-Parserfilter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




