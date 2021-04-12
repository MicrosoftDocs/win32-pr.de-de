---
title: Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen
description: Sie können die Benutzeroberflächen Funktionen von Microsoft Windows Desktop Search (WDS) und dem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "104208747"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="042f8-103">Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen</span><span class="sxs-lookup"><span data-stu-id="042f8-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="042f8-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="042f8-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="042f8-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="042f8-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="042f8-106">Sie können die Benutzeroberflächen Funktionen von Microsoft Windows Desktop Search (WDS) und dem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="042f8-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="042f8-107">Ohne weitere Erweiterung enthält der Protokollhandler, den Sie erstellen, nicht die folgenden Benutzeroberflächen:</span><span class="sxs-lookup"><span data-stu-id="042f8-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="042f8-108">In WDS werden keine spezifischen Symbole für Ihre Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="042f8-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="042f8-109">Wenn Benutzer auf ein Element doppelklicken, reagiert die Benutzeroberfläche nicht auf das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="042f8-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="042f8-110">Wenn Benutzer mit der rechten Maustaste auf ein Element klicken, werden keine Vorgänge für das Element vom Kontextmenü unterstützt.</span><span class="sxs-lookup"><span data-stu-id="042f8-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="042f8-111">Für **IShellFolder** sind minimale Implementierungen von **ipersistent** und **ipersistfolder** erforderlich, und für **IContextMenu** und **iextracticon** ist eine minimale Implementierung von **IShellFolder** erforderlich. die beiden Schnittstellen bieten eine nahtlose Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="042f8-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="042f8-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="042f8-112">IPersist</span></span>

<span data-ttu-id="042f8-113">Die **ipersistent** -Schnittstelle definiert die einzelne **GetClassID-** Methode, die für die Bereitstellung der CLSID eines Objekts konzipiert ist, das im System dauerhaft gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="042f8-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="042f8-114">Methode</span><span class="sxs-lookup"><span data-stu-id="042f8-114">Method</span></span>       | <span data-ttu-id="042f8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="042f8-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="042f8-116">GetClassID ()</span><span class="sxs-lookup"><span data-stu-id="042f8-116">GetClassID()</span></span> | <span data-ttu-id="042f8-117">Gibt die ClassID des Protokoll Handlers zurück.</span><span class="sxs-lookup"><span data-stu-id="042f8-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="042f8-118">Die gleiche CLSID sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="042f8-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="042f8-119">Ipersistfolder</span><span class="sxs-lookup"><span data-stu-id="042f8-119">IPersistFolder</span></span>

<span data-ttu-id="042f8-120">Die **ipersistfolder** -Schnittstelle wird verwendet, um Shellordner Objekte zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="042f8-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="042f8-121">Die Implementierung dieser Schnittstelle, die von **ipersistent** abgeleitet wird, ist die Art und Weise, wie der Ordner im Shellnamespace informiert wird.</span><span class="sxs-lookup"><span data-stu-id="042f8-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="042f8-122">Methode</span><span class="sxs-lookup"><span data-stu-id="042f8-122">Method</span></span>       | <span data-ttu-id="042f8-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="042f8-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="042f8-124">Initialisieren ()</span><span class="sxs-lookup"><span data-stu-id="042f8-124">Initialize()</span></span> | <span data-ttu-id="042f8-125">Weist ein shellordnerobjekt an, sich auf der Grundlage der bestandenen Informationen selbst zu initialisieren, und gibt S OK zurück. \_</span><span class="sxs-lookup"><span data-stu-id="042f8-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="042f8-126">Die gleiche CLSID sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="042f8-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="042f8-127">Sie verwenden diese Schnittstelle nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="042f8-127">You do not use this interface directly.</span></span> <span data-ttu-id="042f8-128">Sie wird von der Dateisystem Implementierung der IShellFolder:: bindtoken Object-Schnittstelle verwendet, wenn ein shellordnerobjekt initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="042f8-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="042f8-129">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="042f8-129">IShellFolder</span></span>

