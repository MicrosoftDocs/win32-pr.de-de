---
description: Ruft ein Array von Rechtecke ab, das den Bereich von ianalysisregion definiert.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Ianalysisregion:: GetRegionScans-Methode (iacom. h)'
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
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347199"
---
# <a name="ianalysisregiongetregionscans-method"></a>Ianalysisregion:: GetRegionScans-Methode

Ruft ein Array von Rechtecke ab, das den Bereich von [**ianalysisregion**](ianalysisregion.md)definiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der in *pregionscans* zurückgegebenen Rechtecke.

</dd> <dt>

*pregionscans* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von Rechtecke, das den Bereich von [**ianalysisregion**](ianalysisregion.md)definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn *pregionscans* als **null**-Werte übergangen werden, gibt die **GetRegionScans** -Methode **S \_ OK** zurück, und die Anzahl der Rechtecke wird in *pulCount* zurückgegeben.

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *pregionscans* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Die Begrenzungen der Rechtecke befinden sich in frei Hand Raumkoordinaten.

Die Vereinigung der zurückgegebenen Rechtecke stellt den Bereich von [**ianalysisregion**](ianalysisregion.md)dar.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie die Rechtecke, die den Bereich von [**ianalysisregion**](ianalysisregion.md)definieren, `region` und nur die Anzahl der Rechtecke erhalten.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Ianalysisregion:: GetBounds-Methode**](ianalysisregion-getbounds.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

