---
description: Implementieren eines com+-Ressourcen Verteilers
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementieren eines com+-Ressourcen Verteilers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127549"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementieren eines com+-Ressourcen Verteilers

Die folgenden Schritte beschreiben ein allgemeines Verfahren zum Implementieren eines com+-Ressourcen Verteilers:

1.  Entscheiden Sie sich für das **restypid** -Format, in dem die Unterschiede zwischen den Ressourcen voneinander kategorisiert werden.

2.  Verwenden Sie die Header Datei bzw. die Bibliothek "mtxdm. h" und "mtxdm. lib".

3.  Erstellen Sie eine DLL, die die [**idispenser Server Driver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) -Schnittstelle und die API implementiert, die Sie für Anwendungen verfügbar machen möchten.

4.  Aufrufen der [**getdispenser-Manager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) -Funktion beim Start ([*DllMain*](/windows/desktop/Dlls/dllmain) oder ersten Aufrufen der Dispenser-API). Dies gibt einen Zeiger auf die [**idispenser Manager Manager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) -Schnittstelle des Dispenser-Managers zurück.

5.  Wenden Sie [**idispenser Server Manager:: registerdispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser)an, und übergeben Sie einen Zeiger auf Ihre Implementierung von [**idispenser Server Driver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Dies bewirkt, dass der Dispenser-Manager einen Halter (Pooling-Manager) für den Ressourcen Verteiler erstellt und dann den Zeiger auf Ihre [**ihälter**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) -Schnittstelle zurückgibt.

6.  Speichern Sie diesen Zeiger, damit Sie [**ihälter:: Zuweisung**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) und [**ihälter:: freeresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)aufrufen können.

7.  Sie können jetzt (als Reaktion auf Aufrufe ihrer API) Aufrufe an " [**zugriffsource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) " und " [**freeresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)" tätigen. " **Zuweisung** " ist zunächst eine Antwort auf die [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) -Methode, **die später jedoch** aus dem wachsenden Ressourcenpool bedient wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> <dt>

[Com+-Ressourcen Verteiler Schnittstellen](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
