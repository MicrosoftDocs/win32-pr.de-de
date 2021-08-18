---
description: Implementieren eines COM+-Ressourcenverteilers
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementieren eines COM+-Ressourcenverteilers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9c37de2a4910af908bdc3f2e38f1c1b55699b133a59a818b8a09236f8c0a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547892"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implementieren eines COM+-Ressourcenverteilers

In den folgenden Schritten wird ein allgemeines Verfahren zum Implementieren eines COM+-Ressourcenverteilers beschrieben:

1.  Entscheiden Sie sich für das **RESTYPID-Format,** das kategorisiert, wie sich Ihre Ressourcen voneinander unterscheiden.

2.  Verwenden Sie die Headerdatei bzw. Bibliothek "Mtxdm.h" und "Mtxdm.lib".

3.  Erstellen Sie eine DLL, die die [**IDispenserDriver-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) und die API implementiert, die Sie für Anwendungen verfügbar machen möchten.

4.  Rufen Sie beim Start ([*DllMain*](/windows/desktop/Dlls/dllmain) oder erster Aufruf der Verteiler-API) die [**GetDispenserManager-Funktion**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) auf. Dadurch wird ein Zeiger auf die [**IDispenserManager-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) des Verteiler-Managers zurückgegeben.

5.  Rufen Sie [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser)auf, und übergeben Sie einen Zeiger auf Ihre Implementierung von [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Dies bewirkt, dass der Verteiler-Manager einen Halter (Pooling-Manager) für Ihren Ressourcenspender erstellt und dann den Zeiger auf Ihre [**IHolder-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) zurückgibt.

6.  Store diesen Zeiger, damit Sie [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) und [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)aufrufen können.

7.  Sie können jetzt (als Reaktion auf Aufrufe Ihrer API) Aufrufe von [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) und [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource)durchführen. **AllocResource** antwortet zunächst, indem es die [**CreateResource-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) zurückruft, aber spätere **AllocResource-Aufrufe** werden aus dem wachsenden Ressourcenpool bedient.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Ressourcenverteilerkonzepte](com--resource-dispenser-concepts.md)
</dt> <dt>

[COM+-Ressourcenverteilerschnittstellen](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
