---
description: Wählen Sie eine statische oder dynamische Kontextmenümethode aus, wenn Sie ein benutzerdefiniertes Dateiformat in der Windows Shell implementieren.
title: Auswählen einer statischen oder dynamischen Kontextmenümethode
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: dfd73ee052594e1136fe2885ce92b682f229096b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394775"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="1fc07-103">Auswählen einer statischen oder dynamischen Kontextmenümethode</span><span class="sxs-lookup"><span data-stu-id="1fc07-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="1fc07-104">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="1fc07-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1fc07-105">Auswählen einer Verbmethode</span><span class="sxs-lookup"><span data-stu-id="1fc07-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="1fc07-106">Statische Verbmethoden</span><span class="sxs-lookup"><span data-stu-id="1fc07-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="1fc07-107">Bevorzugte dynamische Verbmethoden</span><span class="sxs-lookup"><span data-stu-id="1fc07-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="1fc07-108">Von dynamischen Verbmethoden abgeraten</span><span class="sxs-lookup"><span data-stu-id="1fc07-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="1fc07-109">Erweitern eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="1fc07-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="1fc07-110">Unterstützung für Verbmethoden nach Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="1fc07-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="1fc07-111">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1fc07-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="1fc07-112">Auswählen einer Verbmethode</span><span class="sxs-lookup"><span data-stu-id="1fc07-112">Choose a Verb Method</span></span>

<span data-ttu-id="1fc07-113">Es wird dringend empfohlen, ein Kontextmenü mit einer der statischen Verbmethoden zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="1fc07-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="1fc07-114">Statische Verbmethoden</span><span class="sxs-lookup"><span data-stu-id="1fc07-114">Static Verb Methods</span></span>

