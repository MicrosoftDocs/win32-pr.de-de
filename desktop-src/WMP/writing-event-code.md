---
title: Schreiben von Ereignis Code
description: Schreiben von Ereignis Code
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player Skins, Schreiben von Code
- Skins, Schreiben von Code
- Ereignisse, Schreiben von Code
- Schreiben von Code für Skins, Informationen zu
- Windows Media Player Skins, Ereignisse
- Skins, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037569"
---
# <a name="writing-event-code"></a><span data-ttu-id="bdd12-109">Schreiben von Ereignis Code</span><span class="sxs-lookup"><span data-stu-id="bdd12-109">Writing Event Code</span></span>

<span data-ttu-id="bdd12-110">Ereignisse werden ähnlich wie Attribute behandelt.</span><span class="sxs-lookup"><span data-stu-id="bdd12-110">Events are treated similarly to attributes.</span></span> <span data-ttu-id="bdd12-111">Sie müssen dem Ereignis einen Wert übergeben, und der Wert ist der Code, den Sie ausführen möchten, wenn das Ereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="bdd12-111">You must give the event a value, and the value is the code you want to run when the event happens.</span></span> <span data-ttu-id="bdd12-112">Das Wort "on" wird am Anfang des Ereignis namens hinzugefügt. das Click-Ereignis wird z. b. auf **OnClick** fest.</span><span class="sxs-lookup"><span data-stu-id="bdd12-112">The word "on" is added to the front of the event name; for example, the click event will become **onclick**.</span></span>

<span data-ttu-id="bdd12-113">Der Ereignis Wert ist in doppelten Anführungszeichen und beginnt mit dem Wort JScript gefolgt von einem Doppelpunkt.</span><span class="sxs-lookup"><span data-stu-id="bdd12-113">The event value is in double quotes and starts with the word JScript followed by a colon.</span></span> <span data-ttu-id="bdd12-114">Der Code, den Sie ausführen möchten, wird als nächstes angezeigt, gefolgt von einem Semikolon und den schließenden doppelten Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="bdd12-114">The code you want to run comes next, followed by a semicolon and the closing double quotes.</span></span> <span data-ttu-id="bdd12-115">Wenn Sie z. b. die Wiedergabe beenden möchten, wenn der Benutzer auf eine Schaltfläche klickt, geben Sie Folgendes als Attribut in den Code des **Schalt** Flächen Elements ein:</span><span class="sxs-lookup"><span data-stu-id="bdd12-115">For example, to stop playing when the user clicks on a button, type the following as an attribute in your **BUTTON** element code:</span></span>


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



<span data-ttu-id="bdd12-116">Wenn Sie über einen Code verfügen, der Anführungszeichen erfordert, verwenden Sie einfache Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="bdd12-116">If you have a code that requires quotes, use single quotes.</span></span> <span data-ttu-id="bdd12-117">Es muss sorgfältig vorgegangen werden, wenn Anführungszeichen verwendet werden, damit Sie ordnungsgemäß ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="bdd12-117">Care must be taken when using quotation marks so that they are balanced properly.</span></span> <span data-ttu-id="bdd12-118">Im folgenden finden Sie ein Beispiel für die Verwendung beider Typen:</span><span class="sxs-lookup"><span data-stu-id="bdd12-118">Here is an example of using both types:</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



<span data-ttu-id="bdd12-119">Sie können auch die Attribute Ihrer Skin ändern, wenn Sie ein externes Ereignis verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bdd12-119">You can also change attributes of your skin when handling an external event.</span></span> <span data-ttu-id="bdd12-120">Wenn Sie z. b. eine Ansicht mit dem Namen MyView schließen möchten, können Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="bdd12-120">For example, to close a view named myView, you could type:</span></span>


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a><span data-ttu-id="bdd12-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bdd12-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdd12-122">**Behandeln von Ereignissen**</span><span class="sxs-lookup"><span data-stu-id="bdd12-122">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




