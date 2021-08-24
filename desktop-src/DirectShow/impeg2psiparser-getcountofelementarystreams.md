---
description: 'IMpeg2PsiParser::GetCountOfElementaryStreams-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: IMpeg2PsiParser::GetCountOfElementaryStreams-Methode
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
ms.openlocfilehash: e241697884a4b665c160dc9991e4cb7f02c76f1ba32bc7a0656515faf1117a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767380"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>IMpeg2PsiParser::GetCountOfElementaryStreams-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetCountOfElementaryStreams` -Methode ruft die Anzahl der elementaren Streams in einem angegebenen Programm ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wProgramNumber* \[ In\]
</dt> <dd>

Gibt das \_ Programmnummernfeld für das Programm an, wie im PAT angegeben.

</dd> <dt>

*pwVal* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der elementaren Streams im Programm empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die **GetRecordProgramNumber-Methode,** um die Programmnummer abzurufen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[PSI Parser-Filterbeispiel](psi-parser-filter-sample.md)
</dt> </dl>

 

 




