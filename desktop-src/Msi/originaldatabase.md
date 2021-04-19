---
description: Der Windows Installer legt die Eigenschaft originaldatabase auf den Pfad der Installations Datenbank fest, mit der die Installation gestartet wird.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Originaldatabase (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367011"
---
# <a name="originaldatabase-property"></a><span data-ttu-id="20838-103">Originaldatabase (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="20838-103">OriginalDatabase property</span></span>

<span data-ttu-id="20838-104">Der Windows Installer legt die Eigenschaft **originaldatabase** auf den Pfad der Installations Datenbank fest, mit der die Installation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="20838-104">The Windows Installer sets the **OriginalDatabase** property to the path of the installation database used to launch the installation.</span></span> <span data-ttu-id="20838-105">Wenn die Installation über eine Befehlszeile gestartet wird, hängt der Wert davon ab, ob die Option "Recache Package" (das-v-Flag) in der Eigenschaft " [**REINSTALLMODE**](reinstallmode.md) " vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="20838-105">If the installation is launched from a command line, the value depends on whether the recache package option (the -v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>



| <span data-ttu-id="20838-106">Installationsmethode</span><span class="sxs-lookup"><span data-stu-id="20838-106">Installation Method</span></span>                                                                                                                                                                                  | <span data-ttu-id="20838-107">Originaldatabase-Wert</span><span class="sxs-lookup"><span data-stu-id="20838-107">OriginalDatabase Value</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="20838-108">Alle Installationen, die durch Aufrufen des Pfads des Installationspakets (MSI-Datei) gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="20838-108">Any installation launched by invoking the path of the installation package (.msi file).</span></span>                                                                                                              | <span data-ttu-id="20838-109">Pfad zum Installationspaket (MSI-Datei).</span><span class="sxs-lookup"><span data-stu-id="20838-109">Path to the installation package (.msi file).</span></span> |
| <span data-ttu-id="20838-110">Die Installation wurde von der Befehlszeile aus gestartet.</span><span class="sxs-lookup"><span data-stu-id="20838-110">Installation launched from a command line.</span></span> <span data-ttu-id="20838-111">Die Installation wird nicht von einem Paketpfad gestartet.</span><span class="sxs-lookup"><span data-stu-id="20838-111">The installation is not launched from a package path.</span></span> <span data-ttu-id="20838-112">Die Recache-Option (-v-Flag) ist in der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20838-112">The recache option (-v flag) is present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>     | <span data-ttu-id="20838-113">Der Pfad zur Datenbank in der Quelle.</span><span class="sxs-lookup"><span data-stu-id="20838-113">Path to the database on the source.</span></span>           |
| <span data-ttu-id="20838-114">Die Installation wurde von der Befehlszeile aus gestartet.</span><span class="sxs-lookup"><span data-stu-id="20838-114">Installation launched from a command line.</span></span> <span data-ttu-id="20838-115">Die Installation wird nicht von einem Paketpfad gestartet.</span><span class="sxs-lookup"><span data-stu-id="20838-115">The installation is not launched from a package path.</span></span> <span data-ttu-id="20838-116">Die Recache-Option (-v-Flag) ist in der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20838-116">The recache option (-v flag) is not present in the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> | <span data-ttu-id="20838-117">Der Pfad zur zwischengespeicherten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="20838-117">Path to the cached database.</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="20838-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20838-118">Remarks</span></span>

<span data-ttu-id="20838-119">Bei der erstmaligen Installation kann eine benutzerdefinierte Aktion, die vor der [ResolveSource-Aktion](resolvesource-action.md) sequenziert wurde, die **originaldatabase** -Eigenschaft verwenden, um den Speicherort der Installationsquelle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="20838-119">During a first time installation, a custom action sequenced before the [ResolveSource action](resolvesource-action.md) can use the **OriginalDatabase** property to determine the location of the installation source.</span></span>

## <a name="requirements"></a><span data-ttu-id="20838-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20838-120">Requirements</span></span>



| <span data-ttu-id="20838-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20838-121">Requirement</span></span> | <span data-ttu-id="20838-122">Wert</span><span class="sxs-lookup"><span data-stu-id="20838-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20838-123">Version</span><span class="sxs-lookup"><span data-stu-id="20838-123">Version</span></span><br/> | <span data-ttu-id="20838-124">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20838-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="20838-125">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20838-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="20838-126">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="20838-126">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="20838-127">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="20838-127">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20838-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20838-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20838-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="20838-129">Properties</span></span>](properties.md)
</dt> </dl>

 

 




