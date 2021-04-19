---
description: Ruft den Analyse Hinweis ab, der diese Warnung ausgelöst hat.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Ianalysiswarning:: GetHint-Methode (iacom. h)'
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
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346959"
---
# <a name="ianalysiswarninggethint-method"></a>Ianalysiswarning:: GetHint-Methode

Ruft den Analyse Hinweis ab, der diese Warnung ausgelöst hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*panalysishint* \[ vorgenommen\]
</dt> <dd>

Der Kontext Knoten des Analyse Hinweises, der diese Warnung verursacht hat, oder **null** , wenn ein Analyse Hinweis Diese Warnung nicht verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *panalysishint* aufrufen, wenn Sie den Kontext Knoten des Analyse Hinweises nicht mehr verwenden müssen.

 

Ein Beispiel für einen Analyse Hinweis, der eine [**ianalysiswarning**](ianalysiswarning.md) generiert, ist ein Analyse Hinweis, der eine falsch geschriebene Faktoid enthält. In diesem Fall gibt die frei Hand Analyse einen [**ianalysisstatus**](ianalysisstatus.md) zurück, der ein **ianalysiswarning** -Element enthält, das auf den Kontext Knoten des Analyse Hinweises mit der falsch geschriebenen Faktoid verweist. In diesem Fall gibt die [**ianalysiswarning:: getwarningcode**](ianalysiswarning-getwarningcode.md) -Methode der Analyse Warnung außerdem einen [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) -Wert von **AnalysisWarningCode \_ FactoidNotSupported** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysiswarning**](ianalysiswarning.md)
</dt> <dt>

[**Ianalysisstatus**](ianalysisstatus.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

