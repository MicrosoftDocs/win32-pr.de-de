---
description: Poolfähige Objekte müssen bestimmte Anforderungen erfüllen, damit eine einzelne Objektinstanz von mehreren Clients verwendet werden kann.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Anforderungen für poolfähige Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3e3b67f7d796c199649b64f711ec32a75374bff60ebf900b34871ed4bc310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047288"
---
# <a name="requirements-for-poolable-objects"></a>Anforderungen für poolfähige Objekte

Poolfähige Objekte müssen bestimmte Anforderungen erfüllen, damit eine einzelne Objektinstanz von mehreren Clients verwendet werden kann.

## <a name="stateless"></a>Zustandslos

Um Sicherheit, Konsistenz und Isolation zu gewährleisten, sollten poolfähige Objekte keinen clientspezifischen Zustand von Client zu Client enthalten. Sie können jeden clientspezifischen Zustand mithilfe von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)verwalten, eine kontextspezifische Initialisierung mit [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) durchführen und alle Clientstatus mit [**IObjectControl::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)bereinigen. Weitere Informationen finden Sie unter [Steuern der Objektlebensdauer und des Zustands.](controlling-object-lifetime-and-state.md)

## <a name="no-thread-affinity"></a>Keine Threadaffinität

Poolfähige Objekte können nicht an einen bestimmten Thread gebunden werden. Andernfalls kann die Leistung möglicherweise unerschwert sein. Aus diesem Grund können poolfähige Objekte nicht für die Ausführung im Apartmentmodell markiert werden. sie müssen im Multithread-Apartment oder im neutralen Apartment ausgeführt werden. Darüber hinaus sollten poolfähige Objekte weder den lokalen Threadspeicher verwenden noch den Freethread-Marshaller aggregieren. Weitere Informationen zum Threading in COM+ finden Sie unter [COM+-Threadingmodelle.](com--threading-models.md)

> [!Note]  
> Die Microsoft Visual Basic 6.0 und frühere Entwicklungsumgebungen können nur Apartmentmodellkomponenten erstellen. In Visual Basic .NET können Komponenten jedoch in einem Pool zusammengefasst werden.

 

## <a name="aggregatable"></a>Aggregierbar

Poolfähige Objekte müssen aggregation unterstützen, d. h., sie müssen das Erstellen durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit einem *pUnkOuter-Argument* unterstützen, das nicht NULL ist. Wenn COM+ ein in einem Pool zusammengefasstes Objekt aktiviert, wird ein Aggregat erstellt, um die Lebensdauer des in einem Pool zusammengefassten Objekts zu verwalten und Methoden für [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)aufzurufen. Ausführliche Informationen zum Schreiben von aggregierbaren Objekten finden Sie unter [Aggregation](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Transaktionskomponenten

Poolfähige Objekte, die an Transaktionen teilnehmen, müssen verwaltete Ressourcen manuell eintragen. Wenn ihr Objekt eine verwaltete Ressource enthält, z. B. eine Datenbankverbindung, kann der Ressourcen-Manager beim Aktivieren des Objekts im kontextgesteuerten Kontext keine automatische Eintragung in eine Transaktion durchführen, während es in einem Pool zusammengefasst ist. Daher muss das Objekt selbst die Logik der Erkennung der Transaktion verarbeiten, die automatische Eintragung des Ressourcen-Managers deaktivieren und alle darin enthaltenen Ressourcen manuell eintragen. Darüber hinaus sollte ein Transaktionspoolobjekt den aktuellen Zustand seiner Ressourcen in den Parameterwerten von [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)widerspiegeln. Weitere Informationen finden Sie unter [Pooling Transactional Objects](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementieren von IObjectControl zum Verwalten der Objektlebensdauer

Poolfähige Objekte sollten [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)implementieren, obwohl dies nicht unbedingt erforderlich ist. Transaktionskomponenten, die in einem Pool zusammengefasst sind, müssen jedoch **IObjectControl** implementieren. Diese Komponenten sollten den Zustand der ressourcen, die sie enthalten, überwachen und angeben, wann sie nicht wiederverwendet werden können. Wenn [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) false zurückgibt, wird eine Transaktion untergangen. Weitere Informationen finden Sie unter [Steuern der Objektlebensdauer und des Zustands.](controlling-object-lifetime-and-state.md)

## <a name="language-restrictions"></a>Spracheinschränkungen

Komponenten, die mit Microsoft Visual Basic 6.0 und früher entwickelt wurden, können nicht in einem Pool zusammengefasst werden, da diese Komponenten im Apartmentmodell gethreadt werden. In Visual Basic .NET können Komponenten jedoch in einem Pool zusammengefasst werden.

## <a name="legacy-components"></a>Legacykomponenten

Solange sie nicht transaktional sind und den entsprechenden vorherigen Anforderungen entsprechen, können Komponenten auch dann in einem Pool zusammengefasst werden, wenn sie nicht speziell unter Berücksichtigung der Poolfunktion geschrieben wurden. Es ist nicht erforderlich, [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)zu implementieren. Eine Komponente, die dies nicht tut, nimmt einfach nicht an der Verwaltung ihrer Lebensdauer teil. Wenn [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) nicht implementiert ist, wird das Objekt weiterhin wiederverwendet, bis der Pool die maximale Größe erreicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Steuern der Lebensdauer und des Zustands von Objekten](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funktionsweise von Objektpooling](how-object-pooling-works.md)
</dt> <dt>

[Verbessern der Leistung mit Objektpooling](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling von Transaktionsobjekten](pooling-transactional-objects.md)
</dt> </dl>

 

 
