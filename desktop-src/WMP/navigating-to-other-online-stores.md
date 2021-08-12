---
title: Navigieren zu anderen Onlineshops
description: Navigieren zu anderen Onlineshops
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player Onlineshops, Navigieren
- Onlineshops, Navigieren
- Geben Sie 2 Onlineshops ein, und navigieren Sie
- Navigieren in 2 Onlineshops
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1b2cb120ac161fd92bf8d35826b9dc096c95c37d916f19eb2aeb7362aabe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574433"
---
# <a name="navigating-to-other-online-stores"></a>Navigieren zu anderen Onlineshops

Sie können Links zu anderen Onlineshops erstellen, deren Eigentümer Sie sind, oder eine Querverknüpfung mit Onlineshops erstellen, die von anderen angeboten werden. Hierzu müssen Sie den Schlüsselnamen für den Onlineshop kennen, zu dem Sie navigieren möchten.

Der folgende Beispielcode zeigt HTML, mit dem ein Link erstellt wird, um vom Proseware-Onlineshop zum Feature "ServiceTask2" des Onlinespeichers "South australia Video" zu wechseln:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Wenn der Benutzer auf den Link klickt, fordert Windows Media Player den Benutzer auf, zum South australia Video Store zu wechseln. Wenn der Benutzer dies zulässt, wechselt der Player zum Speichern und Navigieren zum angegebenen Aufgabenbereich und fügt die Abfragezeichenfolgenparameter an. Die im vorherigen Beispiel gezeigten Abfragezeichenfolgenparameter sind benutzerdefinierte Parameter. Dies bedeutet, dass der Onlineshop, zu dem Sie wechseln, diese Werte erwarten und verarbeiten muss. Ihr Onlineshop (und jeder Speicher, zu dem Sie wechseln) kann Abfragezeichenfolgenparameter auf beliebige Weise verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Navigieren zwischen Dienstaufgabenbereichen**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navigation für Onlineshops vom Typ 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




