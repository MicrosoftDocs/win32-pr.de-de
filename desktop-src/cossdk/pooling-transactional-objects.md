---
description: Transaktionale Komponenten, die in einem Pool zusammengefasst werden sollen, müssen besondere Anforderungen erfüllen.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Pooling von transaktionalen Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345445"
---
# <a name="pooling-transactional-objects"></a>Pooling von transaktionalen Objekten

Transaktionale Komponenten, die in einem Pool zusammengefasst werden sollen, müssen besondere Anforderungen erfüllen.

## <a name="manually-enlisting-resources"></a>Manuelles eintragen von Ressourcen

In Poolable-Objekten, die an Transaktionen teilnehmen, müssen verwaltete Ressourcen manuell eingetragen werden. Wenn ein Objekt verwaltete Ressourcen zwischen Clients enthält, gibt es keine Möglichkeit für den Ressourcen-Manager, sich automatisch in eine Transaktion einzutragen, wenn das Objekt in einem bestimmten Kontext aktiviert wird.

Das Objekt selbst muss die Logik zum Erkennen der Transaktion, zum Ausschalten der automatischen Eintragung des Ressourcen-Managers und zum manuellen eintragen der darin befindlichen Ressourcen verarbeiten. Die erforderlichen Schritte sind spezifisch für den Ressourcen-Manager, den Sie verwenden. Wenn Sie eine manuelle Eintragung ausführen müssen, lesen Sie die Dokumentation für Ihren Ressourcen-Manager.

Wie unten beschrieben, können Objekte mit Transaktions Affinität in einem Pool zusammengefasst werden, während eine Transaktion aktiv ist und mit Transaktions Affinität aktiviert werden kann, wenn Sie von einem Client aufgerufen wird, der dieser Transaktion zugeordnet ist. Vor der Eintragung von Ressourcen sollten Sie zunächst die Transaktions Affinität überprüfen. Wenn das Objekt aus dem für diese Transaktion spezifischen Pool entnommen wurde, hat es bereits in dieser Transaktion gearbeitet und seine Ressourcen eingetragen.

## <a name="turning-off-automatic-enlistment"></a>Deaktivieren der automatischen Eintragung

Die automatische Eintragung muss ausgeschaltet werden, nachdem die Ressource abgerufen wurde, normalerweise im Konstruktor des Objekts. Das heißt, Sie deaktivieren die automatische Eintragung und stellen dann eine Verbindung her.

Das Deaktivieren der automatischen Eintragung kann manchmal ein sehr feines Verfahren sein, insbesondere im Fall von mehrstufigen Datenzugriffs Anbietern. Die automatische Eintragung ist manchmal mit dem Verbindungspooling gekoppelt, wie z.b. mit ODBC, und manchmal nicht, wie bei OLE DB. Möglicherweise müssen Sie sicherstellen, dass die automatische Eintragung auf mehreren Ebenen von Anbietern deaktiviert ist.

## <a name="implementing-iobjectcontrol"></a>Implementieren von IObjectControl

In einem Pool enthaltene Objekte, die an Transaktionen teilnehmen, müssen den aktuellen Status der Ressourcen überwachen, die Sie halten. Wenn das Objekt erkennt, dass es sich in einem nicht wiederverwendbaren Zustand befindet – z. b. Wenn eine Verbindung fehlerfrei ist – sollte für [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)der Wert false zurückgegeben werden. Dies hat den Effekt, dass die Objektinstanz verworfen und die aktuelle Transaktion angedockt wird.

## <a name="transaction-specific-pools"></a>Transaction-Specific Pools

Ein Pool von Objekten ist im allgemeinen homogen, und jedes in einem Pool enthaltene Objekt, das zurzeit nicht verwendet wird, kann zu einem beliebigen Client zurückkehren. Die einzige Ausnahme von dieser Regel sind Transaktions Objekte, bei denen das Objekt Pooling optimiert ist. Wenn der Client, der ein Objekt anfordert, über eine zugeordnete Transaktion verfügt, scannt com+ den Pool nach einem verfügbaren Objekt, das bereits der Transaktion zugeordnet ist. Wenn ein Objekt mit Transaktions Affinität gefunden wird, wird es an den Client zurückgegeben. Andernfalls wird ein Objekt aus dem allgemeinen Pool zurückgegeben.

Auf diese Weise werden spezielle unter Pools verwaltet, die Objekte mit Affinität für eine bestimmte Transaktion enthalten. Wenn die Transaktion ausgeführt wird oder abgebrochen wird, werden diese Objekte ohne Transaktions Affinität an den allgemeinen Pool zurückgegeben und können von jedem beliebigen Client verwendet werden.

Wenn Ihre verwalteten Ressourcen von der Komponente manuell in eine Transaktion eingetragen werden, sollten Sie daher zunächst überprüfen, ob Sie bereits eingetragen wurden. Wenn dies der Fall ist, müssen Sie sich nicht eintragen.

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

[Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



