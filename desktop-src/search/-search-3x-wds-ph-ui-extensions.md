---
description: Um sicherzustellen, dass Ihre Daten während der Suche indiziert und dem Benutzer ordnungsgemäß angezeigt werden, müssen Sie shelldatenspeicher (auch als Shellnamespace Erweiterungen bezeichnet) und Dateityp Handler (auch als Shellerweiterungen, Erweiterungs Handler oder Shellerweiterungs Handler bezeichnet) implementieren.
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Hinzufügen von Symbolen, Vorschauen und Kontextmenüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525532"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="ba6e7-103">Hinzufügen von Symbolen, Vorschauen und Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="ba6e7-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="ba6e7-104">Um sicherzustellen, dass Ihre Daten während der Suche indiziert und dem Benutzer ordnungsgemäß angezeigt werden, müssen Sie shelldatenspeicher (auch als [Shellnamespace Erweiterungen](../shell/nse-works.md)bezeichnet) und Dateityp Handler (auch als Shellerweiterungen, [Erweiterungs Handler](../shell/handlers.md)oder Shellerweiterungs Handler bezeichnet) implementieren.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="ba6e7-105">In diesem Thema werden die folgenden Schnittstellen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="ba6e7-106">Implementieren von Dateityp Handlern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="ba6e7-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="ba6e7-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="ba6e7-108">Ipersistfolder</span><span class="sxs-lookup"><span data-stu-id="ba6e7-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="ba6e7-109">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="ba6e7-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="ba6e7-110">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="ba6e7-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="ba6e7-111">Iextracticon</span><span class="sxs-lookup"><span data-stu-id="ba6e7-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="ba6e7-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="ba6e7-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="ba6e7-113">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba6e7-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ba6e7-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba6e7-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="ba6e7-115">Implementieren von Dateityp Handlern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="ba6e7-116">Diese Shellerweiterungen oder Dateityp Handler stellen den Benutzern die folgenden Shellfunktionen bereit:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="ba6e7-117">Die Ergebnis Ansicht zeigt ein bestimmtes Symbol für den Elementtyp an.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="ba6e7-118">In der Ergebnis Ansicht wird eine Vorschau des Elements angezeigt, wenn der Benutzer das Element auswählt.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="ba6e7-119">Benutzer können auf Elemente doppelklicken, um Ereignisse wie das Öffnen der Datei zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="ba6e7-120">Benutzer können mit der rechten Maustaste auf Elemente klicken, um auf ein Kontextmenü (Kontextmenü) zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="ba6e7-121">Benutzer können Elemente per Drag & amp; Drop verschieben.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="ba6e7-122">Wie alle Component Object Model (com)-Objekte müssen Dateityp Handler eine [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle und eine Klassenfactory implementieren.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="ba6e7-123">In Windows XP oder früheren Versionen sollten Handler außerdem Folgendes implementieren:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="ba6e7-124">Beide [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="ba6e7-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="ba6e7-125">Oder [ishellextinit-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span><span class="sxs-lookup"><span data-stu-id="ba6e7-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="ba6e7-126">In Windows Vista wurden die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) und die [ishellextinit-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) durch die folgenden drei Schnittstellen ersetzt, damit die Shell den Handler initialisieren kann:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="ba6e7-127">IInitializeWithStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba6e7-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="ba6e7-128">IInitializeWithItem-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba6e7-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="ba6e7-129">IInitializeWithFile-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ba6e7-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="ba6e7-130">Zum Bereitstellen eines angemessenen Benutzer Erlebnisses müssen Sie einen Shell-Datenspeicher mit Ihrem Protokollhandler bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="ba6e7-131">Der Datenspeicher dient dann als "Factory" für Symbol Handler, Verknüpfungen von Menü Handlern, Vorschau Handlern usw.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="ba6e7-132">Für die [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)sind minimale Implementierungen der [ipersistent-Schnitt](/windows/desktop/api/objidl/nn-objidl-ipersist) Stelle und die [ipersistfolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) -Schnittstelle erforderlich, und eine minimale Implementierung der IShellFolder-Schnittstelle ist für " [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) " und " [iextracticon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)" erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="ba6e7-133">Der gleiche Klassen Bezeichner (CLSID) sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="ba6e7-134">Weitere Informationen zum Erstellen eines Shell-Datenspeicher zur Unterstützung eines Protokoll Handlers finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ba6e7-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="ba6e7-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="ba6e7-135">IPersist</span></span>

<span data-ttu-id="ba6e7-136">Die **ipersistent** -Schnittstelle definiert die einzelne **GetClassID-** Methode, die für die Bereitstellung der CLSID eines Objekts konzipiert ist, das im System dauerhaft gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="ba6e7-137">Methode</span><span class="sxs-lookup"><span data-stu-id="ba6e7-137">Method</span></span>     | <span data-ttu-id="ba6e7-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba6e7-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="ba6e7-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="ba6e7-139">GetClassID</span></span> | <span data-ttu-id="ba6e7-140">Gibt die CLSID des shelldatenspeicher-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="ba6e7-141">Ipersistfolder</span><span class="sxs-lookup"><span data-stu-id="ba6e7-141">IPersistFolder</span></span>

<span data-ttu-id="ba6e7-142">Die **ipersistfolder** -Schnittstelle wird verwendet, um Shellordner Objekte zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="ba6e7-143">Die Implementierung dieser Schnittstelle, die von **ipersistent** abgeleitet wird, ist die Art und Weise, wie der Ordner im Shellnamespace informiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="ba6e7-144">Sie verwenden diese Schnittstelle nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-144">You do not use this interface directly.</span></span> <span data-ttu-id="ba6e7-145">Sie wird von der Dateisystem Implementierung der [IShellFolder:: BindTo Object-Methode](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) verwendet, wenn ein shellordnerobjekt initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="ba6e7-146">Methode</span><span class="sxs-lookup"><span data-stu-id="ba6e7-146">Method</span></span>     | <span data-ttu-id="ba6e7-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba6e7-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba6e7-148">Initialisieren</span><span class="sxs-lookup"><span data-stu-id="ba6e7-148">Initialize</span></span> | <span data-ttu-id="ba6e7-149">Weist ein shellordnerobjekt an, sich auf der Grundlage der bestandenen Informationen selbst zu initialisieren, und gibt S OK zurück. \_</span><span class="sxs-lookup"><span data-stu-id="ba6e7-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="ba6e7-150">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="ba6e7-150">IShellFolder</span></span>

<span data-ttu-id="ba6e7-151">Die [IShellFolder-Schnittstellen](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Schnittstelle wird zum Verwalten von Ordnern verwendet, und eine partielle Implementierung ist erforderlich, damit die Symbol-und Kontext Schnittstellen, die für einen Protokollhandler implementiert werden, in der Benutzeroberfläche der Windows-Suchergebnisse ordnungsgemäß Verhalten.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="ba6e7-152">Der größte Teil der erforderlichen Funktionalität wird durch die **getuiobjectof** -Methode verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="ba6e7-153">Diese Methode ermöglicht es einem Add-in, die **iextracticon** -Schnittstelle und die **IContextMenu** -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="ba6e7-154">Die [IShellFolder-Schnittstellen](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) Schnittstelle verwendet pidls anstelle von URLs.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="ba6e7-155">Im Gegensatz zu den Anforderungen eines kompletten Shell-Datenspeicher kann für Add-Ins eine einfache IDL-Struktur verwendet werden, die nur die URL enthält.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="ba6e7-156">Die folgenden Methoden der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) müssen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="ba6e7-157">Fünf dieser Methoden erfordern eine minimale Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="ba6e7-158">Methode</span><span class="sxs-lookup"><span data-stu-id="ba6e7-158">Method</span></span>           | <span data-ttu-id="ba6e7-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba6e7-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba6e7-160">Bindjeobject</span><span class="sxs-lookup"><span data-stu-id="ba6e7-160">BindToObject</span></span>     | <span data-ttu-id="ba6e7-161">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ba6e7-162">Bindungsspeicher</span><span class="sxs-lookup"><span data-stu-id="ba6e7-162">BindToStorage</span></span>    | <span data-ttu-id="ba6e7-163">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ba6e7-164">"Ansichts Objekt"</span><span class="sxs-lookup"><span data-stu-id="ba6e7-164">CreateViewObject</span></span> | <span data-ttu-id="ba6e7-165">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ba6e7-166">Setnameof</span><span class="sxs-lookup"><span data-stu-id="ba6e7-166">SetNameOf</span></span>        | <span data-ttu-id="ba6e7-167">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ba6e7-168">Name des Parametern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-168">ParseDisplayName</span></span> | <span data-ttu-id="ba6e7-169">Konvertiert eine URL in die PIDL-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="ba6e7-170">Compareids</span><span class="sxs-lookup"><span data-stu-id="ba6e7-170">CompareIDs</span></span>       | <span data-ttu-id="ba6e7-171">Vergleicht zwei PIDL-Werte.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ba6e7-172">GetDisplayNameOf</span><span class="sxs-lookup"><span data-stu-id="ba6e7-172">GetDisplayNameOf</span></span> | <span data-ttu-id="ba6e7-173">Gibt die URL für eine PIDL zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ba6e7-174">Getuiobjectof</span><span class="sxs-lookup"><span data-stu-id="ba6e7-174">GetUIObjectOf</span></span>    | <span data-ttu-id="ba6e7-175">Diese Methode ähnelt der [IUnknown:: QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="ba6e7-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="ba6e7-176">Wenn ein Symbol angefordert wird, fordert der Aufrufer die IID \_ iextracticon an. Wenn ein Kontextmenü angefordert wird, fordert der Aufrufer das IID \_ IContextMenu an.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="ba6e7-177">**IShellFolder** wird nicht zum Auflisten von Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="ba6e7-178">Dies bedeutet, dass der Anzeige Name eines Ordners die physische URL ist.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="ba6e7-179">Dies kann sich in Zukunft ändern.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="ba6e7-180">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="ba6e7-180">IContextMenu</span></span>

<span data-ttu-id="ba6e7-181">Wenn die Windows-Suche Ergebnisse für den Benutzer anzeigt, kann der Benutzer mit der rechten Maustaste auf ein Element klicken und ein Kontextmenü sehen, das von der **IContextMenu** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="ba6e7-182">Kontextmenüs werden auch als Kontextmenüs bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="ba6e7-183">Die Standardaktion im Kontextmenü ist dieselbe Aktion, die ausgeführt wird, wenn auf das Element Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="ba6e7-184">Ohne die entsprechenden **IShellFolder** -oder **IContextMenu** -Schnittstellen für das Element besteht das Standardverhalten eines Doppelklick Ereignisses darin, die URL als Argument an die [ShellExecute-Funktions](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="ba6e7-185">Weitere Informationen zum Erstellen von Kontextmenü Handlern finden Sie unter [Erstellen von Kontextmenü](../shell/context-menu-handlers.md) Handlern und [Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md) für Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="ba6e7-186">Iextracticon</span><span class="sxs-lookup"><span data-stu-id="ba6e7-186">IExtractIcon</span></span>

<span data-ttu-id="ba6e7-187">**Iextracticon** Ruft ein Symbol für die Windows Search-Benutzeroberfläche basierend auf der URL in der PIDL ab, die von Ihrem Protokollhandler bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="ba6e7-188">Weitere Informationen zum Erstellen von Symbol Handlern finden Sie unter [Erstellen von Symbol Handlern](../shell/how-to-create-icon-handlers.md) und [Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md) für Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="ba6e7-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="ba6e7-189">IPreviewHandler</span></span>

<span data-ttu-id="ba6e7-190">[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) rendert eine umfangreiche Vorschauversion eines ausgewählten Elements in Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="ba6e7-191">Vorschau Versionen sind in Windows Search 4,0 oder Windows Vista mit der Windows-Desktop Suche 3. x verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="ba6e7-192">So erstellen Sie einen benutzerdefinierten Vorschau Handler:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="ba6e7-193">Implementieren Sie einen [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) , der einen [IStream](/windows/win32/api/objidl/nn-objidl-istream)annimmt, und befolgen Sie die Richtlinien, die in [Vorschau Handlern](../shell/preview-handlers.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="ba6e7-194">Registrieren Sie Ihren Vorschau Handler:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-194">Register your preview handler:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  <span data-ttu-id="ba6e7-195">Führen Sie die folgenden beiden Schritte aus, um einen Shellordner für Ihre URL zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="ba6e7-196">Behandeln Sie [iqueryassociation](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) in der [IShellFolder:: getuiobjectof-Methode](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), und geben Sie Ihre Zuordnung für Ihre shellelemente zurück, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="ba6e7-197">Nachdem die Shell den Shellordner abgefragt hat, damit der Datenstrom den Vorschau Handler initialisiert, navigieren Sie zu Ihrer [IShellFolder:: BindToObject-Methoden](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) Methode, behandeln IID \_ IStream und geben einen [IStream](/windows/win32/api/objidl/nn-objidl-istream) an Ihre URL zurück.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="ba6e7-198">Um einen vorhandenen Vorschau Handler für den Dateityp wiederzuverwenden, führen Sie die folgenden beiden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="ba6e7-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="ba6e7-199">Registrieren Sie diesen Vorschau Handler für Ihren Dateityp mithilfe der CLSID des vorhandenen Vorschau Handlers anstelle <Ihrer \_ PreviewHandler- \_ GUID>.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="ba6e7-200">Implementieren Sie einen Shellordner.</span><span class="sxs-lookup"><span data-stu-id="ba6e7-200">Implement a Shell folder.</span></span>

<span data-ttu-id="ba6e7-201">Weitere Informationen zum Erstellen von Vorschau Handlern finden Sie unter [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) -und [Vorschau Handler](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e7-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba6e7-202">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba6e7-202">Additional Resources</span></span>

-   <span data-ttu-id="ba6e7-203">Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e7-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="ba6e7-204">Weitere Informationen zum Erstellen von Handlern finden Sie unter [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md), [Erstellen von Shellerweiterungs Handlern](../shell/handlers.md), [Kontextmenü](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell-Namespace Erweiterungen](../shell/nse-works.md) und [Vorschau Handler](../shell/preview-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e7-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba6e7-205">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba6e7-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ba6e7-206">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ba6e7-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ba6e7-207">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="ba6e7-208">Grundlegendes zu Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="ba6e7-209">Benachrichtigen des Index von Änderungen</span><span class="sxs-lookup"><span data-stu-id="ba6e7-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="ba6e7-210">Code Beispiel: Shellerweiterungen für Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="ba6e7-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="ba6e7-211">Installieren und Registrieren von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="ba6e7-212">Erstellen eines Suchconnector für einen Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="ba6e7-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="ba6e7-213">Debuggen von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="ba6e7-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
