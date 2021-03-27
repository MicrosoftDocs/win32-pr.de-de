---
description: Dieses Thema ist ein Verweis auf die Einträge, die in einer Autorun. inf-Datei verwendet werden können. Ein Eintrag besteht aus einem Schlüssel und einem Wert.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Autorun. inf-Einträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214442"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="37102-104">Autorun. inf-Einträge</span><span class="sxs-lookup"><span data-stu-id="37102-104">Autorun.inf Entries</span></span>

<span data-ttu-id="37102-105">Dieses Thema ist ein Verweis auf die Einträge, die in einer Autorun. inf-Datei verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="37102-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="37102-106">Ein Eintrag besteht aus einem Schlüssel und einem Wert.</span><span class="sxs-lookup"><span data-stu-id="37102-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="37102-107">[\[Autorun- \] Schlüssel](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="37102-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="37102-108">action</span><span class="sxs-lookup"><span data-stu-id="37102-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="37102-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="37102-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="37102-110">angezeigt</span><span class="sxs-lookup"><span data-stu-id="37102-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="37102-111">label</span><span class="sxs-lookup"><span data-stu-id="37102-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="37102-112">open</span><span class="sxs-lookup"><span data-stu-id="37102-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="37102-113">Useautoplay</span><span class="sxs-lookup"><span data-stu-id="37102-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="37102-114">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37102-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="37102-115">schel</span><span class="sxs-lookup"><span data-stu-id="37102-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="37102-116">\\shellverb</span><span class="sxs-lookup"><span data-stu-id="37102-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="37102-117">[\[Inhalts \] Schlüssel](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="37102-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="37102-118">[\[Exclusivecontentpath- \] Schlüssel](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="37102-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="37102-119">[\[Ignorecontentpath- \] Schlüssel](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="37102-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="37102-120">[\[Schlüssel für "de viceingestall" \]](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="37102-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="37102-121">DriverPath "</span><span class="sxs-lookup"><span data-stu-id="37102-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="37102-122">\[Autorun- \] Schlüssel</span><span class="sxs-lookup"><span data-stu-id="37102-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="37102-123">action</span><span class="sxs-lookup"><span data-stu-id="37102-123">action</span></span>](#parameters)
-   [<span data-ttu-id="37102-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="37102-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="37102-125">angezeigt</span><span class="sxs-lookup"><span data-stu-id="37102-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="37102-126">label</span><span class="sxs-lookup"><span data-stu-id="37102-126">label</span></span>](#parameters)
-   [<span data-ttu-id="37102-127">open</span><span class="sxs-lookup"><span data-stu-id="37102-127">open</span></span>](#parameters)
-   [<span data-ttu-id="37102-128">Useautoplay</span><span class="sxs-lookup"><span data-stu-id="37102-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="37102-129">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37102-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="37102-130">schel</span><span class="sxs-lookup"><span data-stu-id="37102-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="37102-131">\\shellverb</span><span class="sxs-lookup"><span data-stu-id="37102-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="37102-132">action</span><span class="sxs-lookup"><span data-stu-id="37102-132">action</span></span>

<span data-ttu-id="37102-133">Der **Aktions** Eintrag gibt den Text an, der im Dialogfeld "AutoPlay" für den Handler verwendet wird, der das im [Open](#parameters) -oder [ShellExecute](#shellexecute) -Eintrag in der Datei "Autorun. inf" des Mediums angegebene Programm darstellt.</span><span class="sxs-lookup"><span data-stu-id="37102-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="37102-134">Der Wert kann entweder als Text oder als Ressource ausgedrückt werden, die in einer Binärdatei gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="37102-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="37102-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-135">Parameters</span></span>

-   <span data-ttu-id="37102-136">*Action Text*</span><span class="sxs-lookup"><span data-stu-id="37102-136">*ActionText*</span></span>

    <span data-ttu-id="37102-137">Text, der im Dialogfeld "AutoPlay" für den Handler verwendet wird, der das im Eintrag " [Open](#parameters) " oder " [ShellExecute](#shellexecute) " in der Datei "Autorun. inf" des Mediums angegebene Programm darstellt.</span><span class="sxs-lookup"><span data-stu-id="37102-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="37102-138">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="37102-138">*filepath*</span></span>

    <span data-ttu-id="37102-139">Eine Zeichenfolge, die den voll qualifizierten Pfad des Verzeichnisses enthält, das die Binärdatei enthält, die die Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="37102-140">Wenn kein Pfad angegeben wird, muss sich die Datei im Stammverzeichnis des Laufwerks befinden.</span><span class="sxs-lookup"><span data-stu-id="37102-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="37102-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="37102-141">*filename*</span></span>

    <span data-ttu-id="37102-142">Eine Zeichenfolge, die den Namen der Binärdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="37102-143">*resourceID*</span><span class="sxs-lookup"><span data-stu-id="37102-143">*resourceID*</span></span>

    <span data-ttu-id="37102-144">Die ID der Zeichenfolge in der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="37102-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-145">Remarks</span></span>

<span data-ttu-id="37102-146">Der **Aktions** Schlüssel wird nur in Windows XP Service Pack 2 (SP2) oder höher verwendet.</span><span class="sxs-lookup"><span data-stu-id="37102-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="37102-147">Sie wird nur für Laufwerke vom Typ "Laufwerk Wechsel" und "Laufwerk korrigiert" unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="37102-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="37102-148">Im Fall einer Wechsel Datenträger \_ ist der **Aktions** Schlüssel erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37102-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="37102-149">Ein **Action** -Befehl in der Autorun. inf-Datei einer AudioCD oder Movie DVD wird ignoriert, und diese Medienverhalten sich weiterhin wie in Windows XP Service Pack 1 (SP1) und früher.</span><span class="sxs-lookup"><span data-stu-id="37102-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="37102-150">Die im Dialogfeld "AutoPlay" angezeigte Zeichenfolge wird erstellt, indem der im **Aktions** Eintrag angegebene Text mit hart codiertem Text benannt wird, der von der Shell bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="37102-151">Das [Symbol](#parameters) wird daneben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37102-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="37102-152">Dieser Eintrag wird immer als erste Option im Dialogfeld "AutoPlay" angezeigt und ist standardmäßig ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="37102-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="37102-153">Wenn der Benutzer die Option annimmt, wird die durch den Eintrag " [Open](#parameters) " oder " [ShellExecute](#shellexecute) " in der Datei "Autorun. inf" des Mediums angegebene Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="37102-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="37102-154">Die Option **ausgewählte Aktion immer** ausführen ist in dieser Situation nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37102-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="37102-155">Die [Aktions](#parameters) -und [Symbol](#parameters) Tasten definieren die Darstellung der Anwendung, die vom Endbenutzer im Dialogfeld "AutoPlay" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="37102-156">Sie sollten so zusammengesetzt werden, dass Benutzer Sie leicht identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="37102-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="37102-157">Sie sollten die auszuwendende Anwendung, das Unternehmen, das Sie erstellt hat, und alle zugeordneten Branding angeben.</span><span class="sxs-lookup"><span data-stu-id="37102-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="37102-158">Aus Gründen der Abwärtskompatibilität ist der **Aktions** Eintrag für Geräte vom Typ Laufwerk \_ Fixed optional.</span><span class="sxs-lookup"><span data-stu-id="37102-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="37102-159">Bei diesem Typ wird im Dialogfeld "AutoPlay" ein Standardeintrag verwendet, wenn in der Datei "Autorun. inf" kein **Aktions** Eintrag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37102-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="37102-160">Der **Aktions** Eintrag ist für Geräte vom Typ "Laufwerk Wechsel" obligatorisch \_ , die bis jetzt keine Unterstützung für "Autorun. inf" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="37102-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="37102-161">Wenn kein **Aktions** Eintrag vorhanden ist, wird das Dialogfeld "AutoPlay" angezeigt, aber ohne Option zum Starten des zusätzlichen Inhalts.</span><span class="sxs-lookup"><span data-stu-id="37102-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="37102-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="37102-162">CustomEvent</span></span>

<span data-ttu-id="37102-163">Der **CustomEvent** -Eintrag gibt ein benutzerdefiniertes Ereignis zum Wiedergeben von Inhalten an.</span><span class="sxs-lookup"><span data-stu-id="37102-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="37102-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-164">Parameters</span></span>

-   <span data-ttu-id="37102-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="37102-165">*CustomEventName*</span></span>

    <span data-ttu-id="37102-166">Eine Text Zeichenfolge, die den Namen des AutoPlay-Inhalts Ereignisses enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="37102-167">Der Name darf nicht mehr als 100 alphanumerische Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37102-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-168">Remarks</span></span>

<span data-ttu-id="37102-169">Sie können einen benutzerdefinierten Ereignis Namen in die Datei Autorun. inf eines Volumes einschließen.</span><span class="sxs-lookup"><span data-stu-id="37102-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="37102-170">Wenn der Benutzer von der automatischen Wiedergabe zur Verwendung mit dem Volume aufgefordert wird, werden nur Anwendungen angezeigt, die für den angegebenen benutzerdefinierten Ereignis Namen registriert sind.</span><span class="sxs-lookup"><span data-stu-id="37102-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="37102-171">Informationen dazu, wie Sie eine Anwendung als Handler für das benutzerdefinierte AutoPlay-Inhalts Ereignis registrieren können, finden Sie unter [Automatisches Starten mit Autoplay](/previous-versions/windows/apps/hh452731(v=win.10)) oder [Registrieren eines Ereignis Handlers](how-to-register-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="37102-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="37102-172">Im folgenden Beispiel wird der Wert "mycontentonarrival" als neues AutoPlay-Inhalts Ereignis angegeben.</span><span class="sxs-lookup"><span data-stu-id="37102-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="37102-173">icon</span><span class="sxs-lookup"><span data-stu-id="37102-173">icon</span></span>

<span data-ttu-id="37102-174">Der **Symbol** Eintrag gibt ein Symbol an, das das Autorun-aktivierte Laufwerk in der Windows-Benutzeroberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="37102-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="37102-175">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-175">Parameters</span></span>

-   <span data-ttu-id="37102-176">*IconFileName*</span><span class="sxs-lookup"><span data-stu-id="37102-176">*iconfilename*</span></span>

    <span data-ttu-id="37102-177">Der Name einer ICO-, BMP-, exe-oder DLL-Datei, die die Symbol Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="37102-178">Wenn eine Datei mehr als ein Symbol enthält, müssen Sie auch einen NULL basierten Index des Symbols angeben.</span><span class="sxs-lookup"><span data-stu-id="37102-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-179">Remarks</span></span>

<span data-ttu-id="37102-180">Das Symbol stellt in Verbindung mit der Bezeichnung das Autorun-aktivierte Laufwerk in der Windows-Benutzeroberfläche dar.</span><span class="sxs-lookup"><span data-stu-id="37102-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="37102-181">Beispielsweise wird in Windows-Explorer das Laufwerk durch dieses Symbol anstatt durch das Standard Laufwerk Symbol dargestellt.</span><span class="sxs-lookup"><span data-stu-id="37102-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="37102-182">Die Symbol Datei muss sich im gleichen Verzeichnis befinden wie die Datei, die durch den Befehl " [Öffnen](#parameters) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37102-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="37102-183">Im folgenden Beispiel wird das zweite Symbol in der MyProg.exe-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="37102-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="37102-184">label</span><span class="sxs-lookup"><span data-stu-id="37102-184">label</span></span>

<span data-ttu-id="37102-185">Der Bezeichnungs Eintrag gibt eine Text Bezeichnung an, die das Autorun-aktivierte Laufwerk **in der Windows** -Benutzeroberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="37102-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="37102-186">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-186">Parameters</span></span>

-   <span data-ttu-id="37102-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="37102-187">*LabelText*</span></span>

    <span data-ttu-id="37102-188">Eine Text Zeichenfolge, die die Bezeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-188">A text string containing the label.</span></span> <span data-ttu-id="37102-189">Sie kann Leerzeichen enthalten und darf nicht länger als 32 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="37102-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="37102-190">Es ist möglich, einen Wert in den Parameter " **LabelText** " einzufügen, der mehr als 32 Zeichen enthält und keine Fehlermeldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="37102-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="37102-191">Das System zeigt jedoch nur die ersten 32 Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="37102-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="37102-192">Alle Zeichen nach dem 32. werden abgeschnitten und nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37102-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="37102-193">Beispiel: " **LabelText** " lautet wie folgt: Bezeichnung = "diese CD ist als ultimative Musik-CD konzipiert."</span><span class="sxs-lookup"><span data-stu-id="37102-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="37102-194">Folgendes wird angezeigt: "diese CD ist als UL konzipiert."</span><span class="sxs-lookup"><span data-stu-id="37102-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="37102-195">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-195">Remarks</span></span>

<span data-ttu-id="37102-196">Die Bezeichnung stellt in Verbindung mit einem Symbol das Autorun-aktivierte Laufwerk in der Windows-Benutzeroberfläche dar.</span><span class="sxs-lookup"><span data-stu-id="37102-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="37102-197">Im folgenden Beispiel wird der Wert "My Drive Label" als Bezeichnung des Laufwerks angegeben.</span><span class="sxs-lookup"><span data-stu-id="37102-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="37102-198">open</span><span class="sxs-lookup"><span data-stu-id="37102-198">open</span></span>

<span data-ttu-id="37102-199">Der Eintrag **Öffnen** gibt den Pfad und den Dateinamen der Anwendung an, die gestartet wird, wenn ein Benutzer einen Datenträger in das Laufwerk einfügt.</span><span class="sxs-lookup"><span data-stu-id="37102-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="37102-200">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-200">Parameters</span></span>

-   <span data-ttu-id="37102-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="37102-201">*exefile*</span></span>

    <span data-ttu-id="37102-202">Voll qualifizierter Pfad einer ausführbaren Datei, die beim Einfügen der CD ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="37102-203">Wenn nur ein Dateiname angegeben wird, muss er sich im Stammverzeichnis des Laufwerks befinden.</span><span class="sxs-lookup"><span data-stu-id="37102-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="37102-204">Wenn Sie die Datei in einem Unterverzeichnis suchen möchten, müssen Sie einen Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="37102-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="37102-205">Sie können auch einen oder mehrere Befehlszeilenparameter einschließen, um Sie an die Start Anwendung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="37102-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="37102-206">Useautoplay</span><span class="sxs-lookup"><span data-stu-id="37102-206">UseAutoPlay</span></span>

<span data-ttu-id="37102-207">Unter Windows XP gibt der **useautoplay** -Eintrag an, dass AutoPlay anstelle von Autorun verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37102-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="37102-208">Unter Windows Vista und höher bewirkt dieser Eintrag, dass alle für Autorun angegebenen Aktionen (entweder mithilfe der Einträge " **Open** " oder " **ShellExecute** ") im Dialogfeld "AutoPlay" unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="37102-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="37102-209">Dieser Eintrag hat keine Auswirkung auf ältere Windows-Versionen als Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37102-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="37102-210">Wenn Sie unter Windows 8 und höher den Wert 0 angeben, wird die automatische Wiedergabe für dieses Gerät deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="37102-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="37102-211">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-211">Parameters</span></span>

<span data-ttu-id="37102-212">Um diese Option zu verwenden, fügen Sie der Datei Autorun. inf einen Eintrag für **useautoplay** hinzu, und legen Sie den Eintrag auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="37102-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="37102-213">In Windows-Versionen vor Windows 8 wird kein anderer Wert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37102-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="37102-214">Geben Sie unter Windows 8 und höher den Wert 0 an, um die automatische Wiedergabe für dieses Gerät zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="37102-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="37102-215">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-215">Remarks</span></span>

<span data-ttu-id="37102-216">**Useautoplay** ist derzeit nur unter Windows XP oder höher und nur auf einem Laufwerk anwendbar, das von [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) als **Laufwerk- \_ CDROM** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="37102-217">Wenn **useautoplay** verwendet wird, werden alle Aktionen, die von den Einträgen " **Open** " oder " **ShellExecute** " in "Autorun. inf" angegeben werden, unter Windows XP ignoriert und im Dialogfeld "AutoPlay" unter Windows Vista ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="37102-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="37102-218">Autorun wird in der Regel zum automatischen Ausführen oder Laden von auf den eingefügten Medien enthaltenen Medien verwendet, während die automatische Wiedergabe ein Dialogfeld mit einer Liste relevanter Aktionen darstellt, die durchgeführt werden können, und dem Benutzer die Auswahl der auszuführenden Aktion ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="37102-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="37102-219">Weitere Informationen zu den Unterschieden zwischen Autorun und AutoPlay finden Sie unter [Erstellen einer Autorun-aktivierten CD-ROM-Anwendung](autoplay.md) und [verwenden und Konfigurieren der automatischen AutoPlay](autoplay2k-using.md).</span><span class="sxs-lookup"><span data-stu-id="37102-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="37102-220">Verwendungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="37102-220">Usage Example</span></span>

<span data-ttu-id="37102-221">Eine CD enthält drei Dateien: autorun. inf, Readme.txt und Music. WMA.</span><span class="sxs-lookup"><span data-stu-id="37102-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="37102-222">Abhängig von der verwendeten Windows-Version und den in Autorun. inf angegebenen Optionen kann die CD beim Einfügen entweder durch Autorun oder AutoPlay verarbeitet werden (vorausgesetzt, Autorun/AutoPlay ist für das Laufwerk aktiviert, in das die CD eingefügt wird).</span><span class="sxs-lookup"><span data-stu-id="37102-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="37102-223">Nehmen Sie zunächst eine Autorun. inf-Datei mit folgendem Inhalt in Erwägung, und beachten Sie, dass **useautoplay = 1** nicht angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="37102-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="37102-224">Die Aktion, die von der Shell durchgeführt wird, wenn diese CD eingefügt wird, hängt von der verwendeten Windows-Version ab:</span><span class="sxs-lookup"><span data-stu-id="37102-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="37102-225">Unter Windows XP oder früher wird diese CD von Autorun verarbeitet, wenn Sie eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="37102-226">In diesem Fall wird der Eintrag **ShellExecute** gelesen, und die Shell Ruft den Datei Handler auf, der den txt-Dateien zugeordnet ist. in der Regel würde dies Readme.txt in Notepad öffnen.</span><span class="sxs-lookup"><span data-stu-id="37102-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="37102-227">Unter Windows Vista bewirkt das vorhanden sein einer Autorun. inf-Datei mit einem **ShellExecute** -Eintrag, dass das Medium als AutoPlay-Typ "Software und Games" identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="37102-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="37102-228">In diesem Fall wird dem Benutzer ein Dialogfeld für die automatische Wiedergabe angezeigt, in dem die durch den Eintrag **ShellExecute** angegebene Aktion (als "Load Readme.txt" im Dialogfeld dargestellt) zusammen mit den Medien vom Typ "Software und Spiele" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="37102-229">Um anzugeben, dass AutoPlay anstelle von Autorun unter Windows XP verwendet werden soll, und dass die vom Autorun ShellExecute-Eintrag angegebene Aktion im Dialogfeld "AutoPlay" unter Windows Vista unterdrückt werden soll, fügen Sie **useautoplay** wie folgt in die Datei Autorun. inf ein:</span><span class="sxs-lookup"><span data-stu-id="37102-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="37102-230">Die Aktion, die von der Shell durchgeführt wird, wenn diese CD eingefügt wird, hängt von der verwendeten Windows-Version ab.</span><span class="sxs-lookup"><span data-stu-id="37102-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="37102-231">In früheren Windows-Versionen als Windows XP wird Autorun weiterhin verwendet, und die von **ShellExecute** angegebene Aktion wird ausgeführt, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="37102-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="37102-232">(Beachten Sie, dass nur Autorun in früheren Windows-Versionen als Windows XP verfügbar ist.)</span><span class="sxs-lookup"><span data-stu-id="37102-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="37102-233">Unter Windows XP bewirkt der **useautoplay** -Eintrag, dass AutoPlay anstelle von Autorun verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37102-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="37102-234">In diesem Fall wird durch die automatische Wiedergabe festgelegt, dass das Medium eine Windows Media Audio Datei (. WMA) enthält, und der Inhalt wird als "Musikdateien" kategorisiert.</span><span class="sxs-lookup"><span data-stu-id="37102-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="37102-235">Dem Benutzer wird ein Dialogfeld für die automatische Wiedergabe mit registrierten Handlern für den Medientyp "Musikdateien" angezeigt. der Eintrag Autorun ShellExecute wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="37102-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="37102-236">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="37102-236">shellexecute</span></span>

[<span data-ttu-id="37102-237">Version 5,0.</span><span class="sxs-lookup"><span data-stu-id="37102-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="37102-238">Der Eintrag **ShellExecute** gibt eine Anwendung oder eine Datendatei an, die Autorun zum Aufrufen von [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)verwendet.</span><span class="sxs-lookup"><span data-stu-id="37102-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="37102-239">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-239">Parameters</span></span>

-   <span data-ttu-id="37102-240">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="37102-240">*filepath*</span></span>

    <span data-ttu-id="37102-241">Eine Zeichenfolge, die den voll qualifizierten Pfad des Verzeichnisses enthält, das die Daten oder die ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="37102-242">Wenn kein Pfad angegeben wird, muss sich die Datei im Stammverzeichnis des Laufwerks befinden.</span><span class="sxs-lookup"><span data-stu-id="37102-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="37102-243">*filename*</span><span class="sxs-lookup"><span data-stu-id="37102-243">*filename*</span></span>

    <span data-ttu-id="37102-244">Eine Zeichenfolge, die den Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="37102-244">A string that contains the file's name.</span></span> <span data-ttu-id="37102-245">Wenn es sich um eine ausführbare Datei handelt, wird Sie gestartet.</span><span class="sxs-lookup"><span data-stu-id="37102-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="37102-246">Wenn es sich um eine Datendatei handelt, muss Sie ein Member eines [Dateityps](fa-file-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="37102-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="37102-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) starten Sie den Standardbefehl, der dem Dateityp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="37102-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="37102-248">*paramx*</span><span class="sxs-lookup"><span data-stu-id="37102-248">*paramx*</span></span>

    <span data-ttu-id="37102-249">Enthält alle zusätzlichen Parameter, die an [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)weitergeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37102-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-250">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-250">Remarks</span></span>

<span data-ttu-id="37102-251">Dieser Eintrag ist ähnlich wie [geöffnet](#parameters), ermöglicht Ihnen jedoch die Verwendung von [Datei](fa-intro.md) Zuordnungs Informationen, um die Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="37102-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="37102-252">Shell</span><span class="sxs-lookup"><span data-stu-id="37102-252">shell</span></span>

<span data-ttu-id="37102-253">Der **shelleintrag** gibt einen Standardbefehl für das Kontextmenü des Laufwerks an.</span><span class="sxs-lookup"><span data-stu-id="37102-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="37102-254">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-254">Parameters</span></span>

-   <span data-ttu-id="37102-255">*Verb*</span><span class="sxs-lookup"><span data-stu-id="37102-255">*verb*</span></span>

    <span data-ttu-id="37102-256">Das Verb, das dem Menübefehl entspricht.</span><span class="sxs-lookup"><span data-stu-id="37102-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="37102-257">Das Verb und der zugehörige Menübefehl müssen in der Datei "Autorun. inf" mit [einem \\ shellverb](#shellverb) Eintrag definiert werden.</span><span class="sxs-lookup"><span data-stu-id="37102-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-258">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-258">Remarks</span></span>

<span data-ttu-id="37102-259">Wenn ein Benutzer mit der rechten Maustaste auf das Laufwerk Symbol klickt, wird ein Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37102-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="37102-260">Wenn eine Autorun. inf-Datei vorhanden ist, wird der Standardkontext Menübefehl davon übernommen.</span><span class="sxs-lookup"><span data-stu-id="37102-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="37102-261">Dieser Befehl wird auch ausgeführt, wenn der Benutzer auf das Laufwerk Symbol doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="37102-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="37102-262">Um den Standardkontext Menübefehl anzugeben, definieren Sie zuerst das Verb, die Befehls Zeichenfolge und den Menütext mit dem [ \\ shellverb](#shellverb).</span><span class="sxs-lookup"><span data-stu-id="37102-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="37102-263">Verwenden Sie dann Shell, um Sie als Standardkontext Menübefehl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37102-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="37102-264">Andernfalls ist der Standardmenü Element Text "AutoPlay", wodurch die Anwendung gestartet wird, die durch den [geöffneten](#parameters) Eintrag angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="37102-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="37102-265">\\shellverb</span><span class="sxs-lookup"><span data-stu-id="37102-265">shell\\verb</span></span>

<span data-ttu-id="37102-266">Mit dem Eintrag für den **\\ shellverb** wird dem Kontextmenü des Laufwerks ein benutzerdefinierter Befehl hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="37102-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="37102-267">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-267">Parameters</span></span>

-   <span data-ttu-id="37102-268">*Verb*</span><span class="sxs-lookup"><span data-stu-id="37102-268">*verb*</span></span>

    <span data-ttu-id="37102-269">Das Verb des Menübefehls.</span><span class="sxs-lookup"><span data-stu-id="37102-269">The menu command's verb.</span></span> <span data-ttu-id="37102-270">Der *_\\ Befehls_* Eintrag des **\\ shellverbs** ordnet das Verb einer ausführbaren Datei zu.</span><span class="sxs-lookup"><span data-stu-id="37102-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="37102-271">Verben dürfen keine eingebetteten Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37102-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="37102-272">Standardmäßig ist das *Verb* der Text, der im Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="37102-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="37102-273">*Filename.exe*</span></span>

    <span data-ttu-id="37102-274">Der Pfad und der Dateiname der Anwendung, die die Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="37102-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="37102-275">*MenuText*</span><span class="sxs-lookup"><span data-stu-id="37102-275">*MenuText*</span></span>

    <span data-ttu-id="37102-276">Dieser Parameter gibt den Text an, der im Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="37102-277">Wenn der Wert weggelassen wird, wird das *Verb* angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37102-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="37102-278">*MenuText* kann gemischt und Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37102-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="37102-279">Sie können eine Tastenkombination für das Menü Element festlegen, indem Sie ein kaufmännisches und-Element (&) vor dem Buchstaben platzieren.</span><span class="sxs-lookup"><span data-stu-id="37102-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-280">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-280">Remarks</span></span>

<span data-ttu-id="37102-281">Wenn ein Benutzer mit der rechten Maustaste auf das Laufwerk Symbol klickt, wird ein Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37102-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="37102-282">Durch das Hinzufügen von **\\ shellverb** Einträgen zur Autorun. inf-Datei des Laufwerks können Sie diesem Kontextmenü Befehle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="37102-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="37102-283">Dieser Eintrag besteht aus zwei Teilen, die sich in separaten Zeilen befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="37102-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="37102-284">Der erste Teil ist der *_\\ Befehl_* **\\ shellverb**.</span><span class="sxs-lookup"><span data-stu-id="37102-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="37102-285">Sie ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37102-285">It is required.</span></span> <span data-ttu-id="37102-286">Eine Zeichenfolge, die als *Verb* bezeichnet wird, wird mit der Anwendung verknüpft, die beim Ausführen des Befehls gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37102-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="37102-287">Der zweite Teil ist der **\\ shellverb** Eintrag.</span><span class="sxs-lookup"><span data-stu-id="37102-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="37102-288">Der Vorgang ist optional.</span><span class="sxs-lookup"><span data-stu-id="37102-288">It is optional.</span></span> <span data-ttu-id="37102-289">Sie können ihn einschließen, um den Text anzugeben, der im Kontextmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="37102-290">Um einen Standardkontext Menübefehl anzugeben, definieren Sie das Verb mit dem **\\ shellverb**, und legen Sie es als Standardbefehl mit dem [shelleintrag](#autoruninf-entries) fest.</span><span class="sxs-lookup"><span data-stu-id="37102-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="37102-291">Das folgende Autorun. inf-Beispiel Fragment *ordnet das Readit* -Verb der Befehls Zeichenfolge "Notepad ABC \\readme.txt" zu.</span><span class="sxs-lookup"><span data-stu-id="37102-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="37102-292">Der Menütext ist "Read Me", und "'m" ist als Tastenkombination des Elements definiert.</span><span class="sxs-lookup"><span data-stu-id="37102-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="37102-293">Wenn der Benutzer diesen Befehl auswählt, wird die Datei ABCreadme.txt des Laufwerks \\ mit Microsoft Notepad geöffnet.</span><span class="sxs-lookup"><span data-stu-id="37102-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="37102-294">\[Inhalts \] Schlüssel</span><span class="sxs-lookup"><span data-stu-id="37102-294">\[Content\] Keys</span></span>

<span data-ttu-id="37102-295">Es gibt drei Dateityp Schlüssel: " **musicfiles**", " **PictureFiles**" und " **Videofiles**".</span><span class="sxs-lookup"><span data-stu-id="37102-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="37102-296">Wenn einer dieser Inhalte durch die Werte 1, y, Yes, t oder true auf true festgelegt ist, zeigt die Autoplay-Benutzeroberfläche die diesem Inhaltstyp zugeordneten Handler an, unabhängig davon, ob Inhalt dieses Typs auf dem Medium vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37102-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="37102-297">Wenn einer dieser Inhalte durch die Werte 0, n, Nein, f oder false auf false festgelegt ist, werden die diesem Inhaltstyp zugeordneten Handler von der Benutzeroberfläche für die automatische Wiedergabe nicht angezeigt, auch wenn Inhalt dieses Typs auf dem Medium erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="37102-298">Die Verwendung dieses Abschnitts soll Inhalts Entwicklern ermöglichen, die Absicht von Inhalten an die automatische Wiedergabe zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="37102-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="37102-299">Beispielsweise kann eine CD so kategorisiert werden, dass Sie nur Musikinhalte enthält, obwohl Sie auch über Bilder und Videos verfügt und andernfalls als gemischte Inhalte angesehen werden würde.</span><span class="sxs-lookup"><span data-stu-id="37102-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="37102-300">Der Abschnitt " **\[ Inhalt \]** " wird nur unter Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37102-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="37102-301">\[Exclusivecontentpath- \] Schlüssel</span><span class="sxs-lookup"><span data-stu-id="37102-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="37102-302">Die in diesem Abschnitt aufgeführten Ordner schränken die automatische Wiedergabe ein, um nur die Ordner und deren Unterordner nach Inhalt zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="37102-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="37102-303">Sie können mit oder ohne einen führenden umgekehrten Schrägstrich () angegeben werden \\ .</span><span class="sxs-lookup"><span data-stu-id="37102-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="37102-304">In beiden Fällen werden Sie als absolute Pfade aus dem Stammverzeichnis des Mediums übernommen.</span><span class="sxs-lookup"><span data-stu-id="37102-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="37102-305">Wenn Ordner mit Leerzeichen in ihren Namen vorliegen, dürfen diese nicht in Anführungszeichen eingeschlossen werden, da die Anführungszeichen als Teil des Pfads wörtlich genommen werden.</span><span class="sxs-lookup"><span data-stu-id="37102-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="37102-306">Die Verwendung dieses Abschnitts soll es Autoren von Inhalten ermöglichen, die Absicht von Inhalten an die automatische Wiedergabe zu übermitteln und die Überprüfungs Zeit zu verkürzen, indem die Überprüfung auf bestimmte wichtige Bereiche der Medien beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="37102-307">Die folgenden Pfade sind gültig.</span><span class="sxs-lookup"><span data-stu-id="37102-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="37102-308">Der Abschnitt " **\[ exclusivecontentpath \]** " wird nur unter Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37102-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="37102-309">\[Ignorecontentpath- \] Schlüssel</span><span class="sxs-lookup"><span data-stu-id="37102-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="37102-310">Die in diesem Abschnitt aufgeführten Ordner und deren Unterordner werden bei der Suche nach Inhalten von einem Medium ignoriert.</span><span class="sxs-lookup"><span data-stu-id="37102-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="37102-311">Sie können mit oder ohne einen führenden umgekehrten Schrägstrich () angegeben werden \\ .</span><span class="sxs-lookup"><span data-stu-id="37102-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="37102-312">In beiden Fällen werden Sie als absolute Pfade aus dem Stammverzeichnis des Mediums übernommen.</span><span class="sxs-lookup"><span data-stu-id="37102-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="37102-313">Wenn Ordner mit Leerzeichen in ihren Namen vorliegen, dürfen diese nicht in Anführungszeichen eingeschlossen werden, da die Anführungszeichen als Teil des Pfads wörtlich genommen werden.</span><span class="sxs-lookup"><span data-stu-id="37102-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="37102-314">Die Pfade in diesem Abschnitt haben Vorrang vor Pfaden im Abschnitt **\[ exclusivecontentpath \]** .</span><span class="sxs-lookup"><span data-stu-id="37102-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="37102-315">Wenn ein in **\[ ignorecontentpath \]** angegebener Pfad ein Unterordner eines in **\[ exclusivecontentpath \]** angegebenen Pfads ist, wird er weiterhin ignoriert.</span><span class="sxs-lookup"><span data-stu-id="37102-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="37102-316">Die Verwendung dieses Abschnitts soll es Autoren von Inhalten ermöglichen, die Absicht von Inhalten an die automatische Wiedergabe zu übermitteln und die Überprüfungs Zeit zu verkürzen, indem die Überprüfung auf bestimmte wichtige Bereiche der Medien beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="37102-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="37102-317">Die folgenden Pfade sind gültig.</span><span class="sxs-lookup"><span data-stu-id="37102-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="37102-318">Der **\[ ignorecontentpath \]** -Abschnitt wird nur unter Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37102-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="37102-319">\[Schlüssel für "de viceingestall" \]</span><span class="sxs-lookup"><span data-stu-id="37102-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="37102-320">DriverPath "</span><span class="sxs-lookup"><span data-stu-id="37102-320">DriverPath</span></span>

<span data-ttu-id="37102-321">Der Eintrag **DriverPath** gibt ein Verzeichnis an, in dem rekursiv nach Treiberdateien gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="37102-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="37102-322">Dieser Befehl wird während einer Treiberinstallation verwendet und ist nicht Teil eines Autorun-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="37102-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="37102-323">Der Abschnitt " **\[ deviceingestall \]** " wird nur unter Windows XP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37102-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="37102-324">Parameter</span><span class="sxs-lookup"><span data-stu-id="37102-324">Parameters</span></span>

-   <span data-ttu-id="37102-325">*DirectoryPath*</span><span class="sxs-lookup"><span data-stu-id="37102-325">*directorypath*</span></span>

    <span data-ttu-id="37102-326">Ein Pfad zu einem Verzeichnis, in dem Windows nach Treiberdateien sucht, sowie alle zugehörigen Unterverzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="37102-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="37102-327">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37102-327">Remarks</span></span>

<span data-ttu-id="37102-328">Verwenden Sie die Laufwerk Buchstaben nicht in *Director Path* , wenn Sie von einem Computer zum nächsten wechseln.</span><span class="sxs-lookup"><span data-stu-id="37102-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="37102-329">Fügen Sie zum Durchsuchen mehrerer Verzeichnisse einen **DriverPath** -Eintrag für jedes Verzeichnis hinzu, wie in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="37102-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="37102-330">Wenn kein **DriverPath** -Eintrag im Abschnitt " **\[ deviceinstall \]** " bereitgestellt wird oder der Eintrag " **DriverPath** " keinen Wert aufweist, wird dieses Laufwerk bei der Suche nach Treiberdateien übersprungen.</span><span class="sxs-lookup"><span data-stu-id="37102-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
