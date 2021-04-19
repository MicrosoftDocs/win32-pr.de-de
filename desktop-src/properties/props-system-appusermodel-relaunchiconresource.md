---
description: Gibt das Symbol an, das für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. appusermodel. relaunchienresource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355622"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="f210b-103">System. appusermodel. relaunchienresource</span><span class="sxs-lookup"><span data-stu-id="f210b-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="f210b-104">Gibt das Symbol an, das für die Verknüpfung verwendet wird, die auf der Taskleiste erstellt wird, wenn der Benutzer eine Anwendung an die Taskleiste anheften oder über die Sprung Liste der Schaltfläche eine neue Instanz starten soll.</span><span class="sxs-lookup"><span data-stu-id="f210b-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="f210b-105">Dies ist das Symbol, das für die Task leisten Gruppe verwendet wird, und wird für eine fixierte Anwendung angezeigt, unabhängig davon, ob die Anwendung ausgeführt wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f210b-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="f210b-106">Dies sollte in einem der folgenden Formate angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="f210b-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="f210b-107">Standard Ressourcen Format, z. b. "% systemdir% \\ system32 \\shell32.dll,-128".</span><span class="sxs-lookup"><span data-stu-id="f210b-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="f210b-108">Das Zeichen "-" vor der Ressourcen-ID ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f210b-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="f210b-109">Verwenden Sie das Zeichen ' @ ' nicht an der Vorderseite der Pfad Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f210b-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="f210b-110">Direkter Pfad zu einer Symbol Datei, z. b. "% Program Files% \\ Microsoft \\ Notepad \\ . ico, 0".</span><span class="sxs-lookup"><span data-stu-id="f210b-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="f210b-111">Beachten Sie, dass in der Zeichenfolge eine Ressourcen-ID erforderlich ist, da ICO-Dateien mehrere Symbol Ressourcen enthalten können.</span><span class="sxs-lookup"><span data-stu-id="f210b-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="f210b-112">Wenn es sich bei der ICO-Datei um ein einzelnes Bild handelt, verwenden Sie "0" (ohne das Zeichen "-") als Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f210b-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="f210b-113">[System. appusermodel. relaunchiesresource]() ist eine optionale Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f210b-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="f210b-114">Wenn Sie nicht festgelegt ist, wird das Symbol für das Ziel des Befehls "Relaunch" ([System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f210b-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="f210b-115">Da dies jedoch zu unerwünschten Ergebnissen führen kann, empfehlen wir dringend, dass Sie ein Symbol explizit über diese Eigenschaft bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f210b-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="f210b-116">Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungs Benutzer Modell-ID (appusermodelid) verfügt ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="f210b-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="f210b-117">Wenn das Fenster nicht über eine explizite appusermodelid (System.AppUserModel.ID) verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird so gruppiert und fixiert, als wäre es Teil des besitzenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="f210b-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="f210b-118">Weitere Informationen zur Anwendung von expliziten appusermudelids und deren Auswirkungen auf das Anheften der Taskleiste finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="f210b-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="f210b-119">Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustarts-Informationen bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="f210b-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="f210b-120">Weitere Informationen finden Sie unter [System. appusermodel. relaunchcommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="f210b-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="f210b-121">Wenn für das Fenster eine explizite appusermodelid festgelegt wird, diese Eigenschaft jedoch nicht festgelegt ist, versucht das System, eine Verknüpfung mit der gleichen appusermodelid zu finden, und heftet diese Verknüpfung mit der Taskleiste, um das Fenster darzustellen.</span><span class="sxs-lookup"><span data-stu-id="f210b-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="f210b-122">Wenn keine solche Verknüpfung gefunden werden kann, wird die unterstützende ausführbare Datei des Prozesses verwendet, der Sie besitzt.</span><span class="sxs-lookup"><span data-stu-id="f210b-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="f210b-123">Diese Eigenschaft wird ignoriert, wenn [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f210b-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="f210b-124">Dies ermöglicht es einer Anwendung, die Gruppierung ihrer Fenster zu steuern, indem Ihnen explizit appusermudelids zugewiesen wird, aber verhindert wird, dass diese Fenster fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="f210b-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="f210b-125">Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mithilfe von [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. relaunchienresource]() -Eigenschaft dieses Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f210b-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="f210b-126">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f210b-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="f210b-127">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f210b-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="f210b-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f210b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f210b-129">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="f210b-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="f210b-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="f210b-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="f210b-131">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="f210b-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="f210b-132">propertydescription</span><span class="sxs-lookup"><span data-stu-id="f210b-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f210b-133">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="f210b-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f210b-134">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="f210b-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f210b-135">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="f210b-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f210b-136">Display Info</span><span class="sxs-lookup"><span data-stu-id="f210b-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f210b-137">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="f210b-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="f210b-138">StringFormat</span><span class="sxs-lookup"><span data-stu-id="f210b-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f210b-139">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="f210b-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f210b-140">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="f210b-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f210b-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f210b-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f210b-142">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="f210b-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f210b-143">enum</span><span class="sxs-lookup"><span data-stu-id="f210b-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="f210b-144">enumbereich</span><span class="sxs-lookup"><span data-stu-id="f210b-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="f210b-145">image</span><span class="sxs-lookup"><span data-stu-id="f210b-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="f210b-146">DrawControl</span><span class="sxs-lookup"><span data-stu-id="f210b-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f210b-147">editcontrol</span><span class="sxs-lookup"><span data-stu-id="f210b-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f210b-148">FilterControl</span><span class="sxs-lookup"><span data-stu-id="f210b-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f210b-149">querycontrol</span><span class="sxs-lookup"><span data-stu-id="f210b-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="f210b-150">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="f210b-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="f210b-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="f210b-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
