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
ms.openlocfilehash: ffd03bea09fb9041b91bb214287442eb59a7101be7a8841e0d38e28bcdaf3ecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767360"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>IMpeg2PsiParser::GetPatVersionNumber-Methode

Die Implementierung dieser Methode wird als Beispielcode mit dem DirectShow SDK bereitgestellt. Es handelt sich nicht um eine unterstützte DirectShow-API.

Die `GetPatVersionNumber` -Methode ruft das \_ Versionsnummernfeld aus dem PAT ab. Ein Transportstream enthält höchstens ein PAT. Die Versionsnummer wird erhöht, wenn sich die Informationen in der Tabelle ändern.

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

Zeiger auf eine Variable, die das \_ Versionsnummernfeld empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind u. a. die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                          | Beschreibung         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Erfolg.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> <dt>

[PSI Parser-Filterbeispiel](psi-parser-filter-sample.md)
</dt> </dl>

 

 




