---
description: Das Patch-Objekt stellt eine eindeutige Instanz eines Patches dar, die registriert oder angewendet wurde. Das Objekt kann mit der Patch-Eigenschaft wie &0034 instanziiert werden \# . WindowsInstaller. Installer. Patch (Patchcode, ProductCode, UserSID, context) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367561"
---
# <a name="patch-object"></a><span data-ttu-id="be729-103">Patch-Objekt</span><span class="sxs-lookup"><span data-stu-id="be729-103">Patch object</span></span>

<span data-ttu-id="be729-104">Das **Patch** -Objekt stellt eine eindeutige Instanz eines Patches dar, die registriert oder angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="be729-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="be729-105">Das Objekt kann mit der **Patch** -Eigenschaft als "WindowsInstaller. Installer. Patch (*Patchcode*, *ProductCode*, *UserSID*, *context*)" instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="be729-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="be729-106">Bei einem Computer Kontext muss der *UserSID* -Parameter eine leere Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="be729-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="be729-107">*ProductCode* kann auf eine leere Zeichenfolge für Patches festgelegt werden, die nur registriert sind und noch nicht auf ein Produkt angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="be729-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="be729-108">*ProductCode* kann auf eine leere Zeichenfolge festgelegt werden, wenn nur die Quell Listen Informationen eines Patches gelesen oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="be729-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="be729-109">Member</span><span class="sxs-lookup"><span data-stu-id="be729-109">Members</span></span>

<span data-ttu-id="be729-110">Das **Patch** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="be729-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="be729-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="be729-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="be729-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be729-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="be729-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="be729-113">Methods</span></span>

<span data-ttu-id="be729-114">Das **Patch** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="be729-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="be729-115">Methode</span><span class="sxs-lookup"><span data-stu-id="be729-115">Method</span></span>                                                               | <span data-ttu-id="be729-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be729-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be729-117">**Sourcelistaddmediadisk**</span><span class="sxs-lookup"><span data-stu-id="be729-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="be729-118">Fügen Sie dem Satz registrierter Datenträger einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="be729-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="be729-119">**Sourcelistaddsource**</span><span class="sxs-lookup"><span data-stu-id="be729-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="be729-120">Fügen Sie der Quell Liste eine Netzwerk-oder URL-Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="be729-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="be729-121">**Sourcelistclearall**</span><span class="sxs-lookup"><span data-stu-id="be729-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="be729-122">Löscht die gesamte Quell Liste des angegebenen Quellen Typs.</span><span class="sxs-lookup"><span data-stu-id="be729-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="be729-123">**Sourcelistclearmediadisk**</span><span class="sxs-lookup"><span data-stu-id="be729-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="be729-124">Entfernen Sie einen Datenträger aus der Gruppe der registrierten Datenträger aus der Quell Liste.</span><span class="sxs-lookup"><span data-stu-id="be729-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="be729-125">**Sourcelistclearsource**</span><span class="sxs-lookup"><span data-stu-id="be729-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="be729-126">Entfernen Sie eine Netzwerk-oder URL-Quelle aus der Quell Liste.</span><span class="sxs-lookup"><span data-stu-id="be729-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="be729-127">**Sourcelistforceresolution**</span><span class="sxs-lookup"><span data-stu-id="be729-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="be729-128">Löscht die zuletzt verwendete Quelle aus der Quell Liste.</span><span class="sxs-lookup"><span data-stu-id="be729-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="be729-129">Dadurch wird eine Quell Listen Auflösung erzwungen, wenn die Quelle das nächste Mal benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="be729-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="be729-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="be729-130">Properties</span></span>

<span data-ttu-id="be729-131">Das **patchobjekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="be729-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="be729-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be729-132">Property</span></span>                                                  | <span data-ttu-id="be729-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be729-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be729-134">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="be729-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="be729-135">Der Kontext dieser patchinstanz ist ein msiinstallcontext-Wert.</span><span class="sxs-lookup"><span data-stu-id="be729-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="be729-136">**Mediadisks**</span><span class="sxs-lookup"><span data-stu-id="be729-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="be729-137">Listet alle Medien Datenträger für diese patchinstanz auf.</span><span class="sxs-lookup"><span data-stu-id="be729-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="be729-138">**Patchcode**</span><span class="sxs-lookup"><span data-stu-id="be729-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="be729-139">Gibt den Patchcode zurück.</span><span class="sxs-lookup"><span data-stu-id="be729-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="be729-140">**Patcheigenschaft**</span><span class="sxs-lookup"><span data-stu-id="be729-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="be729-141">Ruft Eigenschaften Informationen zu einem bestimmten Patch ab, der auf eine bestimmte Instanz des Produkts angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="be729-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="be729-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="be729-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="be729-143">Gibt den Produktcode zurück.</span><span class="sxs-lookup"><span data-stu-id="be729-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="be729-144">**Sourcelistinfo**</span><span class="sxs-lookup"><span data-stu-id="be729-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="be729-145">Ruft die Quell Informations Eigenschaften ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="be729-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="be729-146">Dies ist eine Lese-oder Schreib Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="be729-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="be729-147">**Sources**</span><span class="sxs-lookup"><span data-stu-id="be729-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="be729-148">Listet alle Quellen für diese patchinstanz auf.</span><span class="sxs-lookup"><span data-stu-id="be729-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="be729-149">**State**</span><span class="sxs-lookup"><span data-stu-id="be729-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="be729-150">Der Installationsstatus des Patches.</span><span class="sxs-lookup"><span data-stu-id="be729-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="be729-151">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="be729-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="be729-152">Gibt die Benutzer-SID unter dem Konto zurück, auf dem diese patchinstanz verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="be729-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="be729-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be729-153">Requirements</span></span>



| <span data-ttu-id="be729-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be729-154">Requirement</span></span> | <span data-ttu-id="be729-155">Wert</span><span class="sxs-lookup"><span data-stu-id="be729-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be729-156">Version</span><span class="sxs-lookup"><span data-stu-id="be729-156">Version</span></span><br/> | <span data-ttu-id="be729-157">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be729-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be729-158">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be729-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be729-159">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="be729-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="be729-160">DLL</span><span class="sxs-lookup"><span data-stu-id="be729-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="be729-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be729-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="be729-162">IID</span><span class="sxs-lookup"><span data-stu-id="be729-162">IID</span></span><br/>     | <span data-ttu-id="be729-163">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="be729-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="be729-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be729-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be729-165">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="be729-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




