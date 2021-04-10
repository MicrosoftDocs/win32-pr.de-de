---
description: Deaktiviert die Möglichkeit, eine Verknüpfung oder ein Fenster an die Taskleiste oder das Startmenü anzuheften. Diese Eigenschaft bewirkt außerdem, dass das Element in die Liste der am häufigsten verwendeten (MFU) Startmenüs aufgenommen wird.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. appusermodel. preventpinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865564"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="4dc20-104">System. appusermodel. preventpinning</span><span class="sxs-lookup"><span data-stu-id="4dc20-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="4dc20-105">Deaktiviert die Möglichkeit, eine Verknüpfung oder ein Fenster an die Taskleiste oder das **Startmenü** anzuheften.</span><span class="sxs-lookup"><span data-stu-id="4dc20-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="4dc20-106">Diese Eigenschaft bewirkt außerdem, dass das Element in die Liste der am häufigsten verwendeten (MFU) **Startmenüs** aufgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="4dc20-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="4dc20-107">Diese Eigenschaft muss in einem Fenster vor der Eigenschaft [pkey \_ appusermodel \_ ID](./props-system-appusermodel-id.md) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4dc20-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="4dc20-108">Nachdem die pkey- \_ appusermodel- \_ ID-Eigenschaft festgelegt wurde, werden Änderungen an der [pkey- \_ appusermodel \_ ]() -Ausführung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4dc20-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="4dc20-109">Weitere Informationen zu App-Benutzer Modell-IDs (appusermudelids) und anderen Methoden zum Ausschließen eines Elements an die Taskleiste und zum Einbinden von MFU finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="4dc20-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="4dc20-110">Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. preventpinning]() -Eigenschaft dieses Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4dc20-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="4dc20-111">Das Festlegen dieser Eigenschaft bewirkt, dass die folgenden Eigenschaften ignoriert werden:</span><span class="sxs-lookup"><span data-stu-id="4dc20-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="4dc20-112">System. appusermodel. relaunchcommand</span><span class="sxs-lookup"><span data-stu-id="4dc20-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="4dc20-113">System. appusermodel. relaunchdisplaynameresource</span><span class="sxs-lookup"><span data-stu-id="4dc20-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="4dc20-114">System. appusermodel. relaunchienresource</span><span class="sxs-lookup"><span data-stu-id="4dc20-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="4dc20-115">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4dc20-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="4dc20-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dc20-116">Remarks</span></span>

<span data-ttu-id="4dc20-117">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="4dc20-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dc20-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4dc20-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dc20-119">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="4dc20-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="4dc20-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="4dc20-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="4dc20-121">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="4dc20-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="4dc20-122">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="4dc20-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="4dc20-123">propertydescription</span><span class="sxs-lookup"><span data-stu-id="4dc20-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="4dc20-124">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="4dc20-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="4dc20-125">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="4dc20-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="4dc20-126">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="4dc20-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="4dc20-127">Display Info</span><span class="sxs-lookup"><span data-stu-id="4dc20-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="4dc20-128">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="4dc20-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="4dc20-129">StringFormat</span><span class="sxs-lookup"><span data-stu-id="4dc20-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="4dc20-130">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="4dc20-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="4dc20-131">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="4dc20-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="4dc20-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4dc20-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="4dc20-133">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="4dc20-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="4dc20-134">enum</span><span class="sxs-lookup"><span data-stu-id="4dc20-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="4dc20-135">enumbereich</span><span class="sxs-lookup"><span data-stu-id="4dc20-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="4dc20-136">image</span><span class="sxs-lookup"><span data-stu-id="4dc20-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="4dc20-137">DrawControl</span><span class="sxs-lookup"><span data-stu-id="4dc20-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="4dc20-138">editcontrol</span><span class="sxs-lookup"><span data-stu-id="4dc20-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="4dc20-139">FilterControl</span><span class="sxs-lookup"><span data-stu-id="4dc20-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="4dc20-140">querycontrol</span><span class="sxs-lookup"><span data-stu-id="4dc20-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="4dc20-141">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="4dc20-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="4dc20-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="4dc20-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
