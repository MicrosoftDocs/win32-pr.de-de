---
description: Viele System Steuerungsanwendungen zeigen ein Eigenschaften Blatt "Eigenschaften" an, mit dem Benutzer verschiedene Geräte-und Systemeinstellungen anzeigen und ändern können.
title: Registrieren und Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864916"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3d0ff-103">Registrieren und Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung</span><span class="sxs-lookup"><span data-stu-id="3d0ff-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3d0ff-104">Viele System Steuerungsanwendungen zeigen ein Eigenschaften Blatt "Eigenschaften" an, mit dem Benutzer verschiedene Geräte-und Systemeinstellungen anzeigen und ändern können.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="3d0ff-105">Zwei dieser Anwendungen – Maus und Anzeige – ermöglichen es Eigenschaften Blatt Handlern, eine oder mehrere Ihrer Seiten durch eine benutzerdefinierte Seite zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="3d0ff-106">Der folgende Screenshot zeigt das Eigenschaften Blatt für die **Maus Eigenschaften** .</span><span class="sxs-lookup"><span data-stu-id="3d0ff-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![Eigenschaften Blatt "Maus Eigenschaften"](images/propsheethandler3.jpg)

<span data-ttu-id="3d0ff-108">Eigenschaften Blatt Handler für System Steuerungsanwendungen ähneln denen für Dateitypen mit zwei primären Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="3d0ff-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="3d0ff-109">Sie werden von einer System Steuerungsanwendung aufgerufen, nicht von der Shell.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="3d0ff-110">Sie werden anders registriert.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3d0ff-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3d0ff-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3d0ff-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="3d0ff-112">Technologies</span></span>

-   <span data-ttu-id="3d0ff-113">Shell</span><span class="sxs-lookup"><span data-stu-id="3d0ff-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3d0ff-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3d0ff-114">Prerequisites</span></span>

