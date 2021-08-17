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
ms.openlocfilehash: c0c5609f82db98caea02e08f1e4fbd3877eeccbae25a5e83da3ac2804577b100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398107"
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

Die Methode gibt einen HRESULT-Wert zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[PSI Parser-Filterbeispiel](psi-parser-filter-sample.md)
</dt> </dl>

 

 




