---
title: Firstchildlastchildmismatch
description: Firstchildlastchildmismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388494"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="ae752-103">Firstchildlastchildmismatch</span><span class="sxs-lookup"><span data-stu-id="ae752-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="ae752-104">Text</span><span class="sxs-lookup"><span data-stu-id="ae752-104">Text</span></span>

<span data-ttu-id="ae752-105">Wenn Sie von {0} dem getesteten Knoten aus aufrufen und dann wiederholt aufrufen {1} , wird das folgende untergeordnete Element beendet: {2} .</span><span class="sxs-lookup"><span data-stu-id="ae752-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="ae752-106">Dies entsprach nicht dem Ergebnis des Abrufs von {3} auf dem getesteten Knoten, der Folgendes zurückgegeben hat: {4} .</span><span class="sxs-lookup"><span data-stu-id="ae752-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="ae752-107">Stattdessen sollte das untergeordnete Element als übergeordnetes Element für den Testknoten melden.</span><span class="sxs-lookup"><span data-stu-id="ae752-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="ae752-108">type</span><span class="sxs-lookup"><span data-stu-id="ae752-108">Type</span></span>

<span data-ttu-id="ae752-109">Fehler</span><span class="sxs-lookup"><span data-stu-id="ae752-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="ae752-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae752-110">Description</span></span>

<span data-ttu-id="ae752-111">Beim Navigieren zwischen den untergeordneten Elementen liegt ein Problem vor.</span><span class="sxs-lookup"><span data-stu-id="ae752-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="ae752-112">1.</span><span class="sxs-lookup"><span data-stu-id="ae752-112">1.</span></span> <span data-ttu-id="ae752-113">Eine falsche oder ungültige Implementierung der Benutzeroberflächen Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ae752-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="ae752-114">Dieses Problem kann Navigationsprobleme bei automatisierten Tools verursachen, da das Durchlaufen von Elementen möglicherweise erratisch und unvorhersagbar ist.</span><span class="sxs-lookup"><span data-stu-id="ae752-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ae752-115">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="ae752-115">Possible causes</span></span>

<span data-ttu-id="ae752-116">Eine falsche oder ungültige Implementierung der Benutzeroberflächen Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ae752-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae752-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae752-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae752-118">**Iuiautomationelement:: getcachedparent**</span><span class="sxs-lookup"><span data-stu-id="ae752-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="ae752-119">**Iuiautomationtreewalker**</span><span class="sxs-lookup"><span data-stu-id="ae752-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