<span data-ttu-id="1fc07-115">Statische Verben sind die einfachsten Verben, die implementiert werden müssen, bieten aber dennoch umfangreiche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1fc07-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="1fc07-116">Wählen Sie immer die einfachste Kontextmenümethode aus, die Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="1fc07-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fc07-117">Statisches Verb</span><span class="sxs-lookup"><span data-stu-id="1fc07-117">Static Verb</span></span></th>
<th><span data-ttu-id="1fc07-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fc07-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fc07-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> mit Befehlszeilenparametern</span><span class="sxs-lookup"><span data-stu-id="1fc07-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="1fc07-120">Dies ist das einfachste und vertrauteste Mittel zum Implementieren eines statischen Verbs.</span><span class="sxs-lookup"><span data-stu-id="1fc07-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="1fc07-121">Ein Prozess wird durch einen Aufruf der <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess-Funktion</strong></a> mit den ausgewählten Dateien und optionalen Parametern aufgerufen, die als Befehlszeile übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1fc07-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="1fc07-122">Dadurch wird die Datei oder der Ordner geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1fc07-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="1fc07-123">Für diese Methode gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="1fc07-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="1fc07-124">Die Befehlszeilenlänge ist auf 2.000 Zeichen beschränkt, was die Anzahl der Elemente einschränkt, die das Verb verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="1fc07-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="1fc07-125">Kann nur mit Dateisystemelementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fc07-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="1fc07-126">Aktiviert nicht die erneute Verwendung eines bereits ausgeführten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="1fc07-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="1fc07-127">Erfordert, dass eine ausführbare Datei installiert wird, um das Verb zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1fc07-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fc07-128"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fc07-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="1fc07-129">Eine COM-basierte Verbaktivierung bedeutet, dass die In-Proc- oder Out-of-Proc-Aktivierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fc07-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="1fc07-130"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> unterstützt auch die erneute Verwendung eines bereits ausgeführten Handlers, wenn die <strong>IDropTarget-Schnittstelle</strong> von einem lokalen Server implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="1fc07-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="1fc07-131">Außerdem werden die Elemente perfekt über das gemarshallte Datenobjekt ausgedrückt, und es wird ein Verweis auf die aufrufende Websitekette angezeigt, sodass Sie über <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>queryService</strong></a>mit dem Aufrufer interagieren können.</span><span class="sxs-lookup"><span data-stu-id="1fc07-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fc07-132">Windows 7 und höher: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fc07-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="1fc07-133">Die direkteste Implementierungsmethode.</span><span class="sxs-lookup"><span data-stu-id="1fc07-133">The most direct implementation method.</span></span> <span data-ttu-id="1fc07-134">Da es sich hierbei um eine COM-basierte Aufrufmethode (z.B. DropTarget) handelt, unterstützt diese Schnittstelle die In-Proc- und Out-of-Proc-Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="1fc07-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="1fc07-135">Das Verb implementiert <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> und <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>und optional <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fc07-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="1fc07-136">Die Elemente werden direkt als Shell-Elementarray übergeben, und weitere Parameter des Aufrufrs sind für die Verbimplementierungen verfügbar, einschließlich des Aufrufpunkts, des Tastaturzustands usw.</span><span class="sxs-lookup"><span data-stu-id="1fc07-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fc07-137">Windows 7 und höher:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fc07-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="1fc07-138">Ermöglicht Datenquellen, die ihre Befehlsmodulbefehle über <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> bereitstellen, diese Befehle als Verben in einem Kontextmenü zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1fc07-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="1fc07-139">Da diese Schnittstelle nur die Prozessaktivierung unterstützt, wird die Verwendung durch Shell-Datenquellen empfohlen, die die Implementierung zwischen Befehlen und Kontextmenüs freigeben müssen.</span><span class="sxs-lookup"><span data-stu-id="1fc07-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="1fc07-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) ist ein Hybrid zwischen einem statischen und einem dynamischen Verb.</span><span class="sxs-lookup"><span data-stu-id="1fc07-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="1fc07-141">**IExplorerCommand** wurde in Windows Vista deklariert, aber die Möglichkeit, ein Verb in einem Kontextmenü zu implementieren, ist neu in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1fc07-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="1fc07-142">Weitere Informationen zu [**IDropTarget-**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) und Shell-Abfragen für Dateizuordnungsattribute finden Sie unter [Wahrgenommene Typen und Anwendungsregistrierung.](fa-perceivedtypes.md)</span><span class="sxs-lookup"><span data-stu-id="1fc07-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="1fc07-143">Bevorzugte dynamische Verbmethoden</span><span class="sxs-lookup"><span data-stu-id="1fc07-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="1fc07-144">Die folgenden dynamischen Verbmethoden werden bevorzugt:</span><span class="sxs-lookup"><span data-stu-id="1fc07-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="1fc07-145">Verbtyp</span><span class="sxs-lookup"><span data-stu-id="1fc07-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="1fc07-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fc07-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc07-147">Statisches Verb (in der vorherigen Tabelle aufgeführt) + Erweiterte Abfragesyntax (AQS)</span><span class="sxs-lookup"><span data-stu-id="1fc07-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="1fc07-148">Diese Auswahl ruft dynamische Verbsichtbarkeit ab.</span><span class="sxs-lookup"><span data-stu-id="1fc07-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1fc07-149">Windows 7 und höher: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="1fc07-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="1fc07-150">Diese Auswahl ermöglicht eine allgemeine Implementierung von Verben und Explorer-Befehlen, die im Befehlsmodul in Windows-Explorer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1fc07-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1fc07-151">Windows 7 und höher: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + statisches Verb</span><span class="sxs-lookup"><span data-stu-id="1fc07-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="1fc07-152">Diese Auswahl erhält auch dynamische Verbsichtbarkeit.</span><span class="sxs-lookup"><span data-stu-id="1fc07-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="1fc07-153">Es handelt sich um ein Hybridmodell, bei dem ein einfacher In-Process-Handler verwendet wird, um zu berechnen, ob ein bestimmtes statisches Verb disponiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fc07-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="1fc07-154">Dies kann auf alle Implementierungsmethoden für statische Verben angewendet werden, um ein dynamisches Verhalten zu erzielen und die Gefährdung der In-Process-Logik zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="1fc07-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="1fc07-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) bietet den Vorteil der Ausführung in einem Hintergrundthread und vermeidet dadurch das Hängen der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1fc07-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="1fc07-156">Sie ist erheblich einfacher als [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="1fc07-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="1fc07-157">Von dynamischen Verbmethoden abgeraten</span><span class="sxs-lookup"><span data-stu-id="1fc07-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="1fc07-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ist die leistungsfähigste, aber auch die komplizierteste Methode, die implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1fc07-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="1fc07-159">Sie basiert auf prozessin-process-COM-Objekten, die im Thread des Aufrufers ausgeführt werden. Dies Windows-Explorer, kann aber eine beliebige Anwendung sein, die die Elemente hostet.</span><span class="sxs-lookup"><span data-stu-id="1fc07-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="1fc07-160">**IContextMenu** unterstützt Verbsichtbarkeit, Sortierung und benutzerdefiniertes Zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1fc07-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="1fc07-161">Einige dieser Features wurden den statischen Verbfeatures hinzugefügt, z. B. einem Symbol, das einem Befehl zugeordnet werden soll, und [**IExplorerCommand,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) um die Sichtbarkeit zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="1fc07-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="1fc07-162">Wenn Sie das Kontextmenü für einen Dateityp erweitern müssen, indem Sie ein dynamisches Verb für den Dateityp registrieren, befolgen Sie die Anweisungen unter [Anpassen eines Kontextmenüs mit dynamischen Verben.](shortcut-menu-using-dynamic-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="1fc07-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="1fc07-163">Erweitern eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="1fc07-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="1fc07-164">Nachdem Sie eine Verbmethode ausgewählt haben, können Sie ein Kontextmenü für einen Dateityp erweitern, indem Sie ein statisches Verb für den Dateityp registrieren.</span><span class="sxs-lookup"><span data-stu-id="1fc07-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="1fc07-165">Weitere Informationen finden Sie unter [Erstellen von Kontextmenühandlern.](context-menu-handlers.md)</span><span class="sxs-lookup"><span data-stu-id="1fc07-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="1fc07-166">Unterstützung für Verbmethoden nach Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="1fc07-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="1fc07-167">Die Unterstützung für Verbaufrufmethoden nach Betriebssystem ist in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fc07-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



| <span data-ttu-id="1fc07-168">Verb-Methode</span><span class="sxs-lookup"><span data-stu-id="1fc07-168">Verb Method</span></span>          | <span data-ttu-id="1fc07-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fc07-169">Windows XP</span></span> | <span data-ttu-id="1fc07-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fc07-170">Windows Vista</span></span> | <span data-ttu-id="1fc07-171">Windows 7 und darüber hinaus</span><span class="sxs-lookup"><span data-stu-id="1fc07-171">Windows 7 and beyond</span></span> |
|----------------------|------------|---------------|----------------------|
| <span data-ttu-id="1fc07-172">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="1fc07-172">CreateProcess</span></span>        | <span data-ttu-id="1fc07-173">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-173">X</span></span>          | <span data-ttu-id="1fc07-174">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-174">X</span></span>             | <span data-ttu-id="1fc07-175">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-175">X</span></span>                    |
| <span data-ttu-id="1fc07-176">DDE</span><span class="sxs-lookup"><span data-stu-id="1fc07-176">DDE</span></span>                  | <span data-ttu-id="1fc07-177">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-177">X</span></span>          | <span data-ttu-id="1fc07-178">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-178">X</span></span>             | <span data-ttu-id="1fc07-179">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-179">X</span></span>                    |
| <span data-ttu-id="1fc07-180">DropTarget</span><span class="sxs-lookup"><span data-stu-id="1fc07-180">DropTarget</span></span>           | <span data-ttu-id="1fc07-181">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-181">X</span></span>          | <span data-ttu-id="1fc07-182">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-182">X</span></span>             | <span data-ttu-id="1fc07-183">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-183">X</span></span>                    |
| <span data-ttu-id="1fc07-184">Executecommand</span><span class="sxs-lookup"><span data-stu-id="1fc07-184">ExecuteCommand</span></span>       |            | <span data-ttu-id="1fc07-185">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-185">X</span></span>             | <span data-ttu-id="1fc07-186">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-186">X</span></span>                    |
| <span data-ttu-id="1fc07-187">ExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="1fc07-187">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="1fc07-188">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-188">X</span></span>                    |
| <span data-ttu-id="1fc07-189">ExplorerCommandState</span><span class="sxs-lookup"><span data-stu-id="1fc07-189">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="1fc07-190">X</span><span class="sxs-lookup"><span data-stu-id="1fc07-190">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="1fc07-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fc07-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc07-192">Bewährte Methoden für Kontextmenühandler und Verben für mehrfache Auswahl</span><span class="sxs-lookup"><span data-stu-id="1fc07-192">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="1fc07-193">Erstellen von Kontextmenühandlern</span><span class="sxs-lookup"><span data-stu-id="1fc07-193">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="1fc07-194">Anpassen eines Kontextmenüs mit dynamischen Verben</span><span class="sxs-lookup"><span data-stu-id="1fc07-194">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="1fc07-195">Kontextmenüs und Kontextmenühandler</span><span class="sxs-lookup"><span data-stu-id="1fc07-195">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="1fc07-196">Kontextmenüreferenz</span><span class="sxs-lookup"><span data-stu-id="1fc07-196">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="1fc07-197">Verben und Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="1fc07-197">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
