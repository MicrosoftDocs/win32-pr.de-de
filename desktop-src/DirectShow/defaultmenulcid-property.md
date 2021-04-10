---
description: Die dvdadm. defaultmenulcid-Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für Menüs fest oder ruft Sie ab.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Defaultmenulcid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125174"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="66110-103">Defaultmenulcid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="66110-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="66110-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66110-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="66110-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="66110-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="66110-106">Die `DVDAdm.DefaultMenuLCID` -Eigenschaft legt die Registrierungs Einstellung für die benutzerdefinierte Standard-LCID für Menüs fest oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="66110-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="66110-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66110-107">Return Value</span></span>

<span data-ttu-id="66110-108">Gibt einen ganzzahligen Wert zurück, der die LCID darstellt, die in den Registrierungs Einstellungen für die DVD-Anwendung gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="66110-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="66110-109">Dieser Wert ist nicht notwendigerweise identisch mit der Standardmenü Sprache, die auf der DVD erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="66110-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="66110-110">Informationen zum Bereich gültiger LCIDs finden Sie in der Win32-Dokumentation im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="66110-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="66110-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66110-111">Remarks</span></span>

<span data-ttu-id="66110-112">Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="66110-112">This property is read/write with no default value.</span></span> <span data-ttu-id="66110-113">Wenn keine Standardmenü-LCID angegeben wird, verwendet das msdvdadm-Objekt die Sprache, die als Standardmenü Sprache auf der Festplatte gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="66110-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="66110-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66110-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66110-115">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="66110-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



