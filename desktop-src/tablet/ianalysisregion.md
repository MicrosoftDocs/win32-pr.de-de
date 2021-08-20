---
description: Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: IAnalysisRegion-Schnittstelle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d8dc5b0af5746328ead68be3896148b7a4ddf79d6844a6d4ae976b2f29592d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045064"
---
# <a name="ianalysisregion-interface"></a>IAnalysisRegion-Schnittstelle

Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.

## <a name="members"></a>Member

Die **IAnalysisRegion-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisRegion** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAnalysisRegion-Schnittstelle** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](ianalysisregion-clone.md)                           | Erstellt eine Kopie der **IAnalysisRegion**.<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | Schränkt den Bereich von **IAnalysisRegion** auf den Teil des Bereichs ein, der das angegebene Rechteck nicht schneidet.<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | Schränkt den Bereich von **IAnalysisRegion** auf den Teil des Bereichs ein, der die angegebene **IAnalysisRegion nicht überschneidet.**<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Ruft das umgebundene Rechteck der **IAnalysisRegion ab.**<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Ruft ein Array von Rechtecke ab, das den Bereich der **IAnalysisRegion definiert.**<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | Schränkt den Bereich dieser **IAnalysisRegion** auf den Bereich ein, der durch seine Schnittmenge mit dem angegebenen Rechteck erstellt wird.<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | Schränkt den Bereich von **IAnalysisRegion** auf den Bereich ein, der durch seine Schnittmenge mit der angegebenen **IAnalysisRegion erstellt wird.**<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | Bestimmt, ob sich der Bereich von **IAnalysisRegion** mit dem angegebenen Rechteck überschneidet.<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | Ruft einen Wert ab, der angibt, ob **IAnalysisRegion einen** leeren Bereich darstellt.<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | Ruft einen Wert ab, der angibt, ob **IAnalysisRegion einen** unendlichen Bereich darstellt.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Reduziert **IAnalysisRegion, um** einen leeren Bereich zu darstellen.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Erweitert **IAnalysisRegion, um** einen unendlichen Bereich zu darstellen.<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | Erweitert den Bereich dieser **IAnalysisRegion** auf den Bereich, der durch seine Vereinigung mit dem angegebenen Rechteck erstellt wurde.<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | Erweitert den Bereich dieser **IAnalysisRegion** auf den Bereich, der durch seine Vereinigung mit der angegebenen **IAnalysisRegion erstellt wurde.**<br/>               |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle stellt einen Bereich dar, der aus rechteckigen Bereichen erstellt wird. Der [**IInkAnalyzer gibt**](iinkanalyzer.md) die Koordinaten eines Bereichs innerhalb des Koordinatenraums zurück, in dem er Strichdaten empfängt, oder interpretiert diese.

Um die aktuellen Grenzen von **IAnalysisRegion** zu erhalten, verwenden Sie [**die IAnalysisRegion::GetBounds-Methode**](ianalysisregion-getbounds.md) oder [**die IAnalysisRegion::GetRegionScans-Methode.**](ianalysisregion-getregionscans.md)

Verwenden Sie die folgenden Methoden, um den Bereich einer vorhandenen **IAnalysisRegion** zu ändern.

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**IAnalysisRegion::ExcludeRegion-Methode**](ianalysisregion-excluderegion.md)
-   [**IAnalysisRegion::IntersectRectangle-Methode**](ianalysisregion-intersectrectangle.md)
-   [**IAnalysisRegion::IntersectRegion-Methode**](ianalysisregion-intersectregion.md)
-   [**IAnalysisRegion::MakeEmpty-Methode**](ianalysisregion-makeempty.md)
-   [**IAnalysisRegion::MakeInfinite-Methode**](ianalysisregion-makeinfinite.md)
-   [**IAnalysisRegion::UnionRectangle-Methode**](ianalysisregion-unionrectangle.md)
-   [**IAnalysisRegion::UnionRegion-Methode**](ianalysisregion-unionregion.md)

Diese Schnittstelle entspricht dem System. Windows. Ink.AnalysisCore.AnalysisRegionBase-Klasse im .NET Framework.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

