---
title: Anzeigen von Dialog Feldern
description: Anzeigen von Dialog Feldern
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player Online Stores, Anzeigen von Dialogfeldern
- Online Stores, Anzeigen von Dialogfeldern
- Typ 1 Online Stores, Anzeigen von Dialogfeldern
- Windows Media Player Online Stores, Dialogfelder
- Online Stores, Dialogfelder
- Typ 1 Online Stores, Dialogfelder
- Anzeigen von Dialogfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723512"
---
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="3785a-110">Anzeigen von Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="3785a-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="3785a-111">Der Online Shop kann Dialogfelder über Windows Media Player aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3785a-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="3785a-112">Um dies zu erreichen, müssen Sie im Skriptcode der Ermittlungs Seite " [extern. ShowPopup](external-showpopup.md) " aufrufen und einen benutzerdefinierten Indexwert bereitstellen, der das anzuzeigende Dialogfeld darstellt.</span><span class="sxs-lookup"><span data-stu-id="3785a-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="3785a-113">Dieser Indexwert ist nur für den Online Store-Code von Bedeutung. Dieser Wert wird von Windows Media Player nicht interpretiert.</span><span class="sxs-lookup"><span data-stu-id="3785a-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="3785a-114">Windows Media Player ruft dann [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) \_ auf und übergibt g sziteminfo \_ popupurl für den *bstrinfoname* -Parameter und die Indexnummer für den *pContext* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="3785a-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="3785a-115">Das Plug-in gibt dann einen **BSTR** -Wert zurück, der die URL der Webseite enthält, die im Dialogfeld angezeigt werden soll, und der Player zeigt das Dialogfeld an.</span><span class="sxs-lookup"><span data-stu-id="3785a-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3785a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3785a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3785a-117">**Programmier Handbuch für den Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="3785a-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




