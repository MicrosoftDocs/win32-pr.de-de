---
description: Die Klassen Tabelle enthält com-Server bezogene Informationen, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile kann einen Satz von Registrierungs Schlüsseln und-Werten generieren. Die zugehörigen ProgID-Informationen sind in dieser Tabelle enthalten.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Klassen Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348339"
---
# <a name="class-table"></a><span data-ttu-id="0858c-105">Klassen Tabelle</span><span class="sxs-lookup"><span data-stu-id="0858c-105">Class Table</span></span>

<span data-ttu-id="0858c-106">Die Klassen Tabelle enthält com-Server bezogene Informationen, die als Teil der Produktankündigung generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0858c-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="0858c-107">Jede Zeile kann einen Satz von Registrierungs Schlüsseln und-Werten generieren.</span><span class="sxs-lookup"><span data-stu-id="0858c-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="0858c-108">Die zugehörigen ProgID-Informationen sind in dieser Tabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="0858c-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="0858c-109">Die Klassen Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="0858c-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="0858c-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="0858c-110">Column</span></span>           | <span data-ttu-id="0858c-111">Typ</span><span class="sxs-lookup"><span data-stu-id="0858c-111">Type</span></span>                         | <span data-ttu-id="0858c-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="0858c-112">Key</span></span> | <span data-ttu-id="0858c-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="0858c-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="0858c-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="0858c-114">CLSID</span></span>            | [<span data-ttu-id="0858c-115">GUID</span><span class="sxs-lookup"><span data-stu-id="0858c-115">GUID</span></span>](guid.md)             | <span data-ttu-id="0858c-116">J</span><span class="sxs-lookup"><span data-stu-id="0858c-116">Y</span></span>   | <span data-ttu-id="0858c-117">N</span><span class="sxs-lookup"><span data-stu-id="0858c-117">N</span></span>        |
| <span data-ttu-id="0858c-118">Kontext</span><span class="sxs-lookup"><span data-stu-id="0858c-118">Context</span></span>          | [<span data-ttu-id="0858c-119">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0858c-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="0858c-120">J</span><span class="sxs-lookup"><span data-stu-id="0858c-120">Y</span></span>   | <span data-ttu-id="0858c-121">N</span><span class="sxs-lookup"><span data-stu-id="0858c-121">N</span></span>        |
| <span data-ttu-id="0858c-122">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="0858c-122">Component\_</span></span>      | [<span data-ttu-id="0858c-123">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0858c-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="0858c-124">J</span><span class="sxs-lookup"><span data-stu-id="0858c-124">Y</span></span>   | <span data-ttu-id="0858c-125">N</span><span class="sxs-lookup"><span data-stu-id="0858c-125">N</span></span>        |
| <span data-ttu-id="0858c-126">ProgID- \_ Standard</span><span class="sxs-lookup"><span data-stu-id="0858c-126">ProgId\_Default</span></span>  | [<span data-ttu-id="0858c-127">Text</span><span class="sxs-lookup"><span data-stu-id="0858c-127">Text</span></span>](text.md)             | <span data-ttu-id="0858c-128">N</span><span class="sxs-lookup"><span data-stu-id="0858c-128">N</span></span>   | <span data-ttu-id="0858c-129">J</span><span class="sxs-lookup"><span data-stu-id="0858c-129">Y</span></span>        |
| <span data-ttu-id="0858c-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0858c-130">Description</span></span>      | [<span data-ttu-id="0858c-131">Text</span><span class="sxs-lookup"><span data-stu-id="0858c-131">Text</span></span>](text.md)             | <span data-ttu-id="0858c-132">N</span><span class="sxs-lookup"><span data-stu-id="0858c-132">N</span></span>   | <span data-ttu-id="0858c-133">J</span><span class="sxs-lookup"><span data-stu-id="0858c-133">Y</span></span>        |
| <span data-ttu-id="0858c-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="0858c-134">AppId\_</span></span>          | [<span data-ttu-id="0858c-135">GUID</span><span class="sxs-lookup"><span data-stu-id="0858c-135">GUID</span></span>](guid.md)             | <span data-ttu-id="0858c-136">N</span><span class="sxs-lookup"><span data-stu-id="0858c-136">N</span></span>   | <span data-ttu-id="0858c-137">J</span><span class="sxs-lookup"><span data-stu-id="0858c-137">Y</span></span>        |
| <span data-ttu-id="0858c-138">Filetypemask</span><span class="sxs-lookup"><span data-stu-id="0858c-138">FileTypeMask</span></span>     | [<span data-ttu-id="0858c-139">Text</span><span class="sxs-lookup"><span data-stu-id="0858c-139">Text</span></span>](text.md)             | <span data-ttu-id="0858c-140">N</span><span class="sxs-lookup"><span data-stu-id="0858c-140">N</span></span>   | <span data-ttu-id="0858c-141">J</span><span class="sxs-lookup"><span data-stu-id="0858c-141">Y</span></span>        |
| <span data-ttu-id="0858c-142">Symbol\_</span><span class="sxs-lookup"><span data-stu-id="0858c-142">Icon\_</span></span>           | [<span data-ttu-id="0858c-143">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0858c-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="0858c-144">N</span><span class="sxs-lookup"><span data-stu-id="0858c-144">N</span></span>   | <span data-ttu-id="0858c-145">J</span><span class="sxs-lookup"><span data-stu-id="0858c-145">Y</span></span>        |
| <span data-ttu-id="0858c-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="0858c-146">IconIndex</span></span>        | [<span data-ttu-id="0858c-147">Integer</span><span class="sxs-lookup"><span data-stu-id="0858c-147">Integer</span></span>](integer.md)       | <span data-ttu-id="0858c-148">N</span><span class="sxs-lookup"><span data-stu-id="0858c-148">N</span></span>   | <span data-ttu-id="0858c-149">J</span><span class="sxs-lookup"><span data-stu-id="0858c-149">Y</span></span>        |
| <span data-ttu-id="0858c-150">Definprochandler</span><span class="sxs-lookup"><span data-stu-id="0858c-150">DefInprocHandler</span></span> | [<span data-ttu-id="0858c-151">Filename</span><span class="sxs-lookup"><span data-stu-id="0858c-151">Filename</span></span>](filename.md)     | <span data-ttu-id="0858c-152">N</span><span class="sxs-lookup"><span data-stu-id="0858c-152">N</span></span>   | <span data-ttu-id="0858c-153">J</span><span class="sxs-lookup"><span data-stu-id="0858c-153">Y</span></span>        |
| <span data-ttu-id="0858c-154">Argument</span><span class="sxs-lookup"><span data-stu-id="0858c-154">Argument</span></span>         | [<span data-ttu-id="0858c-155">Großformatige</span><span class="sxs-lookup"><span data-stu-id="0858c-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="0858c-156">N</span><span class="sxs-lookup"><span data-stu-id="0858c-156">N</span></span>   | <span data-ttu-id="0858c-157">J</span><span class="sxs-lookup"><span data-stu-id="0858c-157">Y</span></span>        |
| <span data-ttu-id="0858c-158">Funktion\_</span><span class="sxs-lookup"><span data-stu-id="0858c-158">Feature\_</span></span>        | [<span data-ttu-id="0858c-159">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="0858c-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="0858c-160">N</span><span class="sxs-lookup"><span data-stu-id="0858c-160">N</span></span>   | <span data-ttu-id="0858c-161">N</span><span class="sxs-lookup"><span data-stu-id="0858c-161">N</span></span>        |
| <span data-ttu-id="0858c-162">Attribute</span><span class="sxs-lookup"><span data-stu-id="0858c-162">Attributes</span></span>       | [<span data-ttu-id="0858c-163">Integer</span><span class="sxs-lookup"><span data-stu-id="0858c-163">Integer</span></span>](integer.md)       | <span data-ttu-id="0858c-164">N</span><span class="sxs-lookup"><span data-stu-id="0858c-164">N</span></span>   | <span data-ttu-id="0858c-165">J</span><span class="sxs-lookup"><span data-stu-id="0858c-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="0858c-166">Spalten Informationen</span><span class="sxs-lookup"><span data-stu-id="0858c-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="0858c-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="0858c-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="0858c-168">Der Klassen Bezeichner (ID) eines COM-Servers.</span><span class="sxs-lookup"><span data-stu-id="0858c-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Kontext</span><span class="sxs-lookup"><span data-stu-id="0858c-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="0858c-170">Der Server Kontext für diesen Server.</span><span class="sxs-lookup"><span data-stu-id="0858c-170">The server context for this server.</span></span> <span data-ttu-id="0858c-171">Geben Sie einen der folgenden Werte für den CLSID-Schlüssel ein.</span><span class="sxs-lookup"><span data-stu-id="0858c-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="0858c-172">CLSID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="0858c-172">CLSID KEY</span></span>                             | <span data-ttu-id="0858c-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0858c-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="0858c-174">LocalServer</span><span class="sxs-lookup"><span data-stu-id="0858c-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="0858c-175">Gibt den vollständigen Pfad zu einer 16-Bit-Anwendung für den lokalen Server an.</span><span class="sxs-lookup"><span data-stu-id="0858c-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="0858c-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="0858c-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="0858c-177">Gibt den vollständigen Pfad zu einer lokalen 32-Bit-Serveranwendung an.</span><span class="sxs-lookup"><span data-stu-id="0858c-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="0858c-178">InprocServer</span><span class="sxs-lookup"><span data-stu-id="0858c-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="0858c-179">Gibt den Pfad zu einer Prozess internen Server-DLL an.</span><span class="sxs-lookup"><span data-stu-id="0858c-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="0858c-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="0858c-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="0858c-181">Gibt den Pfad zu einem in-Process-32-Bit-Server und dem Threading Modell an.</span><span class="sxs-lookup"><span data-stu-id="0858c-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0858c-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="0858c-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="0858c-183">Externer Schlüssel in der [Komponenten Tabelle](component-table.md) , der die Komponente angibt, deren Schlüsseldatei den com-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0858c-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgID- \_ Standard</span><span class="sxs-lookup"><span data-stu-id="0858c-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="0858c-185">Die standardmäßige Programm-ID, die dieser Klassen-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0858c-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="0858c-186">Diese Spalte ist ein Fremdschlüssel in der [ProgID-Tabelle](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="0858c-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0858c-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0858c-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="0858c-188">Lokalisierte Beschreibung, die der Klassen-ID und Programm-ID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0858c-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppID\_</span><span class="sxs-lookup"><span data-stu-id="0858c-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="0858c-190">Anwendungs-ID mit DCOM-Informationen für die zugeordnete Anwendung (Zeichen folgen- [GUID](guid.md)).</span><span class="sxs-lookup"><span data-stu-id="0858c-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="0858c-191">Diese Spalte ist ein Fremdschlüssel in die [AppID-Tabelle](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="0858c-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0858c-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>Filetypemask</span><span class="sxs-lookup"><span data-stu-id="0858c-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="0858c-193">Enthält Informationen für den Schlüssel HKCR (this CLSID).</span><span class="sxs-lookup"><span data-stu-id="0858c-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="0858c-194">Wenn mehrere Muster vorhanden sind, müssen Sie durch ein Semikolon getrennt werden, und es werden numerische Unterschlüssel generiert: 0, 1, 2... Weitere Informationen zu dieser Funktionalität finden Sie unter [**getclassfile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span><span class="sxs-lookup"><span data-stu-id="0858c-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="0858c-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Angezeigt\_</span><span class="sxs-lookup"><span data-stu-id="0858c-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="0858c-196">Die Datei, die das Symbol bereitstellt, das dieser CLSID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0858c-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="0858c-197">Das Installationsprogramm schreibt den Eintrag in dieser Spalte unter den der ProgID zugeordneten DefaultIcon-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0858c-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="0858c-198">Wenn er nicht NULL ist, ist die Spalte ein Fremdschlüssel in der [Symboltabelle](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="0858c-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="0858c-199">Wenn er NULL ist, stellt der com-Server die Symbol Ressource bereit.</span><span class="sxs-lookup"><span data-stu-id="0858c-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="0858c-200">Bei angekündigten Dateizuordnungen und Verknüpfungen ist in dieser Spalte ein Wert ungleich NULL erforderlich, um ordnungsgemäß angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="0858c-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="0858c-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="0858c-202">Symbol Index in der Symbol Datei.</span><span class="sxs-lookup"><span data-stu-id="0858c-202">Icon index into the icon file.</span></span> <span data-ttu-id="0858c-203">Diese kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0858c-203">This can be null.</span></span>

<span data-ttu-id="0858c-204">Nur nicht negative Zahlen.</span><span class="sxs-lookup"><span data-stu-id="0858c-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>Definprochandler</span><span class="sxs-lookup"><span data-stu-id="0858c-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="0858c-206">Dieses Feld gibt den in-Process-Standard Handler für den Server Kontext an, der im Kontext Feld angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0858c-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="0858c-207">Dieses Feld muss NULL sein, wenn ein InprocServer-oder InprocServer-CLSID-Schlüssel im Kontext Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0858c-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="0858c-208">Wenn ein LocalServer-oder LocalServer32 CLSID-Schlüssel im Kontext Feld angezeigt wird, identifiziert der Wert im Feld definprochandler den standardmäßigen Prozess internen Handler.</span><span class="sxs-lookup"><span data-stu-id="0858c-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="0858c-209">Wert</span><span class="sxs-lookup"><span data-stu-id="0858c-209">Value</span></span>                | <span data-ttu-id="0858c-210">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0858c-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0858c-211">nicht numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="0858c-211">non-numeric value</span></span>    | <span data-ttu-id="0858c-212">Das Installationsprogramm behandelt einen nicht numerischen Wert im Feld definprochandler als Systemdatei, die als 32-Bit-Prozess interne, in-Process-Handler, der durch den InprocHandler32-Schlüssel angegeben ist, fungiert.</span><span class="sxs-lookup"><span data-stu-id="0858c-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="0858c-213">Null</span><span class="sxs-lookup"><span data-stu-id="0858c-213">Null</span></span>                 | <span data-ttu-id="0858c-214">Die Felder "definprochandler" und "Argument" können für einen LocalServer-oder LocalServer32 CLSID-Schlüssel NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0858c-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="0858c-215">1 = Standard (System)</span><span class="sxs-lookup"><span data-stu-id="0858c-215">1 = default (system)</span></span> | <span data-ttu-id="0858c-216">Der Standardwert ist der von InprocHandler angegebene 16-Bit-in-Process-Handler.</span><span class="sxs-lookup"><span data-stu-id="0858c-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="0858c-217">In diesem Fall ist der Wert von InprocHandler der Name in der Registrierung, mit dem der Wert des in-Process-Standard Handlers gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0858c-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="0858c-218">Beispiel: HKEY- \_ \_ Software Klassen für lokale Computer \\ \\ \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="0858c-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="0858c-219">2 = Standard (System)</span><span class="sxs-lookup"><span data-stu-id="0858c-219">2 = default (system)</span></span> | <span data-ttu-id="0858c-220">Der Standardwert ist der 32-Bit-in-Process-Handler, der durch InprocHandler32 angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0858c-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="0858c-221">In diesem Fall ist der Wert von InprocHandler32 der Name in der Registrierung, mit dem der Wert des in-Process-Standard Handlers gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="0858c-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="0858c-222">Beispiel: HKEY- \_ \_ Software Klassen für lokale Computer \\ \\ \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="0858c-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="0858c-223">3 = Standard (System)</span><span class="sxs-lookup"><span data-stu-id="0858c-223">3 = default (system)</span></span> | <span data-ttu-id="0858c-224">Der Standardwert ist ein in-Process-Handler mit 16-Bit-oder 32-Bit-Prozess.</span><span class="sxs-lookup"><span data-stu-id="0858c-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="0858c-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Gestritten</span><span class="sxs-lookup"><span data-stu-id="0858c-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="0858c-226">Wenn ein LocalServer-oder LocalServer32 CLSID-Schlüssel im Kontext Feld angezeigt wird, wird der Text in diesem Feld als Argument für den Server registriert und von com zum Aufrufen des Servers verwendet.</span><span class="sxs-lookup"><span data-stu-id="0858c-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="0858c-227">Die Felder "definprochandler" und "Argument" können NULL sein, wenn "LocalServer" oder "localserver32" im Kontext Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0858c-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="0858c-228">Beachten Sie, dass die Auflösung von Eigenschaften im Feld Argument eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="0858c-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="0858c-229">Eine Eigenschaft, die als \[ Eigenschaft \] in diesem Feld formatiert ist, kann nur aufgelöst werden, wenn die Eigenschaft bereits den vorgesehenen Wert aufweist, wenn die Komponente, die die Klasse besitzt, installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0858c-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="0858c-230">Damit das Argument "MyDoc.doc" z. b. \[ \# \] in den richtigen Wert aufgelöst wird, muss der gleiche Prozess die Datei MyDoc.doc und die Komponente installieren, die die Klasse besitzt.</span><span class="sxs-lookup"><span data-stu-id="0858c-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_</span><span class="sxs-lookup"><span data-stu-id="0858c-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="0858c-232">Externer Schlüssel in der [Featuretabelle](feature-table.md) , der die Funktion angibt, die den com-Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0858c-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="0858c-233">Externer Schlüssel für Spalte einer der featuretabellen.</span><span class="sxs-lookup"><span data-stu-id="0858c-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="0858c-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt</span><span class="sxs-lookup"><span data-stu-id="0858c-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="0858c-235">Wenn in dieser Spalte " **msidbClassAttributesRelativePath** " festgelegt ist, kann der Bare-Dateiname für com-Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0858c-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="0858c-236">Der Dateiname wird nur von dem Installer anstelle des gesamten Pfads registriert.</span><span class="sxs-lookup"><span data-stu-id="0858c-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="0858c-237">Dadurch kann der Server im aktuellen Verzeichnis Vorrang haben und mehrere Kopien derselben Komponente zulassen.</span><span class="sxs-lookup"><span data-stu-id="0858c-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="0858c-238">Attribut</span><span class="sxs-lookup"><span data-stu-id="0858c-238">Attribute</span></span>                            | <span data-ttu-id="0858c-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="0858c-239">Decimal</span></span> | <span data-ttu-id="0858c-240">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="0858c-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="0858c-241">**msidbClassAttributesRelativePath**</span><span class="sxs-lookup"><span data-stu-id="0858c-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="0858c-242">1</span><span class="sxs-lookup"><span data-stu-id="0858c-242">1</span></span>       | <span data-ttu-id="0858c-243">0x001</span><span class="sxs-lookup"><span data-stu-id="0858c-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0858c-244">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0858c-244">Remarks</span></span>

<span data-ttu-id="0858c-245">Diese Tabelle wird beim Ausführen der [RegisterClassInfo-Aktion](registerclassinfo-action.md) oder der [unregisterclassinfo-Aktion](unregisterclassinfo-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0858c-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="0858c-246">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="0858c-246">Validation</span></span>

<dl>

[<span data-ttu-id="0858c-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="0858c-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0858c-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="0858c-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0858c-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="0858c-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="0858c-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="0858c-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0858c-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="0858c-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="0858c-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="0858c-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="0858c-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="0858c-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="0858c-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="0858c-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="0858c-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="0858c-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="0858c-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="0858c-256">ICE69</span></span>](ice69.md)  
</dl>

 

 
