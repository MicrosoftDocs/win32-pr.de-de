---
description: Die Fullscreenmode-Eigenschaft legt einen Wert fest, der angibt, ob die Anzeige im Vollbildmodus ist, oder ruft diesen ab.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Fullscreenmode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123554"
---
# <a name="fullscreenmode-property"></a><span data-ttu-id="7e569-103">Fullscreenmode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7e569-103">FullScreenMode Property</span></span>

> [!Note]  
> <span data-ttu-id="7e569-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7e569-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7e569-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7e569-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7e569-106">Die- `FullScreenMode` Eigenschaft legt einen Wert fest, der angibt, ob die Anzeige im Vollbildmodus ist, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="7e569-106">The `FullScreenMode` property sets or retrieves a value indicating whether the display is in full-screen mode.</span></span>

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a><span data-ttu-id="7e569-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e569-107">Return Value</span></span>

<span data-ttu-id="7e569-108">Gibt einen booleschen Wert zurück, der angibt, ob die Vollbildwiedergabe aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e569-108">Returns a Boolean value indicating whether to enable or disable full-screen playback.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e569-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e569-109">Remarks</span></span>

<span data-ttu-id="7e569-110">Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false.</span><span class="sxs-lookup"><span data-stu-id="7e569-110">This property is read/write with a default value of false.</span></span>



| <span data-ttu-id="7e569-111">Wert</span><span class="sxs-lookup"><span data-stu-id="7e569-111">Value</span></span> | <span data-ttu-id="7e569-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e569-112">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="7e569-113">true</span><span class="sxs-lookup"><span data-stu-id="7e569-113">true</span></span>  | <span data-ttu-id="7e569-114">Aktivieren Sie die Vollbildwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="7e569-114">Enable full-screen playback.</span></span> <span data-ttu-id="7e569-115">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="7e569-115">This is the default value</span></span> |
| <span data-ttu-id="7e569-116">false</span><span class="sxs-lookup"><span data-stu-id="7e569-116">false</span></span> | <span data-ttu-id="7e569-117">Deaktivieren Sie die Vollbildwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="7e569-117">Disable full-screen playback.</span></span>                          |



 

<span data-ttu-id="7e569-118">Der Vollbildmodus ist nur verfügbar, wenn das mswebdvd-Steuerelement im Fenstermodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e569-118">Full screen mode is only available when the MSWebDVD control is running in windowed mode.</span></span>

 

 



