---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'IMpeg2PsiParser:: getpmtversionnumber-Methode'
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
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338855"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>IMpeg2PsiParser:: getpmtversionnumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die- `GetPmtVersionNumber` Methode ruft das Feld mit der Versions \_ Nummer von einem angegebenen PMT ab. Die Versionsnummer wird jedes Mal inkrementiert, wenn sich die Programmdefinition ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wprogramnumber* \[ in\]
</dt> <dd>

Gibt das Programm \_ Nummern Feld des Programms an, wie in Pat angegeben.

</dd> <dt>

*ppmtversion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die das Feld mit der Versions \_ Nummer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **getrecordprogramnumber** -Methode, um die Programmnummer abzurufen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser:: getrecordprogramnumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Beispiel für PSI-Parser-Filter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




