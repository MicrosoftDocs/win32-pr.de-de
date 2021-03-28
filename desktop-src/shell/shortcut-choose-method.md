---
description: 'Dieses Thema ist wie folgt organisiert:'
title: Auswählen einer statischen oder dynamischen Kontextmenü Methode
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042569"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="4b90a-103">Auswählen einer statischen oder dynamischen Kontextmenü Methode</span><span class="sxs-lookup"><span data-stu-id="4b90a-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="4b90a-104">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="4b90a-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="4b90a-105">Verb Methode auswählen</span><span class="sxs-lookup"><span data-stu-id="4b90a-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="4b90a-106">Statische Verb-Methoden</span><span class="sxs-lookup"><span data-stu-id="4b90a-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="4b90a-107">Bevorzugte dynamische Verb-Methoden</span><span class="sxs-lookup"><span data-stu-id="4b90a-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="4b90a-108">Nicht abgewehrt dynamische Verb Methoden</span><span class="sxs-lookup"><span data-stu-id="4b90a-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="4b90a-109">Erweitern eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="4b90a-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="4b90a-110">Unterstützung für Verb-Methoden nach Betriebs System</span><span class="sxs-lookup"><span data-stu-id="4b90a-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="4b90a-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b90a-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="4b90a-112">Verb Methode auswählen</span><span class="sxs-lookup"><span data-stu-id="4b90a-112">Choose a Verb Method</span></span>

<span data-ttu-id="4b90a-113">Es wird dringend empfohlen, dass Sie ein Kontextmenü mit einer der statischen Verb-Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="4b90a-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="4b90a-114">Statische Verb-Methoden</span><span class="sxs-lookup"><span data-stu-id="4b90a-114">Static Verb Methods</span></span>