<span data-ttu-id="042f8-130">Die **IShellFolder** -Schnittstelle wird zum Verwalten von Ordnern verwendet, und eine partielle Implementierung ist erforderlich, damit die Symbol-und Kontext Schnittstellen, die für einen Protokollhandler implementiert werden, auf der Benutzeroberfläche der Windows-Desktop Suchergebnisse ordnungsgemäß Verhalten.</span><span class="sxs-lookup"><span data-stu-id="042f8-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="042f8-131">Der größte Teil der erforderlichen Funktionalität wird durch die **getuiobjectof** -Methode verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="042f8-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="042f8-132">Diese Methode ermöglicht es einem Add-in, die **iextracticon** -Schnittstelle und die **IContextMenu** -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="042f8-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="042f8-133">Die **IShellFolder** -Schnittstelle verwendet pidls anstelle von URLs.</span><span class="sxs-lookup"><span data-stu-id="042f8-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="042f8-134">Im Gegensatz zu den Anforderungen einer kompletten Namespace Erweiterung können Add-Ins eine einfache IDL-Struktur verwenden, die nur die URL enthält.</span><span class="sxs-lookup"><span data-stu-id="042f8-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="042f8-135">Die folgenden Methoden von **IShellFolder** müssen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="042f8-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="042f8-136">Beachten Sie, dass für fünf dieser Methoden eine minimale Implementierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="042f8-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="042f8-137">Methode</span><span class="sxs-lookup"><span data-stu-id="042f8-137">Method</span></span>             | <span data-ttu-id="042f8-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="042f8-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="042f8-139">Bindtoken ()</span><span class="sxs-lookup"><span data-stu-id="042f8-139">BindToObject()</span></span>     | <span data-ttu-id="042f8-140">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="042f8-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="042f8-141">Bindesstorage ()</span><span class="sxs-lookup"><span data-stu-id="042f8-141">BindToStorage()</span></span>    | <span data-ttu-id="042f8-142">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="042f8-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="042f8-143">"Kreateviewobject ()"</span><span class="sxs-lookup"><span data-stu-id="042f8-143">CreateViewObject()</span></span> | <span data-ttu-id="042f8-144">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="042f8-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="042f8-145">Setnameof ()</span><span class="sxs-lookup"><span data-stu-id="042f8-145">SetNameOf()</span></span>        | <span data-ttu-id="042f8-146">Gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="042f8-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="042f8-147">Parameydisplay Name ()</span><span class="sxs-lookup"><span data-stu-id="042f8-147">ParseDisplayName()</span></span> | <span data-ttu-id="042f8-148">Konvertiert eine URL in die PIDL-Struktur.</span><span class="sxs-lookup"><span data-stu-id="042f8-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="042f8-149">Compareids ()</span><span class="sxs-lookup"><span data-stu-id="042f8-149">CompareIDs()</span></span>       | <span data-ttu-id="042f8-150">Vergleicht zwei PIDL-Werte.</span><span class="sxs-lookup"><span data-stu-id="042f8-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="042f8-151">GetDisplayNameOf ()</span><span class="sxs-lookup"><span data-stu-id="042f8-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="042f8-152">Gibt die URL für eine PIDL zurück.</span><span class="sxs-lookup"><span data-stu-id="042f8-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="042f8-153">Getuiobjectof ()</span><span class="sxs-lookup"><span data-stu-id="042f8-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="042f8-154">Diese Methode ähnelt der OLE COM-QueryInterface-Methode.</span><span class="sxs-lookup"><span data-stu-id="042f8-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="042f8-155">Wenn ein Symbol angefordert wird, fordert der Aufrufer die IID \_ iextracticon an. Wenn ein Kontextmenü angefordert wird, fordert der Aufrufer das IID \_ IContextMenu an.</span><span class="sxs-lookup"><span data-stu-id="042f8-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="042f8-156">Die gleiche CLSID sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="042f8-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="042f8-157">**IShellFolder** wird nicht zum Auflisten von Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="042f8-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="042f8-158">Dies bedeutet, dass der Anzeige Name eines Ordners die physische URL ist.</span><span class="sxs-lookup"><span data-stu-id="042f8-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="042f8-159">Dies kann sich in Zukunft ändern.</span><span class="sxs-lookup"><span data-stu-id="042f8-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="042f8-160">IContextMenu</span><span class="sxs-lookup"><span data-stu-id="042f8-160">IContextMenu</span></span>

<span data-ttu-id="042f8-161">Wenn WDS Ergebnisse für den Benutzer anzeigt, kann der Benutzer mit der rechten Maustaste auf ein Element klicken und ein Kontextmenü sehen, das von der **IContextMenu** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="042f8-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="042f8-162">Die Standardaktion im Kontextmenü ist dieselbe Aktion, die ausgeführt wird, wenn auf das Element Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="042f8-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="042f8-163">Ohne die entsprechenden **IShellFolder** -oder **IContextMenu** -Schnittstellen für das Element besteht das Standardverhalten eines Doppelklick Ereignisses darin, die URL als Argument an die ShellExecute-Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="042f8-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="042f8-164">Iextracticon</span><span class="sxs-lookup"><span data-stu-id="042f8-164">IExtractIcon</span></span>

<span data-ttu-id="042f8-165">**Iextracticon** Ruft ein Symbol für die WDS-Benutzeroberfläche basierend auf der URL in der PIDL ab, die von Ihrem Protokollhandler bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="042f8-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="042f8-166">Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="042f8-166">Code Sample</span></span>

<span data-ttu-id="042f8-167">Der [Beispiel Code für die Benutzeroberfläche des benutzerdefinierten Protokoll Handlers](-search-2x-wds-ph-ui-samplecode.md) veranschaulicht eine Implementierung von **IShellFolder** und unterstützende Schnittstellen und bietet Unterstützung für die Bearbeitung der pidls.</span><span class="sxs-lookup"><span data-stu-id="042f8-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="042f8-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="042f8-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="042f8-169">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="042f8-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="042f8-170">Beispiel Code für die Benutzeroberfläche des benutzerdefinierten Protokoll Handlers</span><span class="sxs-lookup"><span data-stu-id="042f8-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="042f8-171">Installieren und Registrieren von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="042f8-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




