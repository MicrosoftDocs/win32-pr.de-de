---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960804"
---
# <a name="ajax"></a><span data-ttu-id="3332a-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="3332a-103">AJAX</span></span>

<span data-ttu-id="3332a-104">AJAX-Features in Windows Internet Explorer 8, wie [**XDR (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) und [Cross-Document Messaging (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) , verfügen über systemeigene Eigenschaften, die möglicherweise mit vorhandenen benutzerdefinierten Eigenschaften in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="3332a-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="3332a-105">Windows Internet Explorer macht neue Eigenschaften für bestimmte AJAX-Features verfügbar, wie z. b. [Cross-Document Messaging (xdm)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), auch in der Kompatibilitäts Ansicht.</span><span class="sxs-lookup"><span data-stu-id="3332a-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="3332a-106">Wenn Sie dem Ereignis Objekt benutzerdefinierte Eigenschaften hinzufügen, können Sie mit diesen neuen Eigenschaften, z. b. der **Quelle**, in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="3332a-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="3332a-107">Das folgende Codebeispiel funktioniert in älteren Versionen von Internet Explorer, aber nicht in neueren Versionen, da neue Features die **Source** -Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="3332a-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="3332a-108">Im folgenden Codebeispiel wird gezeigt, wie Sie dieses Objekt ändern können, damit es kompatibel bleibt.</span><span class="sxs-lookup"><span data-stu-id="3332a-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="3332a-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3332a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3332a-110">Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht</span><span class="sxs-lookup"><span data-stu-id="3332a-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



