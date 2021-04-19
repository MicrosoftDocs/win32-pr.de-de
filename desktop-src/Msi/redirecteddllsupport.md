---
description: Der Installer legt die Eigenschaft redirecteddllsupport fest, wenn die Systemplattform, die die Installation ausführt, isolierte Komponenten unterstützt.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Redirecteddllsupport (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354204"
---
# <a name="redirecteddllsupport-property"></a><span data-ttu-id="2dfe0-103">Redirecteddllsupport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2dfe0-103">RedirectedDLLSupport property</span></span>

<span data-ttu-id="2dfe0-104">Der Installer legt die Eigenschaft **redirecteddllsupport** fest, wenn die Systemplattform, die die Installation ausführt, [isolierte Komponenten](isolated-components.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-104">The installer sets the **RedirectedDLLSupport** property if the system platform performing the installation supports [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="2dfe0-105">Der Installer legt die Eigenschaft **redirecteddllsupport** auf den Wert 1 fest, wenn das System, das die Installation ausführt, [isolierte Komponenten](isolated-components.md) unterstützt, die auf basieren. Lokale Dateien.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-105">The installer sets the **RedirectedDLLSupport** property to a value of 1 if the system performing the installation supports [Isolated Components](isolated-components.md) based on .LOCAL files.</span></span> <span data-ttu-id="2dfe0-106">Der Installer legt die Eigenschaft **redirecteddllsupport** auf den Wert 2 fest, wenn das System, das die Installation ausführt, die Isolation mithilfe von unterstützt. Lokale Dateien oder Win32-Assemblys nebeneinander.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-106">The installer sets the **RedirectedDLLSupport** property to a value of 2 if the system that performs the installation supports isolation using either .LOCAL files or Win32 side-by-side assemblies.</span></span>

<span data-ttu-id="2dfe0-107">Die Eigenschaft **redirecteddllsupport** kann verwendet werden, um die [isolatecomponents-Aktion](isolatecomponents-action.md) in der Tabelle [InstallUISequence](installuisequence-table.md) oder der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)zu bedinieren.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-107">The **RedirectedDLLSupport** property can be used to condition the [IsolateComponents action](isolatecomponents-action.md) in the [InstallUISequence table](installuisequence-table.md) or [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2dfe0-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dfe0-108">Requirements</span></span>



| <span data-ttu-id="2dfe0-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dfe0-109">Requirement</span></span> | <span data-ttu-id="2dfe0-110">Wert</span><span class="sxs-lookup"><span data-stu-id="2dfe0-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfe0-111">Version</span><span class="sxs-lookup"><span data-stu-id="2dfe0-111">Version</span></span><br/> | <span data-ttu-id="2dfe0-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2dfe0-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2dfe0-114">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2dfe0-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2dfe0-115">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2dfe0-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2dfe0-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dfe0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dfe0-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2dfe0-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




