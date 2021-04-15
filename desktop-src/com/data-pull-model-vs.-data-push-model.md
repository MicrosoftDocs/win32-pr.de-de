---
title: Data-Pull Modell und Data-Push Modell
description: Data-Pull Modell und Data-Push Modell
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391092"
---
# <a name="data-pull-model-and-data-push-model"></a>Data-Pull Modell und Data-Push Modell

Ein Client mit einem asynchronen Moniker kann zwischen einem datenpull-und einem datenpushmodell wählen, um einen asynchronen [**IMoniker:: bindesstorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) -Vorgang zu tätigen und asynchrone Benachrichtigungen zu empfangen. Im Data-Pull-Modell steuert der Client den Bindungs Vorgang, und der Moniker stellt dem Client nur beim Lesen Daten bereit. Das heißt, dass der Moniker nach dem ersten Aufruf von [**ibindstatus-Callback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))keine Daten für den Client bereitstellt, es sei denn, der Client hat alle bereits verfügbaren Daten verbraucht.

Da Daten nur nach Anforderung heruntergeladen werden, müssen die Clients, die das datenpull-Modell auswählen, sicherstellen, dass diese Daten rechtzeitig gelesen werden. Im Fall von Internet Downloads mit [URL-Monikern](url-monikers.md)schlägt der Bindungs Vorgang möglicherweise fehl, wenn ein Client zu lange wartet, bevor mehr Daten angefordert werden.

Im Daten Push-Modell steuert der Moniker den asynchronen Bindungs Vorgang und benachrichtigt den Client kontinuierlich, wenn neue Daten verfügbar sind. Der Client kann entscheiden, ob die Daten zu einem beliebigen Zeitpunkt während des Bindungs Vorgangs gelesen werden sollen. der Moniker führt den Bindungs Vorgang jedoch unabhängig von der Beendigung durch.

Beachten Sie auch, dass Sie bei der Verwendung asynchroner Moniker daran denken müssen, die com-Regeln für die Speicher Belegung zu befolgen, insbesondere die folgenden:

-   Wenn eine COM-Schnittstelle oder ein Funktionsaufruf einen Puffer (Zeichenfolge oder einen anderen) an den Client zurückgibt, ist der Client für die Freigabe des Arbeitsspeichers durch Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)verantwortlich.
-   Wenn eine COM-Schnittstelle oder-Funktion einen Puffer von Ihrem Client erfordert, muss der Client diesen Puffer mithilfe von [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) zuordnen, und der aufgerufene muss ihn freigeben.

Achten Sie darauf, dass Sie diese Regeln befolgen, wenn Sie Zeichen folgen oder Puffer zuordnen, die an asynchrone Moniker übermittelt werden, und denken Sie daran, den von asynchronen Monikern zurückgegebenen Arbeitsspeicher Ausführliche Informationen finden Sie unter [Verwalten der Speicher Belegung](the-com-library.md) und verwandter Themen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 