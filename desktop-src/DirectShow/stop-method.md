---
description: Die Stopp Methode beendet die Wiedergabe.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Stoppmethode (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960396"
---
# <a name="stop-method-directshow"></a><span data-ttu-id="e486d-103">Stoppmethode (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e486d-103">Stop Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="e486d-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e486d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e486d-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e486d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e486d-106">Die- `Stop` Methode beendet die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="e486d-106">The `Stop` method stops playback.</span></span>

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a><span data-ttu-id="e486d-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e486d-107">Return Value</span></span>

<span data-ttu-id="e486d-108">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e486d-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e486d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e486d-109">Remarks</span></span>

<span data-ttu-id="e486d-110">Wenn [**enableresetonstopp**](enableresetonstop-property.md) auf true festgelegt ist, wird `Stop` beim Aufrufen der DVD-Navigator zusammen mit dem restlichen Filter Diagramm in einen beendeten Zustand versetzt. das bedeutet, dass die Wiedergabe beim nächsten Drücken **der** Wiedergabe Schaltfläche am Anfang der CD beginnt. Wenn **enableresetonstopps** auf true festgelegt ist, wird die Wiedergabe an der Stelle fortgesetzt, an der der Benutzer den nächsten Befehl zum **abspielen** ausgibt</span><span class="sxs-lookup"><span data-stu-id="e486d-110">If [**EnableResetOnStop**](enableresetonstop-property.md) is set to true, calling `Stop` puts the DVD Navigator, along with the rest of the filter graph, into a stopped state, which means that the next time the user presses the **Play** button, playback starts at the beginning of the disc. If **EnableResetOnStop** is set to true, playback resumes where it left off when the user issues the next **Play** command.</span></span>

 

 



