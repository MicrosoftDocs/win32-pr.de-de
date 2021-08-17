---
description: Ruft den Bereich des Dokuments ab, der Änderungen entspricht, die in der Kontextknotenstruktur des IInkAnalyzer-Objekts als Ergebnis der Freihandanalyse vorgenommen wurden.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: IAnalysisStatus::GetAppliedChangesRegion-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044993"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>IAnalysisStatus::GetAppliedChangesRegion-Methode

Ruft den Bereich des Dokuments ab, der Änderungen entspricht, die in der Kontextknotenstruktur des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) als Ergebnis der Freihandanalyse vorgenommen wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAppliedChangesRegion* \[ out\]
</dt> <dd>

Ein Zeiger auf die [**IAnalysisRegion**](ianalysisregion.md) des Dokuments, in dem Änderungen vorgenommen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für \* *pAppliedChangesRegion* auf, wenn Sie die Analyseregion nicht mehr verwenden müssen.

 

Diese Methode wird am häufigsten verwendet, wenn die Anwendung Informationen zu Debugzwecken empfängt und den Bereich, in dem Änderungen auftreten können, ungültig machen muss, damit die Debuginformationen gezeichnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