-   <span data-ttu-id="3d0ff-115">Ein Verständnis der Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="3d0ff-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="3d0ff-116">Ein Verständnis der Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="3d0ff-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="3d0ff-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="3d0ff-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3d0ff-118">Schritt 1: Registrieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung</span><span class="sxs-lookup"><span data-stu-id="3d0ff-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3d0ff-119">Ein Eigenschaften Blatt Handler der System Steuerungsanwendung muss unter dem System Steuerungs Unterschlüssel registriert werden.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="3d0ff-120">Dieser Schlüssel kann sich an einem von zwei Speicherorten befinden, je nachdem, ob der Handler pro Benutzer oder Computer bezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="3d0ff-121">Bei der Registrierung pro Benutzer ist der System Steuerungs Unterschlüssel **HKEY \_ Current \_ User** \\ **Control Panel**.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="3d0ff-122">Das \_ \_ in "regstr. h" definierte Makro "regstr Path ControlPanel" kann im Code anstelle von "Systemsteuerung" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="3d0ff-123">Für die Registrierung pro Computer lautet der Speicherort wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3d0ff-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="3d0ff-124">Auf diesen Pfad kann im Code als HKEY \_ local \_ Machine \\ regstr \_ path \_ controlsfolder verwiesen werden. dabei wird das \_ \_ in regstr. h definierte regstr-Pfad controlsfolder-Makro verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="3d0ff-125">Die System Steuerungsanwendungen, die Eigenschaften Blatt Handler das Ersetzen von Seiten gestatten, haben unter dem Unterschlüssel der Systemsteuerung einen Unterschlüssel, der für die Anwendung benannt ist, wie z. b. Maus und Anzeige.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="3d0ff-126">Der Unterschlüssel der Anwendung muss über einen **shellex** -Unterschlüssel mit einem **propertysheethandlers** -Unterschlüssel verfügen.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="3d0ff-127">Fügen Sie zum Registrieren eines Eigenschaften Blatt Handlers dem Unterschlüssel **propertysheethandlers** , der der System Steuerungsanwendung zugeordnet ist, die GUID hinzu.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="3d0ff-128">Erstellen Sie hierzu einen Unterschlüssel des unter Schlüssels **propertysheethandlers** , der für den Eigenschaften Blatt Handler benannt ist, und legen Sie dessen Standardwert auf die Zeichen folgen Form der GUID des Handlers fest.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="3d0ff-129">Im folgenden Beispiel wird ein Eigenschaften Blatt Handler für die Anwendung mit der Maussteuerung auf Computer Basis registriert.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="3d0ff-130">Um es auf Benutzerbasis zu registrieren, ersetzen Sie **HKEY \_ local \_ Machine** \\ **regstr \_ path \_ controlsfolder** durch **HKEY \_ Current \_ User** \\ **regstr \_ path \_ ControlPanel**.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="3d0ff-131">Schritt 2: Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung</span><span class="sxs-lookup"><span data-stu-id="3d0ff-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="3d0ff-132">Das Verfahren zum Implementieren eines Eigenschaften Blatt Handlers für die Systemsteuerung ähnelt sehr dem, das unter [registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="3d0ff-133">Der Hauptunterschied besteht darin, dass [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) jetzt anstelle von [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)eine nicht-Token-Implementierung benötigt.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="3d0ff-134">Wenn eine System Steuerungsanwendung im Begriff ist, das Eigenschaften Blatt anzuzeigen, wird die [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) -Methode des Eigenschaften Blatt Handlers einmal für jede Seite aufgerufen, die ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="3d0ff-135">Der *upageid* -Parameter wird auf die ID der Seite festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="3d0ff-136">Die IDs für die verfügbaren Seiten werden in "cplext. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="3d0ff-137">Die derzeit verfügbaren IDs sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="3d0ff-138">Seiten-ID</span><span class="sxs-lookup"><span data-stu-id="3d0ff-138">Page ID</span></span>                      | <span data-ttu-id="3d0ff-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d0ff-139">Description</span></span>         | <span data-ttu-id="3d0ff-140">System Steuerungsanwendung</span><span class="sxs-lookup"><span data-stu-id="3d0ff-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="3d0ff-141">cplpage- \_ Maus \_ Tasten</span><span class="sxs-lookup"><span data-stu-id="3d0ff-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="3d0ff-142">Die Schaltflächen Seite</span><span class="sxs-lookup"><span data-stu-id="3d0ff-142">The Buttons page</span></span>    | <span data-ttu-id="3d0ff-143">Maus</span><span class="sxs-lookup"><span data-stu-id="3d0ff-143">Mouse</span></span>                     |
| <span data-ttu-id="3d0ff-144">cplpage- \_ Maus \_ ptrmotion</span><span class="sxs-lookup"><span data-stu-id="3d0ff-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="3d0ff-145">Die Bewegungs Seite</span><span class="sxs-lookup"><span data-stu-id="3d0ff-145">The Motion page</span></span>     | <span data-ttu-id="3d0ff-146">Maus</span><span class="sxs-lookup"><span data-stu-id="3d0ff-146">Mouse</span></span>                     |
| <span data-ttu-id="3d0ff-147">cplpage \_ - \_ Mausrad</span><span class="sxs-lookup"><span data-stu-id="3d0ff-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="3d0ff-148">Die Radseite</span><span class="sxs-lookup"><span data-stu-id="3d0ff-148">The Wheel page</span></span>      | <span data-ttu-id="3d0ff-149">Maus</span><span class="sxs-lookup"><span data-stu-id="3d0ff-149">Mouse</span></span>                     |
| <span data-ttu-id="3d0ff-150">cplpage- \_ Tastatur \_ Geschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="3d0ff-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="3d0ff-151">Die Seite "Geschwindigkeit"</span><span class="sxs-lookup"><span data-stu-id="3d0ff-151">The Speed page</span></span>      | <span data-ttu-id="3d0ff-152">Tastatur</span><span class="sxs-lookup"><span data-stu-id="3d0ff-152">Keyboard</span></span>                  |
| <span data-ttu-id="3d0ff-153">cplpage- \_ Anzeige \_ Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3d0ff-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="3d0ff-154">Die Hintergrundseite</span><span class="sxs-lookup"><span data-stu-id="3d0ff-154">The Background page</span></span> | <span data-ttu-id="3d0ff-155">Anzeige</span><span class="sxs-lookup"><span data-stu-id="3d0ff-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="3d0ff-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d0ff-156">Remarks</span></span>

<span data-ttu-id="3d0ff-157">Die Vorgehensweise zum Erstellen und Ersetzen einer Seite ist identisch mit der Vorgehensweise zum Hinzufügen einer Seite.</span><span class="sxs-lookup"><span data-stu-id="3d0ff-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="3d0ff-158">Weitere Informationen finden Sie unter [registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="3d0ff-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



