---
description: Gibt einen Befehl an, der durch ShellExecute ausgeführt werden kann, um eine Anwendung zu starten, wenn Sie an die Taskleiste angeheftet ist, oder wenn eine neue Instanz der Anwendung über die Sprung Liste der Anwendung gestartet wird.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. appusermodel. relaunchcommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360176"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="fc381-103">System. appusermodel. relaunchcommand</span><span class="sxs-lookup"><span data-stu-id="fc381-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="fc381-104">Gibt einen Befehl an, der durch [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) ausgeführt werden kann, um eine Anwendung zu starten, wenn Sie an die Taskleiste angeheftet ist, oder wenn eine neue Instanz der Anwendung über die Sprung Liste der Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fc381-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="fc381-105">Einige Beispiele dafür sind:</span><span class="sxs-lookup"><span data-stu-id="fc381-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="fc381-106">Diese Eigenschaft wird nur verwendet, wenn ein Fenster über eine explizite Anwendungs Benutzer Modell-ID (appusermodelid) verfügt ([System.AppUserModel.ID](./props-system-appusermodel-id.md), festgelegt über [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="fc381-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="fc381-107">Wenn das Fenster nicht über eine explizite appusermodelid verfügt, wird diese Eigenschaft ignoriert, und das Fenster wird gruppiert und angeheftet, als wäre es Teil des Prozesses, in dem es enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fc381-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="fc381-108">Weitere Informationen zur Anwendung von expliziten appusermudelids und deren Auswirkungen auf das Anheften der Taskleiste finden Sie unter [Anwendungs Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="fc381-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="fc381-109">Diese Eigenschaft soll von Anwendungen oder Fenstern verwendet werden, die nicht standardmäßige Neustarts-Informationen bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="fc381-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="fc381-110">[System. appusermodel. relaunchcommand]() und [System. appusermodel. relaunchdisplaynameresource](./props-system-appusermodel-relaunchdisplaynameresource.md) müssen immer zusammengesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="fc381-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="fc381-111">Wenn eine dieser Eigenschaften nicht festgelegt ist, wird keines von beiden verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc381-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="fc381-112">Diese Eigenschaft kann zusammen mit " [System. appusermodel. relaunchdisplaynameresource](./props-system-appusermodel-relaunchdisplaynameresource.md) " und " [System. appusermodel. relaunchifiresource](./props-system-appusermodel-relaunchiconresource.md) " verwendet werden, um ein Fenster visuell als Anwendung für den Benutzer zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fc381-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="fc381-113">Dies ist nützlich für Host Anwendungsszenarien, in denen eine einzelne Host Instanz mehrere untergeordnete Anwendungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="fc381-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="fc381-114">Beispielsweise kann es vorkommen, dass ein virtueller Computer, auf dem mehrere virtualisierte Anwendungen gehostet werden, die virtualisierten Anwendungen als individuelle Anwendungen für den Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc381-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="fc381-115">Die virtuelle Maschine kann jedes Fenster mit einer expliziten appusermodelid und den entsprechenden Neustart Eigenschaften bezeichnen, damit Sie als Anwendungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc381-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="fc381-116">Der Benutzer kann Sie dann an die Taskleiste anheften und die angeheftete Instanz "neu starten".</span><span class="sxs-lookup"><span data-stu-id="fc381-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="fc381-117">Diese Eigenschaft wird ignoriert, wenn [System. appusermodel. preventpinning](./props-system-appusermodel-preventpinning.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fc381-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="fc381-118">Dies ermöglicht es einer Anwendung, die Gruppierung ihrer Fenster zu steuern, indem Ihnen explizit appusermudelids zugewiesen wird, aber verhindert wird, dass diese Fenster fixiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc381-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="fc381-119">Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mithilfe von [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System. appusermodel. relaunchcommand]() -Eigenschaft dieses Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fc381-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="fc381-120">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc381-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="fc381-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc381-121">Remarks</span></span>

<span data-ttu-id="fc381-122">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="fc381-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc381-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc381-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc381-124">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="fc381-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="fc381-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="fc381-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="fc381-126">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="fc381-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="fc381-127">propertydescription</span><span class="sxs-lookup"><span data-stu-id="fc381-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fc381-128">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="fc381-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fc381-129">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="fc381-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fc381-130">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="fc381-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fc381-131">Display Info</span><span class="sxs-lookup"><span data-stu-id="fc381-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fc381-132">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="fc381-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="fc381-133">StringFormat</span><span class="sxs-lookup"><span data-stu-id="fc381-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fc381-134">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="fc381-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fc381-135">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="fc381-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fc381-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fc381-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fc381-137">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="fc381-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fc381-138">enum</span><span class="sxs-lookup"><span data-stu-id="fc381-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="fc381-139">enumbereich</span><span class="sxs-lookup"><span data-stu-id="fc381-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="fc381-140">image</span><span class="sxs-lookup"><span data-stu-id="fc381-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="fc381-141">DrawControl</span><span class="sxs-lookup"><span data-stu-id="fc381-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fc381-142">editcontrol</span><span class="sxs-lookup"><span data-stu-id="fc381-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fc381-143">FilterControl</span><span class="sxs-lookup"><span data-stu-id="fc381-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fc381-144">querycontrol</span><span class="sxs-lookup"><span data-stu-id="fc381-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="fc381-145">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="fc381-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="fc381-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="fc381-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
