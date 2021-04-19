---
description: Die executemode-Eigenschaft gibt an, wie das Installationsprogramm Systemupdates ausführt.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Executemode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370861"
---
# <a name="executemode-property"></a><span data-ttu-id="1ed7f-103">Executemode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1ed7f-103">EXECUTEMODE property</span></span>

<span data-ttu-id="1ed7f-104">Die **executemode** -Eigenschaft gibt an, wie das Installationsprogramm Systemupdates ausführt.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="1ed7f-105">Diese Eigenschaft ist möglicherweise nützlich, wenn es erforderlich ist, eine Installation auszuführen, ohne das System tatsächlich zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="1ed7f-106">Die-Eigenschaft kann auf keine festgelegt werden, um Aktualisierungs Vorgänge wie die Installation von Dateien und Registrierungs Werten zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="1ed7f-107">Diese Eigenschaft kann einen der folgenden beiden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-107">This property can have one of the following two values.</span></span> <span data-ttu-id="1ed7f-108">Das Installationsprogramm überprüft nur den ersten Buchstaben des Werts und berücksichtigt die Groß-/Kleinschreibung nicht.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="1ed7f-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>Gar</span><span class="sxs-lookup"><span data-stu-id="1ed7f-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="1ed7f-110">Es werden keine Änderungen am System vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-110">No changes are made to the system.</span></span> <span data-ttu-id="1ed7f-111">Das Installationsprogramm führt die Benutzeroberfläche aus und fragt dann die Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="1ed7f-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Web</span><span class="sxs-lookup"><span data-stu-id="1ed7f-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="1ed7f-113">Alle Änderungen am System werden durch die Skriptausführung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="1ed7f-114">Dies ist der Standardmodus.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="1ed7f-115">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1ed7f-115">Default Value</span></span>

<span data-ttu-id="1ed7f-116">Wenn diese Eigenschaft nicht definiert ist, wird für den Ausführungs Modus standardmäßig Script verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed7f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ed7f-117">Requirements</span></span>



| <span data-ttu-id="1ed7f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ed7f-118">Requirement</span></span> | <span data-ttu-id="1ed7f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1ed7f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed7f-120">Version</span><span class="sxs-lookup"><span data-stu-id="1ed7f-120">Version</span></span><br/> | <span data-ttu-id="1ed7f-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1ed7f-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1ed7f-123">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1ed7f-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="1ed7f-124">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="1ed7f-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ed7f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ed7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed7f-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ed7f-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




