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
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="63a81-107">Navigieren zu anderen Online Stores</span><span class="sxs-lookup"><span data-stu-id="63a81-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="63a81-108">Sie können Verknüpfungen zu anderen Online speichern erstellen, die Sie besitzen oder quer zu den von anderen bereitgestellten online speichern.</span><span class="sxs-lookup"><span data-stu-id="63a81-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="63a81-109">Zu diesem Zweck müssen Sie den Schlüsselnamen für den Online Shop kennen, zu dem Sie navigieren möchten.</span><span class="sxs-lookup"><span data-stu-id="63a81-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="63a81-110">Der folgende Beispielcode zeigt eine HTML-Datei, die einen Link zum Wechseln vom Proseware Online Store zum "ServiceTask2"-Feature des southridge Video Online Store erstellt:</span><span class="sxs-lookup"><span data-stu-id="63a81-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="63a81-111">Wenn der Benutzer auf den Link klickt, wird der Benutzer von Windows Media Player aufgefordert, zum southridge-Video Speicher zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="63a81-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="63a81-112">Wenn der Benutzer dies zulässt, schaltet der Spieler die Geschäfte und navigiert zum angegebenen Aufgabenbereich und fügt die Abfrage Zeichenfolgen-Parameter an.</span><span class="sxs-lookup"><span data-stu-id="63a81-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="63a81-113">Die im vorherigen Beispiel gezeigten Abfrage Zeichenfolgen-Parameter sind benutzerdefinierte Parameter.</span><span class="sxs-lookup"><span data-stu-id="63a81-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="63a81-114">Dies bedeutet, dass der Online Shop, zu dem Sie wechseln, diese Werte erwarten und verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="63a81-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="63a81-115">Ihr Online Store (und alle Geschäfte, zu denen Sie wechseln) können Abfrage Zeichenfolgen-Parameter beliebig verwenden.</span><span class="sxs-lookup"><span data-stu-id="63a81-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63a81-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63a81-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63a81-117">**Navigieren zwischen Dienstaufgaben Bereichen**</span><span class="sxs-lookup"><span data-stu-id="63a81-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="63a81-118">**Navigation für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="63a81-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




