---
description: Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Ianalysisregion-Schnittstelle (iacom. h)
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
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751857"
---
# <a name="ianalysisregion-interface"></a>Ianalysisregion-Schnittstelle

Macht Methoden und Eigenschaften für einen Bereich verfügbar, der einen Bereich eines Dokuments darstellt.

## <a name="members"></a>Member

Die **ianalysisregion** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ianalysisregion** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ianalysisregion** -Schnittstelle verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klon**](ianalysisregion-clone.md)                           | Erstellt eine Kopie von **ianalysisregion**.<br/>                                                                                          |
| [**Excluderectangle**](ianalysisregion-excluderectangle.md)     | Schränkt den Bereich von **ianalysisregion** auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.<br/>           |
| [**Excluderegion**](ianalysisregion-excluderegion.md)           | Schränkt den Bereich von **ianalysisregion** auf den Teil des Bereichs ein, der den angegebenen **ianalysisregion** nicht überschneidet.<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Ruft das umgebende Rechteck von **ianalysisregion** ab.<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Ruft ein Array von Rechtecke ab, das den Bereich von **ianalysisregion** definiert.<br/>                                                  |
| [**Intersectrechteck**](ianalysisregion-intersectrectangle.md) | Schränkt den Bereich dieses **ianalysisregion** auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.<br/>                |
| [**Intersectregion**](ianalysisregion-intersectregion.md)       | Schränkt den Bereich von **ianalysisregion** auf den Bereich ein, der durch die Schnittmenge mit der angegebenen **ianalysisregion** erstellt wurde.<br/>       |
| [**Intersecin**](ianalysisregion-intersectswith.md)         | Bestimmt, ob sich der Bereich des **ianalysisregion** mit dem angegebenen Rechteck überschneidet.<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | Ruft einen Wert ab, der angibt, ob **ianalysisregion** einen leeren Bereich darstellt.<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | Ruft einen Wert ab, der angibt, ob **ianalysisregion** einen unendlichen Bereich darstellt.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Reduziert den **ianalysisregion** -Element, um einen leeren Bereich darzustellen.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Erweitert **ianalysisregion** , um einen unendlichen Bereich darzustellen.<br/>                                                                      |
| [**Unionrechteck**](ianalysisregion-unionrectangle.md)         | Erweitert den Bereich dieses **ianalysisregion** auf den Bereich, der durch die zugehörige Union mit dem angegebenen Rechteck erstellt wurde.<br/>                         |
| [**Unionregion**](ianalysisregion-unionregion.md)               | Erweitert den Bereich dieses **ianalysisregion** auf den Bereich, der von seiner Union mit dem angegebenen **ianalysisregion** erstellt wurde.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle stellt einen Bereich dar, der aus rechteckigen Bereichen erstellt wird. Der [**iinkanalyzer**](iinkanalyzer.md) gibt die Koordinaten eines Bereichs innerhalb des Koordinaten Bereichs zurück, in dem er Strich Daten empfängt, oder interpretiert ihn.

Verwenden Sie die [**ianalysisregion:: GetBounds-Methode**](ianalysisregion-getbounds.md) oder die [**ianalysisregion:: GetRegionScans-Methode**](ianalysisregion-getregionscans.md), um die aktuellen Begrenzungen von **ianalysisregion** zu erhalten.

Verwenden Sie die folgenden Methoden, um den Bereich einer vorhandenen **ianalysisregion** zu ändern.

-   [**Ianalysisregion:: excluderectangle**](ianalysisregion-excluderectangle.md)
-   [**Ianalysisregion:: excluderegion-Methode**](ianalysisregion-excluderegion.md)
-   [**Ianalysisregion:: intersectrechteck-Methode**](ianalysisregion-intersectrectangle.md)
-   [**Ianalysisregion:: intersectregion-Methode**](ianalysisregion-intersectregion.md)
-   [**Ianalysisregion:: MakeEmpty-Methode**](ianalysisregion-makeempty.md)
-   [**Ianalysisregion:: MakeInfinite-Methode**](ianalysisregion-makeinfinite.md)
-   [**Ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md)
-   [**Ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md)

Diese Schnittstelle entspricht der Klasse System. Windows. Ink. AnalysisCore. AnalysisRegionBase in der .NET Framework.

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

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

