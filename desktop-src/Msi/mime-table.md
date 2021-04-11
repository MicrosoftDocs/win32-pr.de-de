---
description: Die MIME-Tabelle ordnet einen MIME-Inhaltstyp einer Dateinamenerweiterung oder einer CLSID zu, um die Erweiterung oder die com-Server Informationen zu generieren, die für die Ankündigung des MIME-Inhalts (Multipurpose Internet Mail Extensions) erforderlich sind.
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: MIME-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217346"
---
# <a name="mime-table"></a><span data-ttu-id="553c2-103">MIME-Tabelle</span><span class="sxs-lookup"><span data-stu-id="553c2-103">MIME Table</span></span>

<span data-ttu-id="553c2-104">Die MIME-Tabelle ordnet einen MIME-Inhaltstyp einer Dateinamenerweiterung oder einer CLSID zu, um die Erweiterung oder die com-Server Informationen zu generieren, die für die Ankündigung des MIME-Inhalts (Multipurpose Internet Mail Extensions) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="553c2-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="553c2-105">Die MIME-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="553c2-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="553c2-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="553c2-106">Column</span></span>      | <span data-ttu-id="553c2-107">Typ</span><span class="sxs-lookup"><span data-stu-id="553c2-107">Type</span></span>             | <span data-ttu-id="553c2-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="553c2-108">Key</span></span> | <span data-ttu-id="553c2-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="553c2-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="553c2-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="553c2-110">ContentType</span></span> | [<span data-ttu-id="553c2-111">Text</span><span class="sxs-lookup"><span data-stu-id="553c2-111">Text</span></span>](text.md) | <span data-ttu-id="553c2-112">J</span><span class="sxs-lookup"><span data-stu-id="553c2-112">Y</span></span>   | <span data-ttu-id="553c2-113">N</span><span class="sxs-lookup"><span data-stu-id="553c2-113">N</span></span>        |
| <span data-ttu-id="553c2-114">Durchwahl\_</span><span class="sxs-lookup"><span data-stu-id="553c2-114">Extension\_</span></span> | [<span data-ttu-id="553c2-115">Text</span><span class="sxs-lookup"><span data-stu-id="553c2-115">Text</span></span>](text.md) | <span data-ttu-id="553c2-116">N</span><span class="sxs-lookup"><span data-stu-id="553c2-116">N</span></span>   | <span data-ttu-id="553c2-117">N</span><span class="sxs-lookup"><span data-stu-id="553c2-117">N</span></span>        |
| <span data-ttu-id="553c2-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="553c2-118">CLSID</span></span>       | [<span data-ttu-id="553c2-119">GUID</span><span class="sxs-lookup"><span data-stu-id="553c2-119">GUID</span></span>](guid.md) | <span data-ttu-id="553c2-120">N</span><span class="sxs-lookup"><span data-stu-id="553c2-120">N</span></span>   | <span data-ttu-id="553c2-121">J</span><span class="sxs-lookup"><span data-stu-id="553c2-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="553c2-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="553c2-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="553c2-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span><span class="sxs-lookup"><span data-stu-id="553c2-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="553c2-124">Diese Spalte ist ein Bezeichner für den MIME-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="553c2-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="553c2-125">Sie wird in der Regel in Form des Typs/Formats geschrieben.</span><span class="sxs-lookup"><span data-stu-id="553c2-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="553c2-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Weiterung\_</span><span class="sxs-lookup"><span data-stu-id="553c2-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="553c2-127">Diese Spalte enthält die Server Erweiterung, die dem MIME-Inhalt ohne den Punkt zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="553c2-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="553c2-128">Diese Spalte ist ein Fremdschlüssel in der [Erweiterungs Tabelle](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="553c2-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="553c2-129">Die Erweiterungs Tabelle enthält Informationen zum Dateinamen Erweiterungs Server, die als Teil der Ankündigung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="553c2-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="553c2-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="553c2-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="553c2-131">Diese Spalte enthält die com-Server-CLSID, die dem MIME-Inhalt zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="553c2-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="553c2-132">Die CLSID in dieser Spalte kann ein Fremdschlüssel in die [Klassen Tabelle](class-table.md) oder eine CLSID sein, die bereits auf dem Computer des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="553c2-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="553c2-133">Die Klassen Tabelle enthält com-Server bezogene Informationen, die als Teil der Ankündigung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="553c2-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="553c2-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="553c2-134">Remarks</span></span>

<span data-ttu-id="553c2-135">Diese Tabelle wird beim Ausführen der [registermimeinfo-Aktion](registermimeinfo-action.md) oder der [unregistermimeinfo-Aktion](unregistermimeinfo-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="553c2-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="553c2-136">Im Ankündigungs Modus werden von der registermimeinfo-Aktion alle MIME-Informationen für Server aus der MIME-Tabelle, für die das entsprechende Feature aktiviert ist, registriert.</span><span class="sxs-lookup"><span data-stu-id="553c2-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="553c2-137">Andernfalls registriert die Aktion MIME-Informationen für Server aus der MIME-Tabelle, für die die entsprechende Funktion zurzeit für die Installation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="553c2-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="553c2-138">Die [unregistermimeinfo-Aktion](unregistermimeinfo-action.md) hebt die Registrierung von MIME-bezogenen Registrierungsinformationen im System auf.</span><span class="sxs-lookup"><span data-stu-id="553c2-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="553c2-139">Die-Aktion hebt die Registrierung von MIME-Informationen für Server aus der MIME-Tabelle auf, für die die entsprechende Funktion zurzeit zur Deinstallation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="553c2-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="553c2-140">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="553c2-140">Validation</span></span>

<dl>

[<span data-ttu-id="553c2-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="553c2-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="553c2-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="553c2-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="553c2-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="553c2-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="553c2-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="553c2-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



