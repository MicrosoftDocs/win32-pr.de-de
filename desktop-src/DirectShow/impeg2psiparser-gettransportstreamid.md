---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'IMpeg2PsiParser:: gettransportstreamid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344922"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>IMpeg2PsiParser:: gettransportstreamid-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die- `GetTransportStreamId` Methode ruft das Transportdaten \_ Strom-ID- \_ Feld aus der PAT-Datei ab. Dieser Wert wird vom Benutzer definiert und kann verwendet werden, um einen bestimmten Transportstream von anderen Datenströmen im gleichen Netzwerk zu unterscheiden. Ein Transportstream enthält höchstens einen Pat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstreamid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die das \_ Transportstream- \_ ID-Feld empfängt.

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

 

 




