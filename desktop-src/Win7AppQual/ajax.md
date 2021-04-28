---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088758"
---
# <a name="ajax"></a><span data-ttu-id="43720-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="43720-103">AJAX</span></span>

<span data-ttu-id="43720-104">AJAX-Features in Windows Internet Explorer 8 wie [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) und [Dokumentübergreifendes Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) verfügen über native Eigenschaften, die mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen können.</span><span class="sxs-lookup"><span data-stu-id="43720-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="43720-105">Windows Internet Explorer macht neue Eigenschaften für bestimmte AJAX-Features verfügbar, z. B. dokumentübergreifendes [Messaging (XDM),](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)auch in Kompatibilitätsansicht.</span><span class="sxs-lookup"><span data-stu-id="43720-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="43720-106">Wenn Sie dem Ereignisobjekt benutzerdefinierte Eigenschaften hinzufügen, können diese mit diesen neuen Eigenschaften in Konflikt stehen, z. B. **der Quelle**.</span><span class="sxs-lookup"><span data-stu-id="43720-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="43720-107">Das folgende Codebeispiel funktioniert in älteren Versionen von Internet Explorer jedoch nicht in neueren Versionen, da neue Features die **Quelleigenschaft** verwenden.</span><span class="sxs-lookup"><span data-stu-id="43720-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="43720-108">Das folgende Codebeispiel zeigt, wie Sie dieses Objekt ändern können, um kompatibel zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="43720-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="43720-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43720-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43720-110">Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="43720-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



