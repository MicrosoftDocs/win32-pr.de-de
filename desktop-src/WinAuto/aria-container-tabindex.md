---
title: TabIndex-Fehler bei Aria-Container
description: TabIndex-Fehler bei Aria-Container
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- Ariacontainertabindexerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388674"
---
# <a name="aria-container-tabindex-error"></a><span data-ttu-id="041e0-104">TabIndex-Fehler bei Aria-Container</span><span class="sxs-lookup"><span data-stu-id="041e0-104">ARIA Container Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="041e0-105">Text</span><span class="sxs-lookup"><span data-stu-id="041e0-105">Text</span></span>

<span data-ttu-id="041e0-106">Das-Element ist ein Fokus nutzbarer Container mit aktiven, aber ohne **TabIndex** -Wert größer oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="041e0-106">Element is a focusable container with active descendants defined but without **tabindex** value greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="041e0-107">type</span><span class="sxs-lookup"><span data-stu-id="041e0-107">Type</span></span>

<span data-ttu-id="041e0-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="041e0-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="041e0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="041e0-109">Description</span></span>

<span data-ttu-id="041e0-110">Dieser Fehler gilt für-Elemente, die über das **Aria-activenachfolger** -Attribut verfügen, nicht deaktiviert sind und das **TabIndex** -Attribut nicht auf einen Wert festgelegt ist, der größer oder gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="041e0-110">This error applies to elements that have the **aria-activedescendant** attribute, are not disabled, and do not have the **tabindex** attribute set to a value that is greater than or equal to 0.</span></span> <span data-ttu-id="041e0-111">Diese Elemente müssen sich in der Aktivier Reihenfolge befinden, da Sie für die Verarbeitung von Tastatur Ereignissen für ihre untergeordneten Elemente zuständig sind</span><span class="sxs-lookup"><span data-stu-id="041e0-111">These elements must be in tab order because they are responsible for handling keyboard events for their child elements.</span></span>

<span data-ttu-id="041e0-112">Legen Sie zum Beheben dieses Fehlers das **TabIndex** -Attribut auf einen Wert fest, der größer oder gleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="041e0-112">To fix this error, set the **tabindex** attribute to a value that is greater than or equal to 0.</span></span>

## <a name="example"></a><span data-ttu-id="041e0-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="041e0-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a><span data-ttu-id="041e0-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="041e0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="041e0-115">TabIndex Fehler bei der Aria-Container Rolle (ohne aktiven Nachfolger)</span><span class="sxs-lookup"><span data-stu-id="041e0-115">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




