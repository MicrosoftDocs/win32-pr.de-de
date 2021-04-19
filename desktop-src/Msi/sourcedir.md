---
description: Die SourceDir-Eigenschaft ist das Stammverzeichnis, das die CAB-Quelldatei oder die Quelldatei Struktur des Installationspakets enthält. Dieser Wert wird für die Verzeichnis Auflösung verwendet.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: SourceDir-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372720"
---
# <a name="sourcedir-property"></a><span data-ttu-id="fe620-104">SourceDir-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fe620-104">SourceDir property</span></span>

<span data-ttu-id="fe620-105">Die **SourceDir** -Eigenschaft ist das Stammverzeichnis, das die CAB-Quelldatei oder die Quelldatei Struktur des Installationspakets enthält.</span><span class="sxs-lookup"><span data-stu-id="fe620-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="fe620-106">Dieser Wert wird für die Verzeichnis Auflösung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fe620-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="fe620-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="fe620-107">Default Value</span></span>

<span data-ttu-id="fe620-108">Das Verzeichnis, in dem das Installationspaket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fe620-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe620-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe620-109">Remarks</span></span>

<span data-ttu-id="fe620-110">Die [ResolveSource-Aktion](resolvesource-action.md) muss aufgerufen werden, bevor **die SourceDir** -Eigenschaft in einem Ausdruck verwendet wird, oder es wird versucht, den Wert von **SourceDir** mit [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fe620-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="fe620-111">Die Aktion "ResolveSource" sollte nicht ausgeführt werden, während die Quelle nicht verfügbar ist, z. b. beim Deinstallieren einer Anwendung, da dies zu einer unbeabsichtigten Aufforderung für das Quell Medium führen kann.</span><span class="sxs-lookup"><span data-stu-id="fe620-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe620-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe620-112">Requirements</span></span>



| <span data-ttu-id="fe620-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe620-113">Requirement</span></span> | <span data-ttu-id="fe620-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fe620-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe620-115">Version</span><span class="sxs-lookup"><span data-stu-id="fe620-115">Version</span></span><br/> | <span data-ttu-id="fe620-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fe620-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fe620-117">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe620-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fe620-118">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fe620-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fe620-119">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fe620-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe620-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe620-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe620-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fe620-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




