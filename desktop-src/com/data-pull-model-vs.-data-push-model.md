---
title: Data-Pull-Modell und Data-Push-Modell
description: Data-Pull-Modell und Data-Push-Modell
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab89f61301f9116a7e826f1965bd54f75004a3a90af8c9d1a1bc13acb1fc9c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048448"
---
# <a name="data-pull-model-and-data-push-model"></a>Data-Pull-Modell und Data-Push-Modell

Ein Client eines asynchronen Monikers kann zwischen einem Daten pull- und data-push-Modell wählen, um einen asynchronen [**IMoniker::BindToStorage-Vorgang**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) zu betreiben und asynchrone Benachrichtigungen zu empfangen. Im Daten-Pull-Modell steuert der Client den Bindungsvorgang, und der Moniker stellt daten nur beim Lesen für den Client bereit. Anders ausgedrückt: Nach dem ersten Aufruf von [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))stellt der Moniker keine Daten für den Client bereit, es sei denn, der Client hat alle bereits verfügbaren Daten genutzt.

Da Daten nur so heruntergeladen werden, wie sie angefordert werden, müssen Clients, die das Daten-Pull-Modell auswählen, sicherstellen, dass diese Daten rechtzeitig gelesen werden. Bei Internetdownloads mit [URL-Monikern](url-monikers.md)schlägt der Bindungsvorgang möglicherweise fehl, wenn ein Client zu lange wartet, bevor er weitere Daten anfordert.

Im Daten-Push-Modell steuert der Moniker den asynchronen Bindungsvorgang und benachrichtigt den Client kontinuierlich, wenn neue Daten verfügbar sind. Der Client kann auswählen, ob die Daten zu einem beliebigen Zeitpunkt während des Bindungsvorgangs gelesen werden sollen, aber der Moniker führt den Bindungsvorgang unabhängig davon zum Abschluss.

Denken Sie außerdem daran, die COM-Regeln für die Speicherbelegung zu befolgen, wenn Sie asynchrone Moniker verwenden, insbesondere die folgenden:

-   Wenn eine COM-Schnittstelle oder ein Funktionsaufruf einen Puffer (Zeichenfolge oder andere) an seinen Client zurückgibt, ist der Client für die Freigabe des Arbeitsspeichers durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)verantwortlich.
-   Wenn eine COM-Schnittstelle oder -Funktion einen Puffer vom Client erfordert, muss der Client diesen Puffer mit [**coTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) zuordnen, und der Aufgerufene muss ihn freigeben.

Achten Sie darauf, diese Regeln zu befolgen, wenn Sie Zeichenfolgen oder Puffer zuweisen, die an asynchrone Moniker übergeben werden, und denken Sie daran, den von asynchronen Monikern zurückgegebenen Arbeitsspeicher freizugeben. Ausführliche Informationen finden Sie unter [Verwalten der Speicherbelegung](the-com-library.md) und verwandte Themen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 