---
description: Das Erfassungs Datum der Datei oder des Mediums.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. dateerworbener
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218087"
---
# <a name="systemdateacquired"></a><span data-ttu-id="31aa4-103">System. dateerworbener</span><span class="sxs-lookup"><span data-stu-id="31aa4-103">System.DateAcquired</span></span>

<span data-ttu-id="31aa4-104">Das Erfassungs Datum der Datei oder des Mediums.</span><span class="sxs-lookup"><span data-stu-id="31aa4-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="31aa4-105">Diese Eigenschaft bezieht sich auf einen bestimmten Benutzer oder eine Gruppe von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="31aa4-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="31aa4-106">Diese Daten werden z. b. als Haupt Sortier Achse für den virtuellen Ordner **New Music** verwendet, der es Benutzern ermöglicht, die neuesten Ergänzungen zu Ihrer Sammlung zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="31aa4-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="31aa4-107">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="31aa4-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="31aa4-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31aa4-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="31aa4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31aa4-109">Remarks</span></span>

<span data-ttu-id="31aa4-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="31aa4-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="31aa4-111">[Dateerworbener]() wird als Wert im Hauptstream der Datei gespeichert, ist jedoch möglicherweise nicht immer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="31aa4-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="31aa4-112">In diesen Fällen kann das Erwerbsdatum auf Grundlage anderer bekannter Datumsangaben für den Inhalt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="31aa4-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="31aa4-113">Der Metadatenhandler sollte einen Satz von Regeln verwenden, um das Datum zu bestimmen, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="31aa4-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="31aa4-114">Dies wird im folgenden Beispiel für Musikdateien veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="31aa4-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="31aa4-115">Bei erworbener Musik sollte die Erstellungszeit der Datei verwendet werden, wenn kein Erstellungsdatum vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="31aa4-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="31aa4-116">Der Download Anbieter sollte jedoch die [dateerwordeeigenschaft]() in der Datei festlegen.</span><span class="sxs-lookup"><span data-stu-id="31aa4-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="31aa4-117">Bei Musikdateien, die der Benutzer oder die Gruppe "gerissen" (Kopieren von Musik oder Video von einer CD oder DVD auf eine Festplatte), sollte das Erfassungs Datum das Datum sein, an dem die Aktion stattfindet.</span><span class="sxs-lookup"><span data-stu-id="31aa4-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="31aa4-118">Beispielsweise das [WM/encodingtime-](../wmp/wm-encodingtime-attribute.md) Attribut.</span><span class="sxs-lookup"><span data-stu-id="31aa4-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="31aa4-119">Bei Musik, die von einem anderen Speicherort kopiert wurde, sollte die Erstellungszeit der Datei als Erwerbsdatum verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31aa4-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="31aa4-120">Beispiele für [System. dateerworbene]() sind das Datum und die Uhrzeit, zu denen Bilder von einer Kamera bezogen werden oder wenn Musik online erworben wird.</span><span class="sxs-lookup"><span data-stu-id="31aa4-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="31aa4-121">Dies ist nicht identisch mit [System. dateimportiert](./props-system-dateimported.md).</span><span class="sxs-lookup"><span data-stu-id="31aa4-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31aa4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31aa4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31aa4-123">propertydescription</span><span class="sxs-lookup"><span data-stu-id="31aa4-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="31aa4-124">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="31aa4-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="31aa4-125">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="31aa4-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="31aa4-126">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="31aa4-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="31aa4-127">Display Info</span><span class="sxs-lookup"><span data-stu-id="31aa4-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="31aa4-128">StringFormat</span><span class="sxs-lookup"><span data-stu-id="31aa4-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="31aa4-129">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="31aa4-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="31aa4-130">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="31aa4-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="31aa4-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="31aa4-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="31aa4-132">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="31aa4-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="31aa4-133">DrawControl</span><span class="sxs-lookup"><span data-stu-id="31aa4-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="31aa4-134">editcontrol</span><span class="sxs-lookup"><span data-stu-id="31aa4-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="31aa4-135">FilterControl</span><span class="sxs-lookup"><span data-stu-id="31aa4-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="31aa4-136">querycontrol</span><span class="sxs-lookup"><span data-stu-id="31aa4-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
