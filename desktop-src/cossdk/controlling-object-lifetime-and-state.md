---
description: Steuern der Objekt Lebensdauer und des Zustands
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Steuern der Objekt Lebensdauer und des Zustands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343607"
---
# <a name="controlling-object-lifetime-and-state"></a>Steuern der Objekt Lebensdauer und des Zustands

Ein in einem Pool zusammengefasste Objekt kann daran teilnehmen, wie com+ seine Aktivität im Pool durch Implementieren von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)verwaltet. Wenn ein in einem Pool zusammengestelltes Objekt erstellt wird, wird es in ein größeres Objekt aggregiert, das das Objekt verwaltet, indem die folgenden Methoden für **IObjectControl** an den regulären Punkten im Lebenszyklus des Objekts aufgerufen werden:

-   [**Aktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)– wird aufgerufen, wenn das Objekt an einen Client zurückgegeben wird, das in einem bestimmten Kontext aktiviert ist.
-   [**Deaktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)– wird aufgerufen, wenn ein Objekt vom Client freigegeben wird, oder im Fall eines JIT-aktivierten Objekts, wenn es deaktiviert wird.
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)– wird aufgerufen, wenn ein Objekt an den allgemeinen Pool zurückgegeben werden soll.

Die Implementierung von [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) ist optional, mit Ausnahme von transaktionalen Objekten, die immer [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) implementieren sollten, um den Status der Ressourcen zu überwachen, die Sie enthalten. In den meisten Fällen empfiehlt es sich jedoch, **IObjectControl** zu implementieren, da es eine effiziente Möglichkeit bietet, das Verhalten eines in einem Pool zusammen gepoolten Objekts zu verwalten, wie unten beschrieben.

## <a name="performing-context-specific-initialization"></a>Ausführen Context-Specific Initialisierung

Mithilfe von " [**aktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)" können Sie das Objekt im Kontext initialisieren, in dem es für einen bestimmten Client aktiviert ist. Um z. b. zu ermitteln, ob das Objekt Transaktions Affinität aufweist (seine Ressourcen sind möglicherweise bereits eingetragen), erhalten Sie möglicherweise die Transaktions-ID, die dem Kontext zugeordnet ist.

In der Regel verwenden Sie " [**aktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)", um eine Initialisierung durchzuführen, die für alle Methoden konsistent ist, die vom-Objekt verfügbar gemacht werden, und behandelt diese als kontextspezifischen Teil des-Konstruktors des Objekts.

## <a name="cleaning-up-any-client-state"></a>Bereinigen eines beliebigen Client Zustands

Mithilfe von " [**Deaktivieren**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)" können Sie jeden Client spezifischen Zustand entfernen, der möglicherweise vorhanden ist, damit das Objekt in einem vollständig generischen Zustand an den Pool zurückkehrt und dann von jedem Client verwendet werden kann, ohne die Sicherheit oder Isolation zu beeinträchtigen.

## <a name="controlling-reuse-of-the-object"></a>Steuern der Wiederverwendung des Objekts

Mithilfe von [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)können Sie den internen Zustand Ihres Objekts überwachen und melden, ob er für seine Wiederverwendung geeignet ist. Wenn " **CanBePooled** " den Wert "true" zurückgibt und der Pool "Maximum" nicht erreicht wurde, wird das Objekt wieder im allgemeinen Pool abgelegt. Wenn **CanBePooled** false zurückgibt, wird das-Objekt verworfen. Im Fall von transaktionalen Komponenten wird die aktuelle Transaktion durch Zurückgeben von "false" unterbunden.

In der Regel behalten Sie einen globalen Datenmember für das Objekt bei, und wenn Sie eine Verbindung mit einem ungültigen Zustand erkennen oder eine Ressource in einem fehlerhaften Zustand haben, legen Sie diese so fest, dass Sie die aktuelle Situation widerspiegelt, und geben Sie Sie über " [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)" zurück.

Wenn ein Objekt keine [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)implementiert, werden die Instanzen weiterhin wieder verwendet, bis die maximale Pool Ebene erreicht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings.md)
</dt> <dt>

[Funktionsweise des Objekt Pooling](how-object-pooling-works.md)
</dt> <dt>

[Verbessern der Leistung durch Objekt Pooling](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling von transaktionalen Objekten](pooling-transactional-objects.md)
</dt> <dt>

[Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



