---
description: Ruft eine geordnete Auflistung von iinkanalysiserkenzer-Objekten ab.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862687"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>Iinkanalyzer:: getinkanalysiserkenzersbypriority-Methode

Ruft eine geordnete Auflistung von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppinkanalysiserkenzers* \[ vorgenommen\]
</dt> <dd>

Eine geordnete Auflistung von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) -Objekten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppinkanalysiserkenzers* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Die Reihenfolge der erkenungen in dieser Auflistung gibt die Reihenfolge an, in der [**iinkanalyzer**](iinkanalyzer.md) die verfügbaren erkenungen auswertet. **Iinkanalyzer** verwendet die Sprache der Striche als primäres Kriterium für das Anwenden eines [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md). Als sekundäres Kriterium vergleicht **iinkanalyzer** Analyse Hinweis Informationen mit den unterstützten Funktionen eines **iinkanalysiserkenzer** -Objekts (siehe [**iinkanalysiserkenzer:: getfunktionen**](iinkanalysisrecognizer-getcapabilities.md)). Weitere Informationen zu Analyse hinweisen finden Sie unter [**iinkanalyzer:: erkreateanalysishint-Methode**](iinkanalyzer-createanalysishint.md).

Wenn mehr als ein [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) einen sprach Bezeichner unterstützt, verwendet [**iinkanalyzer**](iinkanalyzer.md) einen "First-Fit"-Algorithmus, um den ersten **iinkanalysiserkenzer** auszuwählen, um Striche dieser Sprache zu analysieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalysiserkenzers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**Iinkanalyzer:: sethighestpriorityinkanalysiserkenzer-Methode**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

