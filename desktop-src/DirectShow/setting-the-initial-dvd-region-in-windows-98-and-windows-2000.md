---
description: Festlegen des ersten DVD-Bereichs
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Festlegen des ersten DVD-Bereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520387"
---
# <a name="setting-the-initial-dvd-region"></a><span data-ttu-id="12ac7-103">Festlegen des ersten DVD-Bereichs</span><span class="sxs-lookup"><span data-stu-id="12ac7-103">Setting the Initial DVD Region</span></span>

<span data-ttu-id="12ac7-104">Es liegt in der Verantwortung des Systemherstellers, einen ersten DVD-Bereich für das DVD-Laufwerk auf ihren PCs auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="12ac7-104">It is the responsibility of the system manufacturer to select an initial DVD region for the DVD drive in their PCs.</span></span>

> [!Note]  
> <span data-ttu-id="12ac7-105">Zum Festlegen der Region können nur verschlüsselte Festplatten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12ac7-105">Only encrypted discs can be used to set the region.</span></span>

 

### <a name="windows-2000-and-later"></a><span data-ttu-id="12ac7-106">Windows 2000 und höher</span><span class="sxs-lookup"><span data-stu-id="12ac7-106">Windows 2000 and Later</span></span>

<span data-ttu-id="12ac7-107">Ab Windows 2000 wird der Standard-DVD-Bereich basierend auf dem Gebiets Schema ausgewählt, für das der Computer eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="12ac7-107">Starting in Windows 2000, the default DVD region is selected based upon the locale that the machine is set up for.</span></span> <span data-ttu-id="12ac7-108">Windows 2000 legt die Anfangs Region für ein DVD-Laufwerk immer mit dieser Standard Region und der Region des Datenträgers fest, wenn sich ein Festplattenlaufwerk auf dem Laufwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="12ac7-108">Windows 2000 will always set the initial region for a DVD drive using this default region as well as the disc's region, if there is a disc is in the drive.</span></span> <span data-ttu-id="12ac7-109">Der Systemhersteller muss nichts tun, um die Anfangs Region für DVD-Laufwerke mit Windows 2000 oder höher festzulegen.</span><span class="sxs-lookup"><span data-stu-id="12ac7-109">The system manufacturer does not have to do anything to set the initial region for Windows 2000 or later DVD drives.</span></span>

<span data-ttu-id="12ac7-110">Wenn während des Starts keine Festplatte im Laufwerk vorhanden ist, wird die Standard Region für RPC1-Laufwerke nur basierend auf dem Gebiets Schema des Computers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12ac7-110">For RPC1 drives, if there is no disc in the drive during boot up then the default region is set based only on the locale of the machine.</span></span> <span data-ttu-id="12ac7-111">Wenn beim Start des Laufwerks eine DVD-CD vorhanden ist, wird die Standard Region als die Region des Laufwerks ausgewählt, sofern Sie mit einem Bereich der Festplatte übereinstimmt. Andernfalls wird die niedrigste Region auf der Festplatte als Ausgangsbereich des Laufwerks ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="12ac7-111">If there is a DVD disc in the drive during boot up, the default region is selected to be the drive's region, provided it matches a region of the disc; otherwise the lowest region on the disc is picked as the initial region of the drive.</span></span> <span data-ttu-id="12ac7-112">Für den Benutzer (oder den Systemhersteller) ist eine verbleibende Änderung zulässig, falls die Standardeinstellung nicht korrekt war.</span><span class="sxs-lookup"><span data-stu-id="12ac7-112">The user (or system manufacturer) has one remaining change allowed, in case the default was not correct.</span></span>

<span data-ttu-id="12ac7-113">Wenn bei der Installation von rpc2-Laufwerken während des Setup Vorgangs Windows 2000 feststellt, dass für das Laufwerk keine Region festgelegt ist, wird versucht, eine Region wie oben auszuwählen. Dies gilt jedoch nur, wenn auf dem Laufwerk eine Platte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="12ac7-113">For RPC2 drives, if during the setup process Windows 2000 finds that the drive does not have any region set, it will try to pick a region as above, but only if there is a disc in the drive.</span></span> <span data-ttu-id="12ac7-114">(Bei RPC1-Laufwerken wird die Region ohne Laufwerk im Laufwerk ausgewählt.)</span><span class="sxs-lookup"><span data-stu-id="12ac7-114">(RPC1 drives will choose the region without any disc in drive).</span></span> <span data-ttu-id="12ac7-115">Nachdem eine Region für rpc2-Laufwerke festgelegt wurde, wird Sie nicht automatisch durch eine Neuinstallation oder eine Neuinstallation des Betriebssystems geändert.</span><span class="sxs-lookup"><span data-stu-id="12ac7-115">Once a region is set for RPC2 drives, it is not auto-changed by either a re-installation or a clean installation of the Operating System.</span></span>

<span data-ttu-id="12ac7-116">Der OEM kann einen Registrierungsschlüssel mit dem Standard-DVD-Bereich für das System festlegen.</span><span class="sxs-lookup"><span data-stu-id="12ac7-116">The OEM can set a registry key containing the default DVD region for the system.</span></span> <span data-ttu-id="12ac7-117">Beim ersten Start wird der Laufwerks Bereich auf diesen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="12ac7-117">On first boot, the drive region will be set to this value.</span></span> <span data-ttu-id="12ac7-118">Der Registrierungsschlüssel unter Windows 2000 und höher ist die HKLM \\ System \\ CurrentControlSet- \\ Steuerelement \\ Klasse \\ <CDROM GUID> \\ <instance number> \\ defaultdvdregion (Binary).</span><span class="sxs-lookup"><span data-stu-id="12ac7-118">The registry key on Windows 2000 and later is HKLM\\System\\CurrentControlSet\\Control\\Class\\<CDROM GUID>\\ <instance number>\\DefaultDVDRegion(binary) .</span></span>

## <a name="related-topics"></a><span data-ttu-id="12ac7-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12ac7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12ac7-120">Unterstützung der Änderung von DVD-Regionen in Windows</span><span class="sxs-lookup"><span data-stu-id="12ac7-120">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



