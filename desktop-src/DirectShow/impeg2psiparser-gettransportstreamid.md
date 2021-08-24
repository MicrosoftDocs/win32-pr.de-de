---
description: 'IMpeg2PsiParser::GetTransportStreamId-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: IMpeg2PsiParser::GetTransportStreamId-Methode
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
ms.openlocfilehash: e78eabce23633029e4ef3dfe6c6777c586a5d74ed28ccfe466c89064851f8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791900"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>IMpeg2PsiParser::GetTransportStreamId-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetTransportStreamId` -Methode ruft das Feld für die \_ \_ Transportstream-ID aus dem PAT ab. Dieser Wert wird vom Benutzer definiert und kann verwendet werden, um einen bestimmten Transportstream von anderen Datenströmen im gleichen Netzwerk zu unterscheiden. Ein Transportstream enthält mindestens ein PAT.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStreamId* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die das Feld für die \_ \_ Transportstream-ID empfängt.

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

 

 




