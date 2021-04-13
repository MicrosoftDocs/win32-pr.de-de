---
description: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'IMpeg2PsiParser:: getpatversionnumber-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392449"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>IMpeg2PsiParser:: getpatversionnumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die- `GetPatVersionNumber` Methode ruft das Feld mit der Versions \_ Nummer von Pat ab. Ein Transportstream enthält höchstens einen Pat. Die Versionsnummer wird jedes Mal inkrementiert, wenn sich die Informationen in der Tabelle ändern.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppatversion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die das Feld mit der Versions \_ Nummer empfängt.

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

 

 




