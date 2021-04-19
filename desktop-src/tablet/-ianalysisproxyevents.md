---
description: Gibt Ereignisse an, die den Daten Proxy Schritten eines iinkanalyzer-Objekts zugeordnet sind.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: _IAnalysisProxyEvents-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106350598"
---
# <a name="_ianalysisproxyevents-interface"></a>\_Ianalysisproxyevents-Schnittstelle

Gibt Ereignisse an, die den Daten Proxy Schritten eines [**iinkanalyzer**](iinkanalyzer.md) -Objekts zugeordnet sind.

-   [Ereignisse](/windows)

### <a name="events"></a>Ereignisse

Die **\_ ianalysisproxyevents** -Schnittstelle enthält diese Ereignisse.



| Ereignis                                                                                      | BESCHREIBUNG                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContextNode created**](-ianalysisproxyevents-contextnodecreated.md)                     | Tritt auf, nachdem [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextnode**](icontextnode.md) -Objekt erstellt hat.<br/>                                                                  |
| [**Contextnodebug**](-ianalysisproxyevents-contextnodedeleting.md)                   | Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt löscht.<br/>                                                                 |
| [**Contextnodelta inkadditions**](-ianalysisproxyevents-contextnodelinkadding.md)               | Tritt auf, bevor [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextlink**](icontextlink.md) -Objekt zwischen zwei [**icontextnode**](icontextnode.md) -Objekten hinzufügt.<br/>           |
| [**Contextnodelinklösch**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | Tritt auf, bevor [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextlink**](icontextlink.md) -Objekt zwischen zwei [**icontextnode**](icontextnode.md) -Objekten löscht.<br/>         |
| [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt an eine neue Position in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt.<br/> |
| [**Contextnodebug propertiesaktualisierten**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | Tritt auf, nachdem der [**iinkanalyzer**](iinkanalyzer.md) eine oder mehrere Eigenschaften eines [**icontextnode**](icontextnode.md) -Objekts aktualisiert hat.<br/>                                        |
| [**Contextnodereenting**](-ianalysisproxyevents-contextnodereparenting.md)             | Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) [**-Objekt durch**](icontextnode.md) Ändern des übergeordneten Knotens verschoben wird.<br/>                                       |
| [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | Tritt auf, bevor die Analyseergebnisse von [**iinkanalyzer**](iinkanalyzer.md) so synchronisiert werden, dass eine Anwendung Daten mit dem **iinkanalyzer** synchronisieren kann.<br/>                      |
| [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md)                   | Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) innerhalb des Bereichs eines teilweise aufgefüllten [**icontextnode**](icontextnode.md) -Objekts eine Analyse ausführt.<br/>               |
| [**Strokereüber geordnet**](-ianalysisproxyevents-strokereparented.md)                         | Tritt auf, wenn der [**iinkanalyzer**](iinkanalyzer.md) einen Strich von einem [**icontextnode**](icontextnode.md) -Objekt zu einem anderen verschiebt.<br/>                                           |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Ereignisse, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Weitere Informationen zum Synchronisieren von Anwendungsdaten mit **iinkanalyzer** finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

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

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_Ianalysil Vents](-ianalysisevents.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

