---
description: Der Anzeige Name in &\# 0034; die meisten&\# 0034;-Formular.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753112"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="d7b30-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="d7b30-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="d7b30-104">Der Anzeige Name im Formular "ganz fertig".</span><span class="sxs-lookup"><span data-stu-id="d7b30-104">The display name in "most complete" form.</span></span> <span data-ttu-id="d7b30-105">Dabei handelt es sich um die eindeutige Darstellung des Element namens, der für Endbenutzer am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d7b30-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="d7b30-106">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7b30-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="d7b30-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7b30-107">Remarks</span></span>

<span data-ttu-id="d7b30-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="d7b30-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="d7b30-109">Dieser Wert ist die verkettierung von [System. itemnameprefix](./props-system-itemnameprefix.md) und [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="d7b30-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="d7b30-110">Wenn es sich bei dem Element um eine Datei handelt, enthält diese Eigenschaft den anzeigen Amen, wie im Datei-Explorer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7b30-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="d7b30-111">Es gibt akzeptable Fälle, in denen [System. filename](./props-system-filename.md) angegeben ist, der Wert dieser Eigenschaft jedoch vollständig anders ist.</span><span class="sxs-lookup"><span data-stu-id="d7b30-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="d7b30-112">E-Mail-Nachrichten sind ein gutes Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d7b30-112">E-mail messages are a good example.</span></span> <span data-ttu-id="d7b30-113">Handelt es sich bei dem Element um eine e-Mail-Nachricht, ist der Elementname normalerweise der Betreff.</span><span class="sxs-lookup"><span data-stu-id="d7b30-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="d7b30-114">In diesem Fall muss der Wert die Verkettung von [System. itemnameprefix](./props-system-itemnameprefix.md) und [System. ItemName](./props-system-itemname.md)sein.</span><span class="sxs-lookup"><span data-stu-id="d7b30-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="d7b30-115">Da der Wert von System. itemnameprefix alle nachfolgenden Leerzeichen ausschließt, muss die Verkettung ein Leerzeichen enthalten, wenn [System. itemnamedisplay]()erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b30-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="d7b30-116">Beachten Sie, dass diese Eigenschaft nicht unbedingt eindeutig ist, sondern so konzipiert ist, dass Sie den wahrscheinlichsten Kandidaten herauf Stufen kann, der eindeutig sein kann und für Endbenutzer sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="d7b30-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="d7b30-117">Für Dokumente könnte z [. b. System. Title](./props-system-title.md) als [System. itemnamedisplay]()verwendet werden. in der Praxis ist der Titel der Dokumente jedoch möglicherweise nicht nützlich oder eindeutig genug, um als alleinige System. itemnamedisplay-Funktion zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="d7b30-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="d7b30-118">Stattdessen ist die Angabe von " [System. filename](./props-system-filename.md) " als Wert von "System. itemnamedisplay" eine bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="d7b30-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="d7b30-119">In Windows Mail wird e-Mail als EML-Dateien im Dateisystem gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d7b30-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="d7b30-120">Die System. filename-Werte für diese Dateien sind nicht Menschen freundlich, da Sie GUIDs sind.</span><span class="sxs-lookup"><span data-stu-id="d7b30-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="d7b30-121">In diesem Beispiel ist die herauf Stufung von [System. Subject](./props-system-subject.md) als System. itemnamedisplay sinnvoller.</span><span class="sxs-lookup"><span data-stu-id="d7b30-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="d7b30-122">**Kompatibilitäts Hinweise:**</span><span class="sxs-lookup"><span data-stu-id="d7b30-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="d7b30-123">Shell-Ordner Implementierungen unter Windows Vista: Verwenden Sie "pkey \_ itemnamedisplay" für die Spalte "Name", wenn Sie möchten, dass Windows-Explorer [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(shgdn \_ Normal) aufruft, um den Wert des Namens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7b30-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="d7b30-124">Verwenden Sie einen anderen pkey (z. b. pkey \_ ItemName), wenn Sie möchten, dass Windows-Explorer entweder den Eigenschaften Speicher des Ordners oder [**IShellFolder2:: getdetailsex**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) aufruft, um den Wert des Namens abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7b30-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="d7b30-125">Shell-Ordner Implementierungen unter Windows XP: die erste Spalte muss die Namensspalte sein, und Windows Explorer ruft [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) auf, um den Wert des Namens zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d7b30-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="d7b30-126">Pkey/scid ist unerheblich.</span><span class="sxs-lookup"><span data-stu-id="d7b30-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="d7b30-127">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="d7b30-127">Item type</span></span>     | <span data-ttu-id="d7b30-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d7b30-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="d7b30-129">File</span><span class="sxs-lookup"><span data-stu-id="d7b30-129">File</span></span>          | <span data-ttu-id="d7b30-130">hello.txt</span><span class="sxs-lookup"><span data-stu-id="d7b30-130">hello.txt</span></span>                 |
| <span data-ttu-id="d7b30-131">`Message`</span><span class="sxs-lookup"><span data-stu-id="d7b30-131">Message</span></span>       | <span data-ttu-id="d7b30-132">Neu: wo ist das Meeting?</span><span class="sxs-lookup"><span data-stu-id="d7b30-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="d7b30-133">Geräte Ordner</span><span class="sxs-lookup"><span data-stu-id="d7b30-133">Device folder</span></span> | <span data-ttu-id="d7b30-134">"Song. wma"</span><span class="sxs-lookup"><span data-stu-id="d7b30-134">song.wma</span></span>                  |
| <span data-ttu-id="d7b30-135">Ordner</span><span class="sxs-lookup"><span data-stu-id="d7b30-135">Folder</span></span>        | <span data-ttu-id="d7b30-136">Dokumente</span><span class="sxs-lookup"><span data-stu-id="d7b30-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="d7b30-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7b30-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b30-138">propertydescription</span><span class="sxs-lookup"><span data-stu-id="d7b30-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d7b30-139">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="d7b30-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d7b30-140">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="d7b30-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d7b30-141">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="d7b30-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d7b30-142">Display Info</span><span class="sxs-lookup"><span data-stu-id="d7b30-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d7b30-143">StringFormat</span><span class="sxs-lookup"><span data-stu-id="d7b30-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d7b30-144">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="d7b30-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d7b30-145">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="d7b30-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d7b30-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d7b30-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d7b30-147">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="d7b30-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d7b30-148">DrawControl</span><span class="sxs-lookup"><span data-stu-id="d7b30-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d7b30-149">editcontrol</span><span class="sxs-lookup"><span data-stu-id="d7b30-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d7b30-150">FilterControl</span><span class="sxs-lookup"><span data-stu-id="d7b30-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d7b30-151">querycontrol</span><span class="sxs-lookup"><span data-stu-id="d7b30-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
