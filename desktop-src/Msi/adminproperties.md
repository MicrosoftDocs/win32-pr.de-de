---
description: Die adminproperties-Eigenschaft sollte in der Eigenschaften Tabelle erstellt werden.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Adminproperties (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372760"
---
# <a name="adminproperties-property"></a><span data-ttu-id="54299-103">Adminproperties (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="54299-103">AdminProperties property</span></span>

<span data-ttu-id="54299-104">Die **adminproperties** -Eigenschaft sollte in der Eigenschaften [Tabelle](property-table.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="54299-104">The **AdminProperties** should be authored into the [Property Table](property-table.md).</span></span> <span data-ttu-id="54299-105">Der Wert von " **adminproperties** " ist eine Liste von Eigenschaftsnamen, die durch Semikolons getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="54299-105">The value of **AdminProperties** is a list of property names separated by semicolons.</span></span> <span data-ttu-id="54299-106">Der Installer speichert die Werte dieser aufgelisteten Eigenschaften zum Zeitpunkt einer [administrativen Installation](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="54299-106">The installer saves the values of these listed properties at the time of an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="54299-107">Wenn Benutzer über das administrative Image installieren, werden bei der Installation die gespeicherten Werte der Eigenschaften anstelle der Werte in der MSI-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="54299-107">When users install from the administrative image, the installation uses the saved values of the properties, rather than the values in the .msi file.</span></span>

## <a name="remarks"></a><span data-ttu-id="54299-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54299-108">Remarks</span></span>

<span data-ttu-id="54299-109">Bei den Eigenschaften Namen in der Liste kann es sich um groß-und Kleinbuchstaben (private Eigenschaften) oder alle Großbuchstaben (öffentliche Eigenschaften) handeln.</span><span class="sxs-lookup"><span data-stu-id="54299-109">The property names in the list can be uppercase and lowercase letters (private properties), or all uppercase (public properties).</span></span>

<span data-ttu-id="54299-110">Diese Eigenschaft darf niemals mit einem Semikolon enden.</span><span class="sxs-lookup"><span data-stu-id="54299-110">This property must never end with a semicolon.</span></span>

## <a name="requirements"></a><span data-ttu-id="54299-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54299-111">Requirements</span></span>



| <span data-ttu-id="54299-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54299-112">Requirement</span></span> | <span data-ttu-id="54299-113">Wert</span><span class="sxs-lookup"><span data-stu-id="54299-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54299-114">Version</span><span class="sxs-lookup"><span data-stu-id="54299-114">Version</span></span><br/> | <span data-ttu-id="54299-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="54299-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="54299-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="54299-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="54299-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="54299-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="54299-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="54299-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54299-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54299-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54299-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54299-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




