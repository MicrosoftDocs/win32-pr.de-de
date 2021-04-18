---
description: Bestimmen Sie die Version von Windows Update-Agent (WUA), bevor Sie Sie verwenden.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Ermitteln der aktuellen WUA-Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347307"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="1b260-103">Ermitteln der aktuellen WUA-Version</span><span class="sxs-lookup"><span data-stu-id="1b260-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="1b260-104">Allgemeine Informationen zum Aktualisieren von WUA, einschließlich Schritt-für-Schritt-Anweisungen zur programmgesteuerten Ermittlung von innerhalb Ihrer APP, unabhängig davon, ob die auf dem Computer laufende Version von WUA Ihren Anforderungen entspricht, finden Sie unter [Aktualisieren des Windows Update-Agents](updating-the-windows-update-agent.md).</span><span class="sxs-lookup"><span data-stu-id="1b260-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="1b260-105">Unter Windows-Versionen vor Windows 7 und Windows Server 2008 R2 sollten Sie die installierte Version von Windows Update-Agent (WUA) bestimmen, bevor Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b260-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="1b260-106">Die aktuelle Version von WUA wird durch die Version der Wuaueng.dll bestimmt, die im \\ Unterverzeichnis System32 der aktuellen Windows-Installation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b260-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="1b260-107">Wenn die Version von Wuaueng.dll Version 5.4.3790.1000 oder eine höhere Version ist, wird WUA installiert.</span><span class="sxs-lookup"><span data-stu-id="1b260-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="1b260-108">Eine frühere Version als 5.4.3790.1000 gibt an, dass Software Update Services (SUS) 1,0 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1b260-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="1b260-109">Wenn Sie SUS 1,0 mithilfe der WUA-API aufruft, wird ein **HRESULT** von Wu \_ E \_ au \_ Legacyserver zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b260-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="1b260-110">Sie können auch die [**iwindowsupdateagentinfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) -Methode verwenden, um die aktuelle Dateiversion von Wuapi.dll abzurufen, die auf einem Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b260-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="1b260-111">Die [**iwindowsupdateagentinfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) -Schnittstelle wird in WUA 1,0 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b260-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
