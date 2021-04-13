---
title: Kontextmenüs
description: Kontextmenüs
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player Online Stores, Kontextmenüs
- Online Stores, Kontextmenüs
- Typ 1 Online Stores, Kontextmenüs
- Windows Media Player Online Stores, benutzerdefinierte Kontextmenüs
- Online Stores, benutzerdefinierte Kontextmenüs
- Typ 1 Online Stores, benutzerdefinierte Kontextmenüs
- Kontextmenüs
- Benutzerdefinierte Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba3ed52b408651607cb1f6dab1a04f53282d3ef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389838"
---
# <a name="context-menus"></a><span data-ttu-id="07d2d-111">Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="07d2d-111">Context Menus</span></span>

<span data-ttu-id="07d2d-112">Online Stores können benutzerdefinierte Kontextmenüs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="07d2d-112">Online stores can provide custom context menus.</span></span> <span data-ttu-id="07d2d-113">Hierzu implementiert das Online Store-Plug-in die Methode [iwmpcontentpartner:: GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) .</span><span class="sxs-lookup"><span data-stu-id="07d2d-113">To do this, the online store plug-in implements the [IWMPContentPartner::GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) method.</span></span> <span data-ttu-id="07d2d-114">Windows Media Player ruft diese Methode auf, um Informationen über den Speicherort in der Benutzeroberfläche bereitzustellen, auf der das Kontextmenü angezeigt wird (in dem der Benutzer mit der rechten Maustaste geklickt hat).</span><span class="sxs-lookup"><span data-stu-id="07d2d-114">Windows Media Player calls this method to provide information about the location in the user interface where the context menu is displayed (where the user right-clicked).</span></span> <span data-ttu-id="07d2d-115">Das Plug-in gibt ein Array von [wmpcontextmenuinfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) -Strukturen zurück, die die einzelnen Kontextmenü Elemente einschließlich einer Befehls-ID für jede beschreiben.</span><span class="sxs-lookup"><span data-stu-id="07d2d-115">The plug-in returns an array of [WMPContextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) structures that describe each context menu item, including a command ID for each.</span></span>

<span data-ttu-id="07d2d-116">Nachdem der Windows-Media Player das Array abgerufen hat, verwendet der Player das Array, um das Kontextmenü zu erstellen, das der Benutzer sieht.</span><span class="sxs-lookup"><span data-stu-id="07d2d-116">After Windows Media Player has retrieved the array, the Player uses the array to build the context menu the user sees.</span></span> <span data-ttu-id="07d2d-117">Wenn der Benutzer im Kontextmenü auf ein Element klickt, ruft der Player [iwmpcontentpartner:: InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)auf und übergibt dabei die Befehls-ID, die dem Menü Element über den *dwcommandid* -Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="07d2d-117">When the user clicks an item in the context menu, the Player calls [IWMPContentPartner::InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand), passing the command ID associated with the menu item through the *dwCommandID* parameter.</span></span> <span data-ttu-id="07d2d-118">Der Player übergibt außerdem einen Bibliotheks Speicherort Wert und ein Array von IDs, die die Elemente darstellen, für die das Menü aufgerufen wurde, z. b. ein Array von Track-IDs.</span><span class="sxs-lookup"><span data-stu-id="07d2d-118">The Player also passes a library location value and an array of IDs that represents the items the menu was invoked upon, such as an array of track IDs.</span></span> <span data-ttu-id="07d2d-119">Wenn Sie diese Informationen verwenden, kann das Plug-in jeden geeigneten Prozess als Reaktion auf den Maus Klick des Benutzers starten.</span><span class="sxs-lookup"><span data-stu-id="07d2d-119">By using this information, the plug-in can start any appropriate process in response to the user's mouse click.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07d2d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07d2d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07d2d-121">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="07d2d-121">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




