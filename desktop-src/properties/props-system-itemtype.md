---
description: Der kanonische Typ des Elements.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218076"
---
# <a name="systemitemtype"></a><span data-ttu-id="6f1fc-103">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="6f1fc-103">System.ItemType</span></span>

<span data-ttu-id="6f1fc-104">Der kanonische Typ des Elements.</span><span class="sxs-lookup"><span data-stu-id="6f1fc-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6f1fc-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f1fc-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6f1fc-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f1fc-106">Remarks</span></span>

<span data-ttu-id="6f1fc-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="6f1fc-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="6f1fc-108">Der Wert für System. ItemType soll Programm gesteuert analysiert werden und kann wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="6f1fc-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="6f1fc-109">Eine Dateierweiterung, die auf einen ProgID-Wert (HKEY \_ Classes \_ root) verweist, \\ <ProgID> der den anzeigen Amen für den Typ enthält.</span><span class="sxs-lookup"><span data-stu-id="6f1fc-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="6f1fc-110">Ein ProgID-Wert (HKEY \_ Classes \_ rroot \\ <ProgID> ), der den anzeigen Amen für den Typ enthält.</span><span class="sxs-lookup"><span data-stu-id="6f1fc-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="6f1fc-111">Das friendlytykename-Element einer ProgID sollte eine lokalisierte Version des Anwendungs namens ( @winword.dll ,-42) sein, während der Standardwert des ProgID-Schlüssels ein nicht lokalisierter Name ist (Word.Doc-enument. 12).</span><span class="sxs-lookup"><span data-stu-id="6f1fc-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="6f1fc-112">Wenn kein kanonischer Typ vorhanden ist, ist der Wert VT \_ empty.</span><span class="sxs-lookup"><span data-stu-id="6f1fc-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="6f1fc-113">Wenn es sich bei dem Element um eine Datei handelt ([System. filename](./props-system-filename.md) ist nicht "VT \_ empty"), ist der Wert identisch mit der Datei " [System. FileExtension](./props-system-fileextension.md)".</span><span class="sxs-lookup"><span data-stu-id="6f1fc-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="6f1fc-114">Verwenden Sie [System. itemtypetext](./props-system-itemtypetext.md) , wenn Sie den Typ für Endbenutzer in einer Ansicht anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="6f1fc-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="6f1fc-115">Wenn es sich bei dem Element um eine Datei handelt, führt die Übergabe des [System. ItemType]() -Werts an [**psformatfordisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) zum gleichen Wert wie [System. itemtypetext](./props-system-itemtypetext.md).</span><span class="sxs-lookup"><span data-stu-id="6f1fc-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="6f1fc-116">Beispielwerte:</span><span class="sxs-lookup"><span data-stu-id="6f1fc-116">Example values:</span></span>



| <span data-ttu-id="6f1fc-117">Pfad</span><span class="sxs-lookup"><span data-stu-id="6f1fc-117">Path</span></span>                                   | <span data-ttu-id="6f1fc-118">ItemType</span><span class="sxs-lookup"><span data-stu-id="6f1fc-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="6f1fc-119">c: \\ "MyDir"- \\ Leiste \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="6f1fc-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="6f1fc-120">.txt</span><span class="sxs-lookup"><span data-stu-id="6f1fc-120">.txt</span></span>             |
| <span data-ttu-id="6f1fc-121">\\\\Server \\ Freigabe \\ "MyDir" \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="6f1fc-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="6f1fc-122">.doc</span><span class="sxs-lookup"><span data-stu-id="6f1fc-122">.doc</span></span>             |
| <span data-ttu-id="6f1fc-123">\\\\Server \\ Freigabe \\ Ordner</span><span class="sxs-lookup"><span data-stu-id="6f1fc-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="6f1fc-124">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="6f1fc-124">Directory</span></span>        |
| <span data-ttu-id="6f1fc-125">c: \\ mydir \\ meinOrdner</span><span class="sxs-lookup"><span data-stu-id="6f1fc-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="6f1fc-126">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="6f1fc-126">Directory</span></span>        |
| <span data-ttu-id="6f1fc-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f1fc-127">\[desktop\]</span></span>                            | <span data-ttu-id="6f1fc-128">Ordner</span><span class="sxs-lookup"><span data-stu-id="6f1fc-128">Folder</span></span>           |
| <span data-ttu-id="6f1fc-129">/Mailbox Account/Inbox/"Re: Hello!"</span><span class="sxs-lookup"><span data-stu-id="6f1fc-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="6f1fc-130">MAPI/IPM. Nachricht</span><span class="sxs-lookup"><span data-stu-id="6f1fc-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6f1fc-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f1fc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f1fc-132">propertydescription</span><span class="sxs-lookup"><span data-stu-id="6f1fc-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-133">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="6f1fc-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-134">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="6f1fc-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-135">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="6f1fc-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-136">Display Info</span><span class="sxs-lookup"><span data-stu-id="6f1fc-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-137">StringFormat</span><span class="sxs-lookup"><span data-stu-id="6f1fc-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-138">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="6f1fc-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-139">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="6f1fc-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6f1fc-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-141">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="6f1fc-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-142">DrawControl</span><span class="sxs-lookup"><span data-stu-id="6f1fc-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-143">editcontrol</span><span class="sxs-lookup"><span data-stu-id="6f1fc-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-144">FilterControl</span><span class="sxs-lookup"><span data-stu-id="6f1fc-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-145">querycontrol</span><span class="sxs-lookup"><span data-stu-id="6f1fc-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="6f1fc-146">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="6f1fc-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
