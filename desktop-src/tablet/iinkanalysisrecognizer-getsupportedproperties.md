---
description: Ruft die GUIDs (Globally Unique Identifiers) für die Eigenschaften ab, die dieser IInkAnalysisRecognizer für Analyseergebnisse generieren kann.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: IInkAnalysisRecognizer::GetSupportedProperties-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fce33317a234d82d6045dbefa93ed582d31d92f6ff54abe9ef87949559a5d269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057860"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>IInkAnalysisRecognizer::GetSupportedProperties-Methode

Ruft die GUIDs (Globally Unique Identifiers) für die Eigenschaften ab, die dieser [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) für Analyseergebnisse generieren kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulPropertiesCount* \[ in, out\]
</dt> <dd>

Die Anzahl der GUIDs in *ppProperties*.

</dd> <dt>

*ppProperties* \[ out\]
</dt> <dd>

Ein Zeiger auf die GUIDs von Eigenschaften, die dieser [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) für Analyseergebnisse generieren kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *ppProperties* frei zu geben, wenn Sie die Informationen nicht mehr benötigen.

 

Eine Recognizer kann Linienmetriken, Zeilennummern, Konfidenzstufen und so weiter unterstützen. Eine vollständige Liste der Eigenschaften, die von einer Erkennung unterstützt werden können, finden Sie unter [RecognitionProperty Constants](recognitionproperty-constants.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[RecognitionProperty-Konstanten](recognitionproperty-constants.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

