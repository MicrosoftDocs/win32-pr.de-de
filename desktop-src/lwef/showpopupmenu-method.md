---
title: ShowPopupMenu-Methode
description: ShowPopupMenu-Methode
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339795"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="dac4a-103">ShowPopupMenu-Methode</span><span class="sxs-lookup"><span data-stu-id="dac4a-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="dac4a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="dac4a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dac4a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dac4a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dac4a-106">Zeigt das Popup Menü des Zeichens an der angegebenen Position an.</span><span class="sxs-lookup"><span data-stu-id="dac4a-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="dac4a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="dac4a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dac4a-108">*Büros. ***Zeichen ("*** Merkmal-ID ***"). ShowPopupMenu*** x, y*</span><span class="sxs-lookup"><span data-stu-id="dac4a-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="dac4a-109">Teil</span><span class="sxs-lookup"><span data-stu-id="dac4a-109">Part</span></span> | <span data-ttu-id="dac4a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dac4a-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac4a-111">*x*</span><span class="sxs-lookup"><span data-stu-id="dac4a-111">*x*</span></span>  | <span data-ttu-id="dac4a-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dac4a-112">Required.</span></span> <span data-ttu-id="dac4a-113">Ein ganzzahliger Wert, der die horizontale (*x*) Bildschirm Koordinate angibt, mit der das Menü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dac4a-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="dac4a-114">Diese Koordinaten müssen in Pixel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dac4a-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="dac4a-115">*y*</span><span class="sxs-lookup"><span data-stu-id="dac4a-115">*y*</span></span>  | <span data-ttu-id="dac4a-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dac4a-116">Required.</span></span> <span data-ttu-id="dac4a-117">Ein *ganzzahliger* Wert, der die vertikale Bildschirm Koordinate (y) angibt, mit der das Menü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dac4a-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="dac4a-118">Diese Koordinaten müssen in Pixel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dac4a-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dac4a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dac4a-119">Remarks</span></span>

<span data-ttu-id="dac4a-120">Der-Agent zeigt automatisch das Popup Menü des Zeichens an, wenn der Benutzer mit der rechten Maustaste auf das Zeichen klickt.</span><span class="sxs-lookup"><span data-stu-id="dac4a-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="dac4a-121">Wenn Sie [**autopopupmenu**](autopopupmenu-property.md) auf **false** festlegen, können Sie mit dieser Methode das Menü anzeigen.</span><span class="sxs-lookup"><span data-stu-id="dac4a-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="dac4a-122">Das Menü wird angezeigt, bis der Benutzer einen Befehl auswählt oder ein anderes Menü anzeigt.</span><span class="sxs-lookup"><span data-stu-id="dac4a-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="dac4a-123">Es kann jeweils nur ein Popup Menü angezeigt werden. Daher wird durch Aufrufe dieser Methode das erste Menü abgebrochen (entfernt).</span><span class="sxs-lookup"><span data-stu-id="dac4a-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="dac4a-124">Diese Methode sollte nur aufgerufen werden, wenn die Client Anwendung der aktive Client des Zeichens ist. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="dac4a-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="dac4a-125">Um den Erfolg dieser Methode zu ermitteln, können Sie Sie als Funktion und einen booleschen Wert zurückgeben, der angibt, ob die Methode erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dac4a-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="dac4a-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dac4a-126">See Also</span></span>

[<span data-ttu-id="dac4a-127">**Autopopupmenu (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="dac4a-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 




