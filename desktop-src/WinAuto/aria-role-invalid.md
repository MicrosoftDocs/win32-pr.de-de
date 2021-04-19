---
title: Aria-Rollen Fehler
description: Aria-Rollen Fehler
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- Ariaroleerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106341337"
---
# <a name="aria-role-error"></a><span data-ttu-id="daf57-104">Aria-Rollen Fehler</span><span class="sxs-lookup"><span data-stu-id="daf57-104">ARIA Role Error</span></span>

## <a name="text"></a><span data-ttu-id="daf57-105">Text</span><span class="sxs-lookup"><span data-stu-id="daf57-105">Text</span></span>

<span data-ttu-id="daf57-106">Das Element hat eine ungültige WAI-ARIA-Rolle.</span><span class="sxs-lookup"><span data-stu-id="daf57-106">Element has invalid WAI-ARIA role.</span></span>

## <a name="type"></a><span data-ttu-id="daf57-107">type</span><span class="sxs-lookup"><span data-stu-id="daf57-107">Type</span></span>

<span data-ttu-id="daf57-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="daf57-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="daf57-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="daf57-109">Description</span></span>

<span data-ttu-id="daf57-110">Dieser Fehler gilt für alle Elemente, die über das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="daf57-110">This error applies to all elements that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute.</span></span> <span data-ttu-id="daf57-111">Der Wert gibt an, dass das **Role** -Attribut kein gültiger Rollen Wert für die webobarrierefreiheits Initiative ist, der von der WAI-ARIA-Spezifikation definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="daf57-111">It indicates that the **role** attribute is not a valid Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value as defined by the WAI-ARIA specification.</span></span> <span data-ttu-id="daf57-112">Durch Festlegen einer gültigen Rolle wird sichergestellt, dass das Element von sprach Lesern und anderen hilfstechnologietools richtig interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="daf57-112">Setting a valid role helps ensure that the element is correctly interpreted by screen readers and other assistive technology tools.</span></span>

<span data-ttu-id="daf57-113">Legen Sie zum Beheben dieses Fehlers das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut auf einen gültigen Wert der Rolle "WAI-ARIA" fest.</span><span class="sxs-lookup"><span data-stu-id="daf57-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role value.</span></span> <span data-ttu-id="daf57-114">Beachten Sie, dass abstrakte WAI-ARIA-Rollen nicht gültig sind.</span><span class="sxs-lookup"><span data-stu-id="daf57-114">Note that abstract WAI-ARIA roles are not valid.</span></span>

## <a name="example"></a><span data-ttu-id="daf57-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="daf57-115">Example</span></span>


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a><span data-ttu-id="daf57-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="daf57-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf57-117">Fehler bei der Aria-Container Rolle</span><span class="sxs-lookup"><span data-stu-id="daf57-117">ARIA Container Role Error</span></span>](aria-container-role.md)
</dt> </dl>

 

 




