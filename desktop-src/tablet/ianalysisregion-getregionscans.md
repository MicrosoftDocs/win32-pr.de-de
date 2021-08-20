---
description: Ruft ein Array von Rechtecke ab, das den Bereich von IAnalysisRegion definiert.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: IAnalysisRegion::GetRegionScans-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e197126a99023fb96c2798343b391d53de4f6cd97aaaa141918f0fe705e5ad1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045317"
---
# <a name="ianalysisregiongetregionscans-method"></a>IAnalysisRegion::GetRegionScans-Methode

Ruft ein Array von Rechtecke ab, das den Bereich von [**IAnalysisRegion**](ianalysisregion.md)definiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ out\]
</dt> <dd>

Die Anzahl der in *pRegionScans zurückgegebenen* Rechtecke.

</dd> <dt>

*pRegionScans* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array von Rechtecke, das den Bereich von [**IAnalysisRegion**](ianalysisregion.md)definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Wenn *pRegionScans* als **NULL** übergeben wird, gibt die **GetRegionScans-Methode** **S \_ OK** zurück, und die Anzahl der Rechtecke wird in *pulCount* zurückgegeben.

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *pRegionScans* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Die Begrenzungen der Rechtecke befinden sich in Freihandraumkoordinaten.

Die Vereinigung der zurückgegebenen Rechtecke stellt den Bereich des [**IAnalysisRegion**](ianalysisregion.md)dar.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Die Rechtecke, die den Bereich von [**IAnalysisRegion**](ianalysisregion.md)definieren, `region` und nur die Anzahl der Rechtecke abrufen.


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::GetBounds-Methode**](ianalysisregion-getbounds.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

