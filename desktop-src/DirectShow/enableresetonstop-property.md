---
description: Die enableresetonstopp-Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der bestimmt, wie die Wiedergabe fortgesetzt wird, wenn das Filter Diagramm einen Übergang von einem beendeten Zustand bewirkt.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Enableresetonstoppt (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746648"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="df211-103">Enableresetonstoppt (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df211-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="df211-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df211-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="df211-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="df211-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="df211-106">Die- `EnableResetOnStop` Eigenschaft legt einen Wert fest oder Ruft einen Wert ab, der bestimmt, wie die Wiedergabe fortgesetzt wird, wenn das Filter Diagramm einen Übergang vom beendeten Zustand bewirkt.</span><span class="sxs-lookup"><span data-stu-id="df211-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="df211-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df211-107">Return Value</span></span>

<span data-ttu-id="df211-108">Gibt einen booleschen Wert zurück, der angibt, wo das mswebdvd-Objekt wieder abgespielt wird, nachdem das Filter Diagramm angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="df211-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="df211-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df211-109">Remarks</span></span>

<span data-ttu-id="df211-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="df211-110">This property is read/write.</span></span>

<span data-ttu-id="df211-111">Mögliche Werte für diese Eigenschaft sind: mit dem Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="df211-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="df211-112">Wert</span><span class="sxs-lookup"><span data-stu-id="df211-112">Value</span></span> | <span data-ttu-id="df211-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df211-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df211-114">true</span><span class="sxs-lookup"><span data-stu-id="df211-114">true</span></span>  | <span data-ttu-id="df211-115">Der DVD-Navigator wird zurückgesetzt und startet am Anfang der Festplatte. Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="df211-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="df211-116">false</span><span class="sxs-lookup"><span data-stu-id="df211-116">false</span></span> | <span data-ttu-id="df211-117">Der DVD-Navigator wird wiedergegeben, wo er aufgehört hat.</span><span class="sxs-lookup"><span data-stu-id="df211-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



