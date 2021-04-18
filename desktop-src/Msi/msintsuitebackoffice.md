---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die msintsuitebackoffice-Eigenschaft auf 1 fest, wenn Microsoft BackOffice-Komponenten installiert sind.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Msintsuitebackoffice (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371526"
---
# <a name="msintsuitebackoffice-property"></a><span data-ttu-id="026aa-103">Msintsuitebackoffice (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="026aa-103">MsiNTSuiteBackOffice property</span></span>

<span data-ttu-id="026aa-104">Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die **msintsuitebackoffice** -Eigenschaft auf 1 fest, wenn Microsoft BackOffice-Komponenten installiert sind.</span><span class="sxs-lookup"><span data-stu-id="026aa-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteBackOffice** property to 1 if Microsoft BackOffice components are installed.</span></span> <span data-ttu-id="026aa-105">Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das "Ver \_ Suite \_ BackOffice"-Flag in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="026aa-105">The installer sets this property to 1 only if the VER\_SUITE\_BACKOFFICE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="026aa-106">Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.</span><span class="sxs-lookup"><span data-stu-id="026aa-106">Otherwise, the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="026aa-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="026aa-107">Requirements</span></span>



| <span data-ttu-id="026aa-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="026aa-108">Requirement</span></span> | <span data-ttu-id="026aa-109">Wert</span><span class="sxs-lookup"><span data-stu-id="026aa-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="026aa-110">Version</span><span class="sxs-lookup"><span data-stu-id="026aa-110">Version</span></span><br/> | <span data-ttu-id="026aa-111">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="026aa-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="026aa-112">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="026aa-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="026aa-113">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="026aa-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="026aa-114">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="026aa-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="026aa-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="026aa-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026aa-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="026aa-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