<span data-ttu-id="4b90a-115">Statische Verben sind die einfachsten zu implementierenden Verben, aber Sie bieten weiterhin umfassende Funktionen.</span><span class="sxs-lookup"><span data-stu-id="4b90a-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="4b90a-116">Wählen Sie immer die einfachste Kontextmenü Methode aus, die Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="4b90a-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b90a-117">Statisches Verb</span><span class="sxs-lookup"><span data-stu-id="4b90a-117">Static Verb</span></span></th>
<th><span data-ttu-id="4b90a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b90a-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4b90a-119">" <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>Kreateprocess</strong></a> " mit Befehlszeilen Parametern</span><span class="sxs-lookup"><span data-stu-id="4b90a-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="4b90a-120">Dies ist die einfachste und vertraute Methode zum Implementieren eines statischen Verbs.</span><span class="sxs-lookup"><span data-stu-id="4b90a-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="4b90a-121">Ein Prozess wird durch einen Aufruf der Funktion " <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>deateprocess</strong></a> " mit den ausgewählten Dateien und allen optionalen Parametern aufgerufen, die als Befehlszeile übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4b90a-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="4b90a-122">Dadurch wird die Datei oder der Ordner geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4b90a-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="4b90a-123">Für diese Methode gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="4b90a-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="4b90a-124">Die Länge der Befehlszeile ist auf 2000 Zeichen beschränkt, was die Anzahl der Elemente einschränkt, die das Verb verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="4b90a-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="4b90a-125">Kann nur mit Dateisystem Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b90a-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="4b90a-126">Die Wiederverwendung eines bereits laufenden Prozesses wird von nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b90a-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="4b90a-127">Erfordert, dass eine ausführbare Datei installiert wird, um das Verb zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4b90a-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b90a-128"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b90a-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="4b90a-129">Eine COM-basierte Verb Aktivierung bedeutet, dass die in-proc-oder out-of-proc-Aktivierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4b90a-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="4b90a-130"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> unterstützt auch die Wiederverwendung eines bereits laufenden Handlers, wenn die <strong>IDropTarget</strong> -Schnittstelle von einem lokalen Server implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="4b90a-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="4b90a-131">Außerdem werden die Elemente über das gemarshallte Datenobjekt hervorragend ausgedrückt, und es wird ein Verweis auf die aufrufende Site Kette bereitgestellt, sodass Sie mit dem aufrufende Instanz über den <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>interagieren können.</span><span class="sxs-lookup"><span data-stu-id="4b90a-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4b90a-132">Windows 7 und höher: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>iexecutecommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b90a-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="4b90a-133">Die direkteste Implementierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="4b90a-133">The most direct implementation method.</span></span> <span data-ttu-id="4b90a-134">Da es sich hierbei um eine COM-basierte Aufruf Methode (z. b. DropTarget) handelt, unterstützt diese Schnittstelle in-proc und außerhalb der proc-Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="4b90a-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="4b90a-135">Das Verb implementiert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>iexecutecommand</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>iobjectwithselection</strong></a>und optional <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>iinitializecommand</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4b90a-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="4b90a-136">Die Elemente werden direkt als shellelementarray weitergegeben, und weitere Parameter aus dem aufrufende Instanz sind für die Verb-Implementierung verfügbar, einschließlich des Aufruf Punkts, des Tastatur Zustands usw.</span><span class="sxs-lookup"><span data-stu-id="4b90a-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4b90a-137">Windows 7 und höher:<strong>explorercommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="4b90a-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="4b90a-138">Ermöglicht Datenquellen, die ihre Befehls Modul Befehle über <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b90a-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="4b90a-139">Da diese Schnittstelle nur die Prozess interne Aktivierung unterstützt, empfiehlt es sich, von shelldatenquellen zu verwenden, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.</span><span class="sxs-lookup"><span data-stu-id="4b90a-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="4b90a-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) ist ein Hybrid zwischen einem statischen und dynamischen Verb.</span><span class="sxs-lookup"><span data-stu-id="4b90a-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="4b90a-141">**IExplorerCommand** wurde in Windows Vista deklariert, aber seine Fähigkeit zum Implementieren eines Verbs in einem Kontextmenü ist neu in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4b90a-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="4b90a-142">Weitere Informationen zu [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -und Shell-Abfragen für Datei Zuordnungs Attribute finden Sie unter [wahrgenommene Typen und Anwendungs Registrierung](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="4b90a-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="4b90a-143">Bevorzugte dynamische Verb-Methoden</span><span class="sxs-lookup"><span data-stu-id="4b90a-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="4b90a-144">Die folgenden dynamischen Verb Methoden werden bevorzugt:</span><span class="sxs-lookup"><span data-stu-id="4b90a-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="4b90a-145">Vertyp</span><span class="sxs-lookup"><span data-stu-id="4b90a-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="4b90a-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b90a-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b90a-147">Statisches Verb (in der vorherigen Tabelle aufgelistet) + Erweiterte Abfrage Syntax (AQS)</span><span class="sxs-lookup"><span data-stu-id="4b90a-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="4b90a-148">Mit dieser Auswahl wird die Sichtbarkeit des dynamischen Verbs abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4b90a-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4b90a-149">Windows 7 und höher: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="4b90a-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="4b90a-150">Diese Auswahl aktiviert eine gängige Implementierung von Verben-und Explorer-Befehlen, die im Befehls Modul in Windows-Explorer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4b90a-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="4b90a-151">Windows 7 und höher: [**iexplorercommandstate**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + statisches Verb</span><span class="sxs-lookup"><span data-stu-id="4b90a-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="4b90a-152">Diese Auswahl erhält auch dynamische Verb Sichtbarkeit.</span><span class="sxs-lookup"><span data-stu-id="4b90a-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="4b90a-153">Dabei handelt es sich um ein Hybridmodell, bei dem ein einfacher in-Process-Handler verwendet wird, um zu berechnen, ob ein bestimmtes statisches Verb verteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b90a-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="4b90a-154">Dies kann auf alle statischen Verb Implementierungs Methoden angewendet werden, um dynamisches Verhalten zu erreichen und das verfügbar machen der in-Process-Logik zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="4b90a-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="4b90a-155">[**Iexplorercommandstate**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) hat den Vorteil, dass Sie in einem Hintergrund Thread ausgeführt wird. Dadurch wird die Benutzeroberfläche nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="4b90a-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="4b90a-156">Es ist wesentlich einfacher als [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="4b90a-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="4b90a-157">Nicht abgewehrt dynamische Verb Methoden</span><span class="sxs-lookup"><span data-stu-id="4b90a-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="4b90a-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Methode, die implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4b90a-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="4b90a-159">Es basiert auf in-Process-COM-Objekten, die auf dem Thread des Aufrufers ausgeführt werden, der normalerweise Windows Explorer ist, aber eine beliebige Anwendung sein kann, die die Elemente gehostet.</span><span class="sxs-lookup"><span data-stu-id="4b90a-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="4b90a-160">**IContextMenu** unterstützt die Sichtbarkeit, Reihenfolge und benutzerdefinierte Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="4b90a-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="4b90a-161">Einige dieser Features wurden den statischen Verb Features hinzugefügt, z. b. einem Symbol, das einem Befehl zugeordnet werden soll, und [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , um die Sichtbarkeit zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="4b90a-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="4b90a-162">Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie für den Dateityp ein dynamisches Verb registrieren, befolgen Sie die Anweisungen unter [Anpassen eines Kontextmenüs mithilfe dynamischer Verben](shortcut-menu-using-dynamic-verbs.md).</span><span class="sxs-lookup"><span data-stu-id="4b90a-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="4b90a-163">Erweitern eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="4b90a-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="4b90a-164">Nachdem Sie eine Verb Methode ausgewählt haben, können Sie ein Kontextmenü für einen Dateityp erweitern, indem Sie für den Dateityp ein statisches Verb registrieren.</span><span class="sxs-lookup"><span data-stu-id="4b90a-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="4b90a-165">Weitere Informationen finden Sie unter [Erstellen von Kontextmenü Handlern](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="4b90a-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="4b90a-166">Unterstützung für Verb-Methoden nach Betriebs System</span><span class="sxs-lookup"><span data-stu-id="4b90a-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="4b90a-167">In der folgenden Tabelle sind die Unterstützung für Verb Aufruf Methoden nach Betriebssystem aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b90a-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | <span data-ttu-id="4b90a-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b90a-168">Windows XP</span></span> | <span data-ttu-id="4b90a-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b90a-169">Windows Vista</span></span> | <span data-ttu-id="4b90a-170">Windows 7 und darüber hinaus</span><span class="sxs-lookup"><span data-stu-id="4b90a-170">Windows 7 and beyond</span></span> |
| <span data-ttu-id="4b90a-171">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="4b90a-171">CreateProcess</span></span>        | <span data-ttu-id="4b90a-172">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-172">X</span></span>          | <span data-ttu-id="4b90a-173">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-173">X</span></span>             | <span data-ttu-id="4b90a-174">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-174">X</span></span>                    |
| <span data-ttu-id="4b90a-175">DDE</span><span class="sxs-lookup"><span data-stu-id="4b90a-175">DDE</span></span>                  | <span data-ttu-id="4b90a-176">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-176">X</span></span>          | <span data-ttu-id="4b90a-177">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-177">X</span></span>             | <span data-ttu-id="4b90a-178">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-178">X</span></span>                    |
| <span data-ttu-id="4b90a-179">DropTarget</span><span class="sxs-lookup"><span data-stu-id="4b90a-179">DropTarget</span></span>           | <span data-ttu-id="4b90a-180">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-180">X</span></span>          | <span data-ttu-id="4b90a-181">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-181">X</span></span>             | <span data-ttu-id="4b90a-182">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-182">X</span></span>                    |
| <span data-ttu-id="4b90a-183">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="4b90a-183">ExecuteCommand</span></span>       |            | <span data-ttu-id="4b90a-184">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-184">X</span></span>             | <span data-ttu-id="4b90a-185">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-185">X</span></span>                    |
| <span data-ttu-id="4b90a-186">Explorercommand</span><span class="sxs-lookup"><span data-stu-id="4b90a-186">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="4b90a-187">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-187">X</span></span>                    |
| <span data-ttu-id="4b90a-188">Explorercommandstate</span><span class="sxs-lookup"><span data-stu-id="4b90a-188">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="4b90a-189">X</span><span class="sxs-lookup"><span data-stu-id="4b90a-189">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="4b90a-190">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b90a-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b90a-191">Bewährte Methoden für Kontextmenü Handler und Mehrfachauswahl Verben</span><span class="sxs-lookup"><span data-stu-id="4b90a-191">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="4b90a-192">Erstellen von Kontextmenü Handlern</span><span class="sxs-lookup"><span data-stu-id="4b90a-192">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="4b90a-193">Anpassen eines Kontextmenüs mithilfe dynamischer Verben</span><span class="sxs-lookup"><span data-stu-id="4b90a-193">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="4b90a-194">Kontextmenüs und Kontextmenü Handler</span><span class="sxs-lookup"><span data-stu-id="4b90a-194">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="4b90a-195">Verweis auf das Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="4b90a-195">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="4b90a-196">Verben und Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="4b90a-196">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
