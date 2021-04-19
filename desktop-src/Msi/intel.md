---
description: Die Intel-Eigenschaft wird von der Windows Installer auf die numerische Prozessor Ebene festgelegt, wenn Sie auf einem Intel-Prozessor ausgeführt wird.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361333"
---
# <a name="intel-property"></a><span data-ttu-id="77686-103">Intel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="77686-103">Intel property</span></span>

<span data-ttu-id="77686-104">Die **Intel** -Eigenschaft wird von der Windows Installer auf die numerische Prozessor Ebene festgelegt, wenn Sie auf einem Intel-Prozessor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77686-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="77686-105">Die Werte sind identisch mit dem *wprocessorlevel* -Feld der [**System \_ Info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="77686-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="77686-106">Bei der Ausführung auf einem x64-Prozessor legt der Windows Installer die **Intel** -Eigenschaft so fest, dass der vom x64-Computer durch das Betriebssystem gemeldete x86-Prozessor wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77686-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="77686-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77686-107">Requirements</span></span>



| <span data-ttu-id="77686-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77686-108">Requirement</span></span> | <span data-ttu-id="77686-109">Wert</span><span class="sxs-lookup"><span data-stu-id="77686-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77686-110">Version</span><span class="sxs-lookup"><span data-stu-id="77686-110">Version</span></span><br/> | <span data-ttu-id="77686-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="77686-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="77686-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="77686-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="77686-113">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77686-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="77686-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="77686-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77686-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77686-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77686-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="77686-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
