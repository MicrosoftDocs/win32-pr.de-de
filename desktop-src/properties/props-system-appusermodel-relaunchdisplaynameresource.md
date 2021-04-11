---
description: Gibt den anzeigen Amen an, der für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. appusermodel. relaunchdisplaynameresource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216098"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="e4484-103">System. appusermodel. relaunchdisplaynameresource</span><span class="sxs-lookup"><span data-stu-id="e4484-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="e4484-104">Gibt den anzeigen Amen an, der für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll.</span><span class="sxs-lookup"><span data-stu-id="e4484-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="e4484-105">Der Wert dieser Eigenschaft muss einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="e4484-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="e4484-106">Eine indirekte Ressourcen Zeichenfolge, z. b. "@% systemdir% \\ system32 \\shell32.dll,-19263".</span><span class="sxs-lookup"><span data-stu-id="e4484-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="e4484-107">Beachten Sie, dass das Zeichen "@" erforderlich ist, um eine indirekte Zeichenfolge von einer nur-Text-Zeichenfolge zu unterscheiden (im nächsten aufzurufenen Absatz beschrieben).</span><span class="sxs-lookup"><span data-stu-id="e4484-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="e4484-108">Diese indirekte Zeichenfolge besteht aus einer Binärdatei und einer Ressourcen-ID der Zeichenfolge, die in dieser Binärdatei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e4484-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="e4484-109">Es wird dringend empfohlen, dieses indirekte Zeichen folgen Formular zu verwenden, das sicherstellt, dass sich der Anzeige Name entsprechend ändert, wenn die Systemsprache über die mehrsprachige Benutzeroberfläche (MUI) geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e4484-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="e4484-110">Das Zeichen "-" vor der Ressourcen-ID ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e4484-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="e4484-111">Eine klar Text Zeichenfolge, die nicht auf eine Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="e4484-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="e4484-112">Dies sollte nur verwendet werden, wenn der Anzeige Name dynamisch berechnet oder aus einer Datenquelle abgerufen wird, die MUI nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4484-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="e4484-113">Die Zeichenfolge könnte z. b. der Name eines Geräts sein, z. b. "Microsoft Zune", in Fällen, in denen die Anwendung angezeigt wird, wenn das Gerät mit dem Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e4484-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="e4484-114">[System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md) und [System. appusermodel. relaunchdisplaynameresource]() müssen immer zusammengesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e4484-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="e4484-115">Wenn eine dieser Eigenschaften nicht festgelegt ist, wird keines von beiden verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4484-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="e4484-116">Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungs Benutzer Modell-ID (appusermodelid) verfügt ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="e4484-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="e4484-117">Wenn das Fenster nicht über eine explizite appusermodelid verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des Prozesses, in dem es enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e4484-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="e4484-118">Weitere Informationen zur Anwendung von expliziten appusermudelids und deren Auswirkungen auf das Anheften der Taskleiste finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="e4484-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="e4484-119">Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustarts-Informationen bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e4484-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="e4484-120">Weitere Informationen finden Sie unter [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="e4484-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="e4484-121">Diese Eigenschaft wird ignoriert, wenn [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e4484-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="e4484-122">Dies ermöglicht es einer Anwendung, die Gruppierung ihrer Fenster zu steuern, indem Ihnen explizit appusermudelids zugewiesen wird, aber verhindert wird, dass diese Fenster fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="e4484-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="e4484-123">Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. relaunchdisplaynameresource]() -Eigenschaft dieses Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e4484-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e4484-124">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4484-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="e4484-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4484-125">Remarks</span></span>

<span data-ttu-id="e4484-126">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="e4484-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4484-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4484-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4484-128">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="e4484-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="e4484-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="e4484-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="e4484-130">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="e4484-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="e4484-131">propertydescription</span><span class="sxs-lookup"><span data-stu-id="e4484-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e4484-132">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="e4484-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e4484-133">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="e4484-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e4484-134">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="e4484-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e4484-135">Display Info</span><span class="sxs-lookup"><span data-stu-id="e4484-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e4484-136">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="e4484-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="e4484-137">StringFormat</span><span class="sxs-lookup"><span data-stu-id="e4484-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e4484-138">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="e4484-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e4484-139">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="e4484-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e4484-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e4484-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e4484-141">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="e4484-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e4484-142">enum</span><span class="sxs-lookup"><span data-stu-id="e4484-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="e4484-143">enumbereich</span><span class="sxs-lookup"><span data-stu-id="e4484-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="e4484-144">image</span><span class="sxs-lookup"><span data-stu-id="e4484-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="e4484-145">DrawControl</span><span class="sxs-lookup"><span data-stu-id="e4484-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e4484-146">editcontrol</span><span class="sxs-lookup"><span data-stu-id="e4484-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e4484-147">FilterControl</span><span class="sxs-lookup"><span data-stu-id="e4484-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e4484-148">querycontrol</span><span class="sxs-lookup"><span data-stu-id="e4484-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="e4484-149">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="e4484-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="e4484-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="e4484-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
