---
description: In Poolable-Objekten müssen bestimmte Anforderungen erfüllt werden, damit eine einzelne Objektinstanz von mehreren Clients verwendet werden kann.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Anforderungen für in einem Pool Bare Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958354"
---
# <a name="requirements-for-poolable-objects"></a>Anforderungen für in einem Pool Bare Objekte

In Poolable-Objekten müssen bestimmte Anforderungen erfüllt werden, damit eine einzelne Objektinstanz von mehreren Clients verwendet werden kann.

## <a name="stateless"></a>Zustandslos

Um Sicherheit, Konsistenz und Isolation zu gewährleisten, sollten in einem Pool einsetzbare Objekte keinen Client spezifischen Zustand vom Client zum Client aufweisen. Sie können jeden Client Status mithilfe von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)verwalten, eine kontextspezifische Initialisierung mit [**IObjectControl:: Aktivierung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) durchführen und einen beliebigen Client Zustand mit [**IObjectControl::D eaktivierungs**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)bereinigen. Weitere Details finden Sie unter [Steuern der Objekt Lebensdauer und des Zustands](controlling-object-lifetime-and-state.md).

## <a name="no-thread-affinity"></a>Keine Thread Affinität

Poolable-Objekte können nicht an einen bestimmten Thread gebunden werden. Andernfalls könnte die Leistung möglicherweise katastrophal sein. Aus diesem Grund können Pool fähige Objekte nicht für die Durchführung im Apartment Modell gekennzeichnet werden. Sie müssen im Multithread-Apartment oder im neutralen Apartment ausgeführt werden. Außerdem sollten in einem Pool einsetzbare Objekte keinen lokalen Thread Speicher verwenden, und Sie sollten nicht den frei Thread-Mars Haller aggregieren. Weitere Details zum Threading in com+ finden Sie unter [com+-Threading Modelle](com--threading-models.md).

> [!Note]  
> Mit den Entwicklungsumgebungen Microsoft Visual Basic 6,0 und früher können nur Apartment Modellkomponenten erstellt werden. In Visual Basic .net können Komponenten jedoch in einem Pool zusammengefasst werden.

 

## <a name="aggregatable"></a>Aggregierbar

In Poolable-Objekten müssen Aggregationen unterstützt werden, d. –. Sie müssen die Erstellung unterstützen, indem [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit einem *pUnkOuter* -Argument ungleich NULL aufgerufen wird. Wenn com+ ein in einem Pool zusammengefasster Objekt aktiviert, wird ein Aggregat erstellt, um die Lebensdauer des gepoolten Objekts zu verwalten und Methoden für [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)aufzurufen. Ausführliche Informationen zum Schreiben von aggregierbare-Objekten finden Sie unter [Aggregation](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Transaktionale Komponenten

In Poolable-Objekten, die an Transaktionen teilnehmen, müssen verwaltete Ressourcen manuell eingetragen werden. Wenn Ihr Objekt eine verwaltete Ressource (z. b. eine Datenbankverbindung) enthält, ist es für den Ressourcen-Manager nicht möglich, sich automatisch in eine Transaktion einzutragen, wenn das Objekt im angegebenen Kontext aktiviert wird. Daher muss das-Objekt selbst die Logik zum Erkennen der Transaktion, das Ausschalten der automatischen Eintragung des Ressourcen-Managers und das manuelle eintragen der darin befindlichen Ressourcen verarbeiten. Außerdem sollte ein transaktionales, in einem Pool zusammengefasste Objekt den aktuellen Zustand seiner Ressourcen in den Parameterwerten von [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)widerspiegeln. Weitere Details finden Sie unter [Pooling von transaktionalen Objekten](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementieren von IObjectControl zum Verwalten der Objekt Lebensdauer

In Poolable-Objekten sollte [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)implementiert werden, obwohl dies nicht zwingend erforderlich ist. Transaktionale Komponenten, die in einem Pool zusammengefasst sind, müssen jedoch **IObjectControl** implementieren. Diese Komponenten sollten den Zustand der Ressourcen überwachen, die Sie enthalten, und angeben, wann Sie nicht wieder verwendet werden können. Wenn [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) den Wert "false" zurückgibt, wird eine Transaktion beendet. Weitere Details finden Sie unter [Steuern der Objekt Lebensdauer und des Zustands](controlling-object-lifetime-and-state.md).

## <a name="language-restrictions"></a>Spracheinschränkungen

Komponenten, die mit Microsoft Visual Basic 6,0 und früher entwickelt wurden, können nicht in einem Pool zusammengefasst werden, da diese Komponenten Apartment Modell Thread sind. In Visual Basic .net können Komponenten jedoch in einem Pool zusammengefasst werden.

## <a name="legacy-components"></a>Legacykomponenten

Solange Sie nicht transaktional sind und den entsprechenden Voraussetzungen entsprechen, können Komponenten in einem Pool zusammengefasst werden, auch wenn Sie nicht speziell mit den Pooling-Funktionen geschrieben wurden. Das Implementieren von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)ist nicht erforderlich. eine Komponente, die dies nicht einfach macht, wird nicht an der Verwaltung Ihrer Lebensdauer beteiligt sein. Wenn [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) nicht implementiert ist, wird das Objekt weiterhin wieder verwendet, bis der Pool die maximale Größe erreicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Steuern der Objekt Lebensdauer und des Zustands](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funktionsweise des Objekt Pooling](how-object-pooling-works.md)
</dt> <dt>

[Verbessern der Leistung durch Objekt Pooling](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling von transaktionalen Objekten](pooling-transactional-objects.md)
</dt> </dl>

 

 
