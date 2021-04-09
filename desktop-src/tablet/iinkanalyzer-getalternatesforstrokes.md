---
description: Ruft Analyse Alternativen für die Striche mit den angegebenen Strich bezeichaten ab.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Iinkanalyzer:: getalternatesforstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129457"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>Iinkanalyzer:: getalternatesforstrokes-Methode

Ruft Analyse Alternativen für die Striche mit den angegebenen Strich bezeichaten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der Stroke-IDs in *plstrokes*.

</dd> <dt>

*pltakte* \[ in\]
</dt> <dd>

Das Array von Strich bezeichlern.

</dd> <dt>

*ulmaximumalteraten* \[ in\]
</dt> <dd>

Die maximale Anzahl der zurückgegebenen Analyse Alternativen.

</dd> <dt>

*ppalternativen* \[ vorgenommen\]
</dt> <dd>

Das [**ianalysisalterniert**](ianalysisalternates.md) -Objekt, das die Analyse Alternativen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppalternativen* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Der oberste [**ianalysisalternate**](ianalysisalternate.md) wird als erste Alternative der Auflistung zurückgegeben.

Die angegebenen Striche müssen keine angrenzenden Bereiche des Dokuments darstellen.

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

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Ianalysisalteraten**](ianalysisalternates.md)
</dt> <dt>

[**Iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Iinkanalyzer:: ModifyTopAlternate-Methode**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Iinkanalyzer:: modifytopmodifiewithconfirmation-Methode**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

