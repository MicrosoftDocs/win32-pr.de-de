---
description: Ruft den Analysehinweis ab, der diese Warnung verursacht hat.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: IAnalysisWarning::GetHint-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940510"
---
# <a name="ianalysiswarninggethint-method"></a>IAnalysisWarning::GetHint-Methode

Ruft den Analysehinweis ab, der diese Warnung verursacht hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAnalysisHint* \[ out\]
</dt> <dd>

Der Analysehinweiskontextknoten, der diese Warnung verursacht hat, oder **NULL,** wenn ein Analysehinweis diese Warnung nicht verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *pAnalysisHint* auf, wenn Sie den Kontextknoten des Analysehinweises nicht mehr verwenden müssen.

 

Ein Beispiel für einen Analysehinweis, der ein [**IAnalysisWarning**](ianalysiswarning.md) generiert, ist ein Analysehinweis, der ein falsch geschriebenes Factoid enthält. In diesem Fall gibt die Freihandanalyse einen [**IAnalysisStatus**](ianalysisstatus.md) zurück, der ein **IAnalysisWarning** enthält, das auf den Analysehinweiskontextknoten mit dem falsch geschriebenen Factoid verweist. In diesem Fall gibt die [**IAnalysisWarning::GetWarningCode-Methode**](ianalysiswarning-getwarningcode.md) der Analysewarnung den [**AnalysisWarningCode-Wert**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ FactoidNotSupported zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Analysiswarningcode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

