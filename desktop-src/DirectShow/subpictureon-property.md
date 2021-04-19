---
description: Die subpictureon-Eigenschaft legt den aktuellen Teil Bild Zustand fest oder ruft ihn ab (ein oder aus).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Subpictureon (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369818"
---
# <a name="subpictureon-property"></a><span data-ttu-id="be5ce-103">Subpictureon (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="be5ce-103">SubpictureOn Property</span></span>

> [!Note]  
> <span data-ttu-id="be5ce-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be5ce-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="be5ce-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="be5ce-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="be5ce-106">Die- `SubpictureOn` Eigenschaft legt den aktuellen Teil Bild Zustand fest oder ruft ihn ab (ein oder aus).</span><span class="sxs-lookup"><span data-stu-id="be5ce-106">The `SubpictureOn` property sets or retrieves the current subpicture state (on or off).</span></span>

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a><span data-ttu-id="be5ce-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be5ce-107">Return Value</span></span>

<span data-ttu-id="be5ce-108">Gibt einen booleschen Wert zurück, der angibt, ob das untergeordnete Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="be5ce-108">Returns a Boolean value indicating whether the subpicture is displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="be5ce-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be5ce-109">Remarks</span></span>

<span data-ttu-id="be5ce-110">Diese Eigenschaft wirkt sich nicht auf die Anzeige von Untertiteln aus.</span><span class="sxs-lookup"><span data-stu-id="be5ce-110">This property does not affect display of Closed Captions.</span></span> <span data-ttu-id="be5ce-111">Untertitel werden in den Videostream eingebettet.</span><span class="sxs-lookup"><span data-stu-id="be5ce-111">Closed Captions are embedded within the video stream.</span></span> <span data-ttu-id="be5ce-112">DVD-Teilbilder werden in einem separaten Stream transportiert.</span><span class="sxs-lookup"><span data-stu-id="be5ce-112">DVD subpictures are transported on a separate stream.</span></span>

<span data-ttu-id="be5ce-113">Wenn der subbildstream mithilfe von [**currentsubpicturestream**](currentsubpicturestream-property.md)geändert wird, wird die `SubpictureOn` Eigenschaft in **true** geändert.</span><span class="sxs-lookup"><span data-stu-id="be5ce-113">When the subpicture stream is changed using [**CurrentSubpictureStream**](currentsubpicturestream-property.md), the `SubpictureOn` property toggles to **True**.</span></span>

<span data-ttu-id="be5ce-114">Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false.</span><span class="sxs-lookup"><span data-stu-id="be5ce-114">This property is read/write with a default value of false.</span></span>

 

 



