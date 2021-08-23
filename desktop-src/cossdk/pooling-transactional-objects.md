---
description: Transaktionskomponenten, die in einem Pool zusammengefasst werden sollen, haben besondere Anforderungen.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Pooling von Transaktionsobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60180011305d0a03fee10fe1a4838f847306393709dc1bfef39f0ea8f69e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047308"
---
# <a name="pooling-transactional-objects"></a>Pooling von Transaktionsobjekten

Transaktionskomponenten, die in einem Pool zusammengefasst werden sollen, haben besondere Anforderungen.

## <a name="manually-enlisting-resources"></a>Manuelles Eintragen von Ressourcen

Poolfähige Objekte, die an Transaktionen teilnehmen, müssen verwaltete Ressourcen manuell eintragen. Wenn ein Objekt verwaltete Ressourcen zwischen Clients enthält, gibt es für den Ressourcen-Manager keine Möglichkeit, sich automatisch in eine Transaktion einzuweisen, wenn das Objekt in einem bestimmten Kontext aktiviert wird.

Das Objekt selbst muss die Logik der Erkennung der Transaktion verarbeiten, die automatische Eintragung des Ressourcen-Managers deaktivieren und alle darin enthaltenen Ressourcen manuell eintragen. Die Schritte hierfür gelten spezifisch für den verwendeten Ressourcen-Manager. Wenn Sie eine manuelle Eintragung durchführen müssen, lesen Sie die Dokumentation für Ihren Ressourcen-Manager.

Wie unten beschrieben, können Objekte mit Transaktionsaffinität zusammengefasst werden, während eine Transaktion aktiv ist, und mit Transaktionsaffinität aktiviert werden, wenn sie von einem Client aufgerufen werden, der dieser Transaktion zugeordnet ist. Bevor Sie Ressourcen eintragen, sollten Sie zunächst die Transaktionsaffinität überprüfen. Wenn das Objekt aus dem poolspezifischen Pool für diese Transaktion entnommen wurde, hat es bereits Arbeit in dieser Transaktion ausgeführt und seine Ressourcen eingetragen.

## <a name="turning-off-automatic-enlistment"></a>Deaktivieren der automatischen Eintragung

Die automatische Eintragung sollte deaktiviert werden, nachdem die Ressource erworben wurde, in der Regel im Konstruktor des Objekts. Das heißt, Sie deaktivieren die automatische Eintragung und stellen dann eine Verbindung her.

Das Deaktivieren der automatischen Eintragung kann manchmal eine dezente Prozedur sein, insbesondere im Fall von mehrstufigen Datenzugriffsanbietern. Die automatische Eintragung ist manchmal mit Verbindungspooling gekoppelt, wie bei ODBC, und manchmal nicht, wie bei OLE DB. Möglicherweise müssen Sie sicherstellen, dass die automatische Eintragung auf mehreren Anbieterebenen deaktiviert ist.

## <a name="implementing-iobjectcontrol"></a>Implementieren von IObjectControl

Poolfähige Objekte, die an Transaktionen teilnehmen, müssen den aktuellen Zustand der Ressourcen überwachen, die sie enthalten. Wenn das Objekt erkennt, dass es sich in einem nicht wiederverwendbaren Zustand befindet , z. B. wenn eine Verbindung fehlerhaft ist, sollte es false für [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)zurückgeben. Dies hat die Auswirkung, dass sowohl die Objektinstanz verworfen als auch die aktuelle Transaktion abgelehnt wird.

## <a name="transaction-specific-pools"></a>Transaction-Specific Pools

Ein Pool von -Objekten ist im Allgemeinen homogen, und alle derzeit nicht verwendeten Poolobjekte kehren gut zu einem beliebigen Client zurück. Die einzige Ausnahme von dieser Regel ist bei Transaktionsobjekten, für die das Objektpooling optimiert ist. Wenn der Client, der ein Objekt anfordert, über eine zugeordnete Transaktion verfügt, überprüft COM+ den Pool auf ein verfügbares Objekt, das dieser Transaktion bereits zugeordnet ist. Wenn ein Objekt mit Transaktionsaffinität gefunden wird, wird es an den Client zurückgegeben. Andernfalls wird ein Objekt aus dem allgemeinen Pool zurückgegeben.

Auf diese Weise werden spezielle Unterpools verwaltet, die Objekte mit Affinität für eine bestimmte Transaktion enthalten. Wenn die Transaktion committet oder abgebrochen wird, werden diese Objekte ohne Transaktionsaffinität an den allgemeinen Pool zurückgegeben, der von jedem Client verwendet werden kann.

Wenn Ihre Komponente ihre verwalteten Ressourcen aus diesem Grund manuell in einer Transaktion einlistet, sollte sie zunächst überprüfen, ob sie bereits eingetragen sind. In diesem Falle ist es nicht erforderlich, sich eintragen zu lassen.

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

[Anforderungen für poolfähige Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



