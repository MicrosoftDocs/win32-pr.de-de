---
title: Fehler bei der Aria-Container Rolle
description: Fehler bei der Aria-Container Rolle
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- Ariacontainerroleerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948024"
---
# <a name="aria-container-role-error"></a><span data-ttu-id="8f6d3-104">Fehler bei der Aria-Container Rolle</span><span class="sxs-lookup"><span data-stu-id="8f6d3-104">ARIA Container Role Error</span></span>

## <a name="text"></a><span data-ttu-id="8f6d3-105">Text</span><span class="sxs-lookup"><span data-stu-id="8f6d3-105">Text</span></span>

<span data-ttu-id="8f6d3-106">Das Element, für das " **Active-** Nachfolger" definiert ist, besitzt keine Container Rolle (**ComboBox**, **Grid**, **ListBox**, **Menu**, **Menüleiste**, **Radio Group**, **Tree**, **treegrid**, **TabList**, **Row**).</span><span class="sxs-lookup"><span data-stu-id="8f6d3-106">Element with **active-descendant** defined does not have a container role (**combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tree**, **treegrid**, **tablist**, **row**).</span></span>

## <a name="type"></a><span data-ttu-id="8f6d3-107">type</span><span class="sxs-lookup"><span data-stu-id="8f6d3-107">Type</span></span>

<span data-ttu-id="8f6d3-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="8f6d3-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="8f6d3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f6d3-109">Description</span></span>

<span data-ttu-id="8f6d3-110">Dieser Fehler gilt für-Elemente, die über das **Aria-activenachfolger** -Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="8f6d3-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="8f6d3-111">Ein Element scheint ein Container zu sein, für den das Attribut " **Aria-activenachfolger** " festgelegt ist, aber das Rollen Attribut des Elements hat keinen Wert, der für einen Container gültig ist.</span><span class="sxs-lookup"><span data-stu-id="8f6d3-111">An element appears to be a container that has the **aria-activedescendant** attribute set, but the element's role attribute doesn’t have a value that is valid for a container.</span></span>

<span data-ttu-id="8f6d3-112">Um diesen Fehler zu beheben, legen Sie das **Role** -Attribut auf eine webressbarrierefreiheits-Initiative zugreifen, auf die der Rollen Wert "Ria-Aria" zugreifen kann, der für ein Containerelement gültig ist: **ComboBox**, **Grid**, **ListBox**, **Menu**, **Menüleiste**, **Radio Group**, **TabList**, **Tree** oder **treegrid**.</span><span class="sxs-lookup"><span data-stu-id="8f6d3-112">To fix this error, set the **role** attribute to a Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role value that is valid for a container element: **combobox**, **grid**, **listbox**, **menu**, **menubar**, **radiogroup**, **tablist**, **tree**, or **treegrid**.</span></span>

## <a name="example"></a><span data-ttu-id="8f6d3-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8f6d3-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1">
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>
```



## <a name="related-topics"></a><span data-ttu-id="8f6d3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f6d3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f6d3-115">Aria-Rollen Fehler</span><span class="sxs-lookup"><span data-stu-id="8f6d3-115">ARIA Role Error</span></span>](aria-role-invalid.md)
</dt> </dl>

 

 




