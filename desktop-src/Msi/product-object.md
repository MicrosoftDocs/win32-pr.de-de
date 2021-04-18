---
description: Das Product-Objekt stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist. Das Objekt kann mit der Product-Eigenschaft wie &0034 instanziiert werden \# . WindowsInstaller. Installer. Product (ProductCode, UserSID, context) &\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Product-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357615"
---
# <a name="product-object"></a><span data-ttu-id="6c019-103">Product-Objekt</span><span class="sxs-lookup"><span data-stu-id="6c019-103">Product object</span></span>

<span data-ttu-id="6c019-104">Das **Product** -Objekt stellt eine eindeutige Instanz eines Produkts dar, das entweder angekündigt, installiert oder unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6c019-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="6c019-105">Das Objekt kann mit der **Product** -Eigenschaft als "WindowsInstaller. Installer. Product (*ProductCode*, *UserSID*, *context*)" instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c019-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="6c019-106">*UserSID* muss für computerspezifischen Kontext null sein.</span><span class="sxs-lookup"><span data-stu-id="6c019-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="6c019-107">*UserSID* kann NULL für den angegebenen aktuellen Benutzer sein, wenn der Kontext nicht pro Computer ist.</span><span class="sxs-lookup"><span data-stu-id="6c019-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="6c019-108">*ProductCode* und *Kontext* Parameter sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6c019-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="6c019-109">Member</span><span class="sxs-lookup"><span data-stu-id="6c019-109">Members</span></span>

<span data-ttu-id="6c019-110">Das **Product** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c019-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="6c019-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c019-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c019-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c019-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c019-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="6c019-113">Methods</span></span>

<span data-ttu-id="6c019-114">Das **Product** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6c019-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="6c019-115">Methode</span><span class="sxs-lookup"><span data-stu-id="6c019-115">Method</span></span>                                                                 | <span data-ttu-id="6c019-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c019-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c019-117">**Sourcelistaddmediadisk**</span><span class="sxs-lookup"><span data-stu-id="6c019-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="6c019-118">Fügen Sie dem Satz registrierter Datenträger einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c019-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="6c019-119">**Sourcelistaddsource**</span><span class="sxs-lookup"><span data-stu-id="6c019-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="6c019-120">Fügen Sie der Quell Liste eine Netzwerk-oder URL-Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="6c019-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="6c019-121">**Sourcelistclearall**</span><span class="sxs-lookup"><span data-stu-id="6c019-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="6c019-122">Löscht die gesamte Quell Liste des angegebenen Quellen Typs.</span><span class="sxs-lookup"><span data-stu-id="6c019-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="6c019-123">**Sourcelistclearmediadisk**</span><span class="sxs-lookup"><span data-stu-id="6c019-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="6c019-124">Entfernen Sie einen Datenträger aus der Gruppe der registrierten Datenträger aus der Quell Liste.</span><span class="sxs-lookup"><span data-stu-id="6c019-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="6c019-125">**Sourcelistclearsource**</span><span class="sxs-lookup"><span data-stu-id="6c019-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="6c019-126">Entfernen Sie eine Netzwerk-oder URL-Quelle aus der Quell Liste.</span><span class="sxs-lookup"><span data-stu-id="6c019-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="6c019-127">**Sourcelistforceresolution**</span><span class="sxs-lookup"><span data-stu-id="6c019-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="6c019-128">Löscht die zuletzt verwendete Quelle.</span><span class="sxs-lookup"><span data-stu-id="6c019-128">Clears the last used source.</span></span> <span data-ttu-id="6c019-129">Dadurch wird eine Quell Listen Auflösung erzwungen, wenn die Quelle das nächste Mal benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c019-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6c019-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c019-130">Properties</span></span>

<span data-ttu-id="6c019-131">Das **Product** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c019-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="6c019-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6c019-132">Property</span></span>                                                      | <span data-ttu-id="6c019-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c019-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c019-134">**Componentstate**</span><span class="sxs-lookup"><span data-stu-id="6c019-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="6c019-135">Der Status einer angegebenen Komponente für diese Produkt Instanz.</span><span class="sxs-lookup"><span data-stu-id="6c019-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="6c019-136">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="6c019-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="6c019-137">Der Kontext dieser Produkt Instanz als msiinstallcontext-Wert.</span><span class="sxs-lookup"><span data-stu-id="6c019-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="6c019-138">**Featurestate**</span><span class="sxs-lookup"><span data-stu-id="6c019-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="6c019-139">Der Status eines angegebenen Features für diese Produkt Instanz.</span><span class="sxs-lookup"><span data-stu-id="6c019-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="6c019-140">**InstallProperty**</span><span class="sxs-lookup"><span data-stu-id="6c019-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="6c019-141">Der Wert einer angegebenen Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6c019-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="6c019-142">**Mediadisks**</span><span class="sxs-lookup"><span data-stu-id="6c019-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="6c019-143">Listet alle Medien Datenträger für diese Produkt Instanz auf.</span><span class="sxs-lookup"><span data-stu-id="6c019-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="6c019-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="6c019-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="6c019-145">Gibt den Produktcode zurück.</span><span class="sxs-lookup"><span data-stu-id="6c019-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="6c019-146">**Sourcelistinfo**</span><span class="sxs-lookup"><span data-stu-id="6c019-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="6c019-147">Informationen zu den Quell Informationen erhalten und festlegen</span><span class="sxs-lookup"><span data-stu-id="6c019-147">Get and set the source information properties.</span></span> <span data-ttu-id="6c019-148">Dies ist eine Lese-oder Schreib Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6c019-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="6c019-149">**Sources**</span><span class="sxs-lookup"><span data-stu-id="6c019-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="6c019-150">Listet alle Quellen für diese Produkt Instanz auf.</span><span class="sxs-lookup"><span data-stu-id="6c019-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="6c019-151">**State**</span><span class="sxs-lookup"><span data-stu-id="6c019-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="6c019-152">Der Installationsstatus des Produkts.</span><span class="sxs-lookup"><span data-stu-id="6c019-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="6c019-153">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="6c019-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="6c019-154">Gibt die Benutzer-SID zurück, unter der dieses Konto verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6c019-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="6c019-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c019-155">Requirements</span></span>



| <span data-ttu-id="6c019-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c019-156">Requirement</span></span> | <span data-ttu-id="6c019-157">Wert</span><span class="sxs-lookup"><span data-stu-id="6c019-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c019-158">Version</span><span class="sxs-lookup"><span data-stu-id="6c019-158">Version</span></span><br/> | <span data-ttu-id="6c019-159">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6c019-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6c019-160">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6c019-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6c019-161">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6c019-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="6c019-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6c019-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c019-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c019-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="6c019-164">IID</span><span class="sxs-lookup"><span data-stu-id="6c019-164">IID</span></span><br/>     | <span data-ttu-id="6c019-165">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6c019-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="6c019-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c019-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c019-167">Skript Beispiele für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6c019-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




