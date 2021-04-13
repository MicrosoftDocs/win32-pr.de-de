---
title: Page-Eigenschaft
description: Page-Eigenschaft
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388291"
---
# <a name="page-property"></a><span data-ttu-id="e961f-103">Page-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e961f-103">Page Property</span></span>

<span data-ttu-id="e961f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e961f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e961f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e961f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e961f-106">Gibt die im Eigenschaften Blatt des Microsoft-Agents angezeigte Seite zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="e961f-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="e961f-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e961f-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="e961f-108">\*Agent \* \* *. PropertySheet.Page*- \*  \[  =  *Zeichenfolge*\]</span><span class="sxs-lookup"><span data-stu-id="e961f-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="e961f-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e961f-109">Part</span></span>     | <span data-ttu-id="e961f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e961f-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e961f-111">*string*</span><span class="sxs-lookup"><span data-stu-id="e961f-111">*string*</span></span> | <span data-ttu-id="e961f-112">Ein Zeichen folgen Ausdruck mit einem der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="e961f-112">A string expression with one of the following values.</span></span> <span data-ttu-id="e961f-113">**"Sprache"** Zeigt die Seite für die Spracheingabe an.</span><span class="sxs-lookup"><span data-stu-id="e961f-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="e961f-114">**"Ausgabe"** Zeigt die Ausgabe Seite an.</span><span class="sxs-lookup"><span data-stu-id="e961f-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="e961f-115">**"Copyright"** Zeigt die Copyright Seite an.</span><span class="sxs-lookup"><span data-stu-id="e961f-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e961f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e961f-116">Remarks</span></span>

<span data-ttu-id="e961f-117">Wenn keine Sprach-Engine installiert ist, hat das Festlegen der **Seite** auf **"Speech"** keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="e961f-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="e961f-118">Außerdem muss die **sichtbare** Eigenschaft des Fensters auf **true** festgelegt werden, damit der Benutzer die Seite sehen kann.</span><span class="sxs-lookup"><span data-stu-id="e961f-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="e961f-119">Der Benutzer kann diese Eigenschaft überschreiben.</span><span class="sxs-lookup"><span data-stu-id="e961f-119">The user can override this property.</span></span>

 

 

 





