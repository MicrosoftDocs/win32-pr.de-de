---
description: 'IMpeg2PsiParser::GetPatVersionNumber-Methode: Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: IMpeg2PsiParser::GetPatVersionNumber-Methode
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
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089148"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>IMpeg2PsiParser::GetPatVersionNumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetPatVersionNumber` -Methode ruft das Feld mit \_ der Versionsnummer aus dem PAT ab. Ein Transportstream enthält mindestens ein PAT. Die Versionsnummer wird erhöht, wenn sich die Informationen in der Tabelle ändern.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPatVersion* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die das Versionsnummerfeld \_ empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind, aber nicht beschränkt auf, die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[BEISPIEL FÜR PSI-Parserfilter](psi-parser-filter-sample.md)
</dt> </dl>

 

 




