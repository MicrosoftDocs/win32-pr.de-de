---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'IMpeg2PsiParser:: getzähltofelementarystreams-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343126"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser:: getzähltofelementarystreams-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die- `GetCountOfElementaryStreams` Methode ruft die Anzahl der elementaren Datenströme in einem angegebenen Programm ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wprogramnumber* \[ in\]
</dt> <dd>

Gibt das \_ Feld für die Programmnummer des Programms an, wie in Pat angegeben.

</dd> <dt>

*pwval* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der elementaren Datenströme im Programm empfängt.

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

 

 




