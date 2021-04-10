---
title: Navigieren zu anderen Online Stores
description: Navigieren zu anderen Online Stores
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player Online Stores, navigieren
- Online Stores, navigieren
- Geben Sie 2 Online Stores ein, navigieren Sie zu
- Navigieren zu Typ 2 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309187"
---
# <a name="navigating-to-other-online-stores"></a>Navigieren zu anderen Online Stores

Sie können Verknüpfungen zu anderen Online speichern erstellen, die Sie besitzen oder quer zu den von anderen bereitgestellten online speichern. Zu diesem Zweck müssen Sie den Schlüsselnamen für den Online Shop kennen, zu dem Sie navigieren möchten.

Der folgende Beispielcode zeigt eine HTML-Datei, die einen Link zum Wechseln vom Proseware Online Store zum "ServiceTask2"-Feature des southridge Video Online Store erstellt:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Wenn der Benutzer auf den Link klickt, wird der Benutzer von Windows Media Player aufgefordert, zum southridge-Video Speicher zu wechseln. Wenn der Benutzer dies zulässt, schaltet der Spieler die Geschäfte und navigiert zum angegebenen Aufgabenbereich und fügt die Abfrage Zeichenfolgen-Parameter an. Die im vorherigen Beispiel gezeigten Abfrage Zeichenfolgen-Parameter sind benutzerdefinierte Parameter. Dies bedeutet, dass der Online Shop, zu dem Sie wechseln, diese Werte erwarten und verarbeiten muss. Ihr Online Store (und alle Geschäfte, zu denen Sie wechseln) können Abfrage Zeichenfolgen-Parameter beliebig verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Navigieren zwischen Dienstaufgaben Bereichen**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navigation für den Typ 2-Online Speicher**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




