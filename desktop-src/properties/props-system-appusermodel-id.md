---
description: Eine explizite App-Benutzer Modell-ID (appusermodelid), die verwendet wird, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344779"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="a1881-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="a1881-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="a1881-104">Eine explizite App-Benutzer Modell-ID (appusermodelid), die verwendet wird, um Prozesse, Dateien und Fenster einer bestimmten Anwendung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a1881-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="a1881-105">In einigen Fällen ist es ausreichend, die interne appusermodelid zu verlassen, die einem Prozess vom System zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a1881-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="a1881-106">Eine Anwendung, die mehrere Prozesse oder eine Anwendung besitzt, die in einem Host Prozess ausgeführt wird, muss sich jedoch möglicherweise explizit durch diese Eigenschaft identifizieren, damit Sie die ansonsten ungleichen Fenster unter einer einzigen Task leisten Schaltfläche gruppieren und den Inhalt der Sprung Liste der Anwendung steuern kann.</span><span class="sxs-lookup"><span data-stu-id="a1881-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="a1881-107">Wenn Sie diese Eigenschaft für ein Fenster festlegen möchten, rufen Sie mit [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) den Eigenschaften Speicher des Fensters ab, und verwenden Sie die Methoden dieses abgerufenen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Objekts, um die [System.AppUserModel.ID]() -Eigenschaft dieses Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a1881-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="a1881-108">Weitere Informationen finden Sie unter [App-Benutzer Modell-IDs (appusermudelids)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="a1881-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="a1881-109">Zu dem Zeitpunkt, an dem die [System.AppUserModel.ID]() -Eigenschaft festgelegt ist, wird die Taskleiste benachrichtigt, um die zugehörigen Informationen im Fenster oder in der Verknüpfung mit der entsprechenden appusermodelid zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a1881-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="a1881-110">Andere Fenster-und Verknüpfungs Eigenschaften können in Verbindung mit einer expliziten appusermodelid verwendet werden, um das Gruppieren und fixieren, das einem Fenster zugeordnet ist, den anzeigen Amen und das Symbol, das in der Taskleiste verwendet wird, und den Befehl zum Starten einer Anwendung, die an die Taskleiste angeheftet ist, bzw</span><span class="sxs-lookup"><span data-stu-id="a1881-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="a1881-111">Diese Eigenschaften sollten vor dem Festlegen der [System.AppUserModel.ID]() -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1881-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="a1881-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a1881-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a1881-113">System. appusermodel. preventpinning</span><span class="sxs-lookup"><span data-stu-id="a1881-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="a1881-114">System. appusermodel. relaunchcommand</span><span class="sxs-lookup"><span data-stu-id="a1881-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="a1881-115">System. appusermodel. relaunchdisplaynameresource</span><span class="sxs-lookup"><span data-stu-id="a1881-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="a1881-116">System. appusermodel. relaunchienresource</span><span class="sxs-lookup"><span data-stu-id="a1881-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a1881-117">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a1881-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="a1881-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1881-118">Remarks</span></span>

<span data-ttu-id="a1881-119">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="a1881-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1881-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1881-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1881-121">Anwendungs Benutzer Modell-IDs (appusermudelids)</span><span class="sxs-lookup"><span data-stu-id="a1881-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="a1881-122">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="a1881-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="a1881-123">propertydescriptionlist</span><span class="sxs-lookup"><span data-stu-id="a1881-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="a1881-124">propertydescription</span><span class="sxs-lookup"><span data-stu-id="a1881-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a1881-125">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="a1881-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a1881-126">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="a1881-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a1881-127">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="a1881-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a1881-128">Display Info</span><span class="sxs-lookup"><span data-stu-id="a1881-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a1881-129">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="a1881-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="a1881-130">StringFormat</span><span class="sxs-lookup"><span data-stu-id="a1881-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a1881-131">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="a1881-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a1881-132">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="a1881-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a1881-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a1881-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a1881-134">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="a1881-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a1881-135">enum</span><span class="sxs-lookup"><span data-stu-id="a1881-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="a1881-136">enumbereich</span><span class="sxs-lookup"><span data-stu-id="a1881-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="a1881-137">image</span><span class="sxs-lookup"><span data-stu-id="a1881-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="a1881-138">DrawControl</span><span class="sxs-lookup"><span data-stu-id="a1881-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a1881-139">editcontrol</span><span class="sxs-lookup"><span data-stu-id="a1881-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a1881-140">FilterControl</span><span class="sxs-lookup"><span data-stu-id="a1881-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a1881-141">querycontrol</span><span class="sxs-lookup"><span data-stu-id="a1881-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="a1881-142">relatedpropertyinfo</span><span class="sxs-lookup"><span data-stu-id="a1881-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="a1881-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="a1881-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
