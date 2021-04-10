---
description: Rückruf zum Speichern oder Beenden des Experiments. Gibt an, dass die Dateispeicherung abgeschlossen ist.
MS-HAID: vspixengine.IFileIOCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ifleiocallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F9C5E117-310C-4769-B78D-9A779A52EAE7
api_name:
- IFileIOCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cccb7895a862b91250101fe2dd9e4b4ca43b0650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213921"
---
# <a name="span-idvspixengineifileiocallbackspanifileiocallback-interface"></a><span data-ttu-id="7908a-104"><span id="vspixengine.ifileiocallback"></span>Ifleiocallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7908a-104"><span id="vspixengine.ifileiocallback"></span>IFileIOCallback interface</span></span>

<span data-ttu-id="7908a-105">Rückruf zum Speichern oder Beenden des Experiments.</span><span class="sxs-lookup"><span data-stu-id="7908a-105">Callback to save or end the experiment.</span></span> <span data-ttu-id="7908a-106">Gibt an, dass die Dateispeicherung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7908a-106">Indicates file save is done.</span></span>

## <a name="members"></a><span data-ttu-id="7908a-107">Member</span><span class="sxs-lookup"><span data-stu-id="7908a-107">Members</span></span>

<span data-ttu-id="7908a-108">Die **IFI** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7908a-108">The **IFileIOCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7908a-109">**Ifleiocallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7908a-109">**IFileIOCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="7908a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7908a-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="7908a-111"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="7908a-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="7908a-112">Die **ifleiocallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7908a-112">The **IFileIOCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="7908a-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7908a-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="7908a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7908a-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="7908a-115"><a href="/windows/desktop/direct3dtools/ifileiocallback-resultcallback-dword"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="7908a-115"><a href="/windows/desktop/direct3dtools/ifileiocallback-resultcallback-dword"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="7908a-116">Eine Rückruffunktion, die verwendet wird, um den Host von Fehlern während der Erfassung oder Wiedergabe zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="7908a-116">A callback function used to notify the host of errors while during capture or playback.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="7908a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7908a-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7908a-118">Header</span><span class="sxs-lookup"><span data-stu-id="7908a-118">Header</span></span></p></td><td><span data-ttu-id="7908a-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7908a-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
