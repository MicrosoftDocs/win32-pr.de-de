---
description: Bei Windows Vista wurde die Elementstruktur der Windows-Abbild Beschaffung (WIA) erheblich geändert.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: Informationen zur IWiaItem2-Elementstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865256"
---
# <a name="about-the-iwiaitem2-item-tree"></a><span data-ttu-id="49d11-103">Informationen zur IWiaItem2-Elementstruktur</span><span class="sxs-lookup"><span data-stu-id="49d11-103">About the IWiaItem2 Item Tree</span></span>

<span data-ttu-id="49d11-104">Bei Windows Vista wurde die Elementstruktur der Windows-Abbild Beschaffung (WIA) erheblich geändert.</span><span class="sxs-lookup"><span data-stu-id="49d11-104">With Windows Vista, the Windows Image Acquisition (WIA) item tree has changed significantly.</span></span> <span data-ttu-id="49d11-105">[**IWiaItem2**](-wia-iwiaitem2.md) Items werden verwendet, um Geräte Attribute und Gerätedaten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="49d11-105">[**IWiaItem2**](-wia-iwiaitem2.md) items are used to represent device attributes and device data.</span></span> <span data-ttu-id="49d11-106">Abbild Erstellungs Anwendungen sehen ein Windows-Abbild Erfassungsgerät (WIA) 2,0 als hierarchische Struktur von Elementen, wobei das Stamm Element das eigentliche Gerät und die untergeordneten Elemente darstellt, die Elemente wie programmierbare Datenquellen, Bilder oder Ordner darstellen, die Bilder enthalten.</span><span class="sxs-lookup"><span data-stu-id="49d11-106">Imaging applications see a Windows Image Acquisition (WIA) 2.0 device as a hierarchical tree of items, with the root item representing the device itself and the child items representing things like programmable data sources, images, or folders that contain images.</span></span>

-   [<span data-ttu-id="49d11-107">Anwendungs Elemente</span><span class="sxs-lookup"><span data-stu-id="49d11-107">Application Items</span></span>](#application-items)
-   [<span data-ttu-id="49d11-108">Elementflags</span><span class="sxs-lookup"><span data-stu-id="49d11-108">Item Flags</span></span>](#item-flags)
-   [<span data-ttu-id="49d11-109">Element Kategorien</span><span class="sxs-lookup"><span data-stu-id="49d11-109">Item Categories</span></span>](#item-categories)
-   [<span data-ttu-id="49d11-110">Stamm Element</span><span class="sxs-lookup"><span data-stu-id="49d11-110">Root Item</span></span>](#root-item)
-   [<span data-ttu-id="49d11-111">Datenelement</span><span class="sxs-lookup"><span data-stu-id="49d11-111">Data Item</span></span>](#data-item)
-   [<span data-ttu-id="49d11-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49d11-112">Related topics</span></span>](#related-topics)

## <a name="application-items"></a><span data-ttu-id="49d11-113">Anwendungs Elemente</span><span class="sxs-lookup"><span data-stu-id="49d11-113">Application Items</span></span>

<span data-ttu-id="49d11-114">Die WIA 2,0-Elementstruktur, die eine Anwendung sehen kann, ist getrennt von der Struktur, die von einem WIA 2,0 Minidriver erstellt und verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="49d11-114">The WIA 2.0 item tree that an application can see is separate from the tree created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="49d11-115">Wenn ein Mini Treiber eine Struktur erstellt, verwendet der WIA 2,0-Dienst diese WIA 2,0-Elementstruktur als Leitfaden, um eine Kopie der Struktur zu erstellen, die von Abbild Erstellungs Anwendungen angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="49d11-115">When a minidriver creates a tree, the WIA 2.0 service uses this WIA 2.0 item tree as a guide to create a copy of the tree that can be viewed by imaging applications.</span></span> <span data-ttu-id="49d11-116">Elemente in der kopierten Struktur werden als *Anwendungs* Elemente bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49d11-116">Items in the copied tree are called *application* items.</span></span> <span data-ttu-id="49d11-117">Elemente in der Struktur, die von einem Mini Treiber erstellt werden, werden als *Treiber* Elemente bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="49d11-117">Items in the tree created by a minidriver are called *driver* items.</span></span>

<span data-ttu-id="49d11-118">Ein WIA-Element kann eine programmierbare Datenquelle für die Dokument-oder Daten eines Scanners darstellen, die auf diesem Gerät gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="49d11-118">A WIA item can represent a programmable data source for a scanner's document feeder or the data stored on that device.</span></span> <span data-ttu-id="49d11-119">Ein WIA-Gerät sollte in einzelne Elemente unterteilt werden, die verschiedene Daten beschreiben, die von diesem Gerät erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-119">A WIA device should be divided into individual items that describe different data produced by that device.</span></span>

<span data-ttu-id="49d11-120">Beispielsweise kann ein WIA-Scanner, der sowohl die Überprüfung des Flatbed als auch das Scannen von Dokumenten Scans unterstützt, unterteilt werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-120">For example, a WIA scanner that supports both flatbed scanning and document feeder scanning might be divided into two child items.</span></span> <span data-ttu-id="49d11-121">Eine stellt die Überprüfungs Funktion für Flat-Scans dar, und die andere stellt die Scanfunktion für die Dokument Prüfung dar.</span><span class="sxs-lookup"><span data-stu-id="49d11-121">One represents the flatbed scanning functionality and the other represents the document feeder scanning functionality.</span></span>

<span data-ttu-id="49d11-122">Mehrere Abbilder, die auf einem flachen Scanner angeordnet und gleichzeitig gescannt werden, können in einem einzigen Ordner abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-122">Multiple images laid out on a flatbed scanner and scanned at the same time can be placed in one folder.</span></span> <span data-ttu-id="49d11-123">Mithilfe des Segmentierungs Filters ([**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md)) kann jedes Bild oder jede Unterregion als untergeordnetes Element des Ordners erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-123">Using the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), each image or subregion can then be created as a child item of the folder.</span></span>

<span data-ttu-id="49d11-124">Die WIA-Struktur für ein Kamera Gerät, das Fotos speichert ("Film"), kann in Elemente aufgeteilt werden, die Ordner, Unterordner und Fotos darstellen.</span><span class="sxs-lookup"><span data-stu-id="49d11-124">The WIA tree for a camera device that stores photos ("Film") can be divided into items that represent folders, subfolders, and photos.</span></span>

## <a name="item-flags"></a><span data-ttu-id="49d11-125">Elementflags</span><span class="sxs-lookup"><span data-stu-id="49d11-125">Item Flags</span></span>

<span data-ttu-id="49d11-126">WIA-elementflags helfen, den Inhalt oder das unterstützte Verhalten eines bestimmten WIA-Elements zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="49d11-126">WIA item flags help classify the content or supported behavior of a particular WIA item.</span></span> <span data-ttu-id="49d11-127">WIA-elementflags fallen in zwei Gruppen.</span><span class="sxs-lookup"><span data-stu-id="49d11-127">WIA item flags fall into two groups.</span></span>

1.  <span data-ttu-id="49d11-128">Elementstatusflags melden den aktuellen Status des WIA-Elements, z. b. [**wiaitemtypegetrennte**](-wia-wia-item-type-flags.md), **wiaitemtypedeleted** usw.</span><span class="sxs-lookup"><span data-stu-id="49d11-128">Item status flags report the current state of the WIA item, for example, [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, and so forth.</span></span>
2.  <span data-ttu-id="49d11-129">Elementdaten Darstellung/nutzungsflags melden die Daten, die das WIA-Element darstellt oder bei der Übertragung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="49d11-129">Item data representation/usage flags report the data that the WIA item represents or can produce if transferred.</span></span> <span data-ttu-id="49d11-130">[**Wiaitemtypeimage**](-wia-wia-item-type-flags.md) ist beispielsweise ein Daten Darstellungs Flag, das der Anwendung mitteilt, dass die Daten, die dem aktuellen WIA-Element zugeordnet sind, Bilddaten sind und über Bild Daten Eigenschaften verfügen sollen.</span><span class="sxs-lookup"><span data-stu-id="49d11-130">For example, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) is a data representation flag that tells the application the data associated with the current WIA item is image data and should have image data properties.</span></span> <span data-ttu-id="49d11-131">**WIA \_ IPA \_ - \_ elementflags** ist ein Element für die Element Verwendung, das der Anwendung mitteilt, dass das WIA-Element konfigurierbar ist und einem Satz vordefinierter Konfigurations Regeln entsprechend der [**WIA \_ IPA- \_ Element \_ Kategorie**](-wia-wiaitempropcommonitem.md) folgt und dass die Konfiguration das Ergebnis für jede Datenübertragung möglicherweise ändern kann.</span><span class="sxs-lookup"><span data-stu-id="49d11-131">**WIA\_IPA\_ITEM\_FLAGS** is an item usage flag that tells the application that the WIA item is configurable and follows a set of predefined configuration rules based on the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) and that the configuration can possibly change the result for each data transfer.</span></span> <span data-ttu-id="49d11-132">(Weitere Informationen zu Kategoriedefinitionen finden [Sie Unterelement Kategorien](#item-categories) Element Kategorien.)</span><span class="sxs-lookup"><span data-stu-id="49d11-132">(For more information about category definitions, see [Item Categories](#item-categories) item categories.)</span></span>

<span data-ttu-id="49d11-133">Die folgende Abbildung zeigt ein Beispiel für eine WIA-Elementstruktur und die verschiedenen Flags, die jedem Element zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="49d11-133">The following graphic shows an example of a WIA item tree and the various flags that might be associated with each item.</span></span>

![Beispiele für elementflags für Elemente in einer Struktur](images/scannertree1.jpg)

## <a name="item-categories"></a><span data-ttu-id="49d11-135">Element Kategorien</span><span class="sxs-lookup"><span data-stu-id="49d11-135">Item Categories</span></span>

<span data-ttu-id="49d11-136">WIA-Elemente werden mithilfe der [**WIA \_ IPA \_ Element \_ Category**](-wia-wiaitempropcommonitem.md) -Eigenschaftswerte in Kategorien gruppiert.</span><span class="sxs-lookup"><span data-stu-id="49d11-136">WIA items are grouped into categories using the [**WIA\_IPA\_ITEM\_CATEGORY**](-wia-wiaitempropcommonitem.md) property values.</span></span> <span data-ttu-id="49d11-137">Diese Kategorien definieren, wie ein WIA-Element behandelt oder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49d11-137">These categories define how a WIA item is to be treated or used.</span></span> <span data-ttu-id="49d11-138">Wenn das Element z. b. eine fertige Datei (die \_ Datei mit der Kategorie ist \_ abgeschlossen \_ ) darstellt, sollte eine WIA-Anwendung davon ausgehen, dass die Daten statisch sind und sich auf dem Gerät befinden.</span><span class="sxs-lookup"><span data-stu-id="49d11-138">For example, if the item represents a finished file (WIA\_CATEGORY\_FINISHED\_FILE), a WIA application should assume that the data is static and located on the device.</span></span> <span data-ttu-id="49d11-139">Wenn das Element einen feedvorgang (WIA \_ Category \_ Feeder) darstellt, sollte die Anwendung erwarten, dass Sie die erforderlichen Eigenschaften für die Dokument feederstellung enthält und wie eine Dokument-feederstellung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="49d11-139">If the item represents a feeder (WIA\_CATEGORY\_FEEDER), the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span>

<span data-ttu-id="49d11-140">Die von WIA definierten Kategorien lauten:</span><span class="sxs-lookup"><span data-stu-id="49d11-140">The categories defined by WIA are:</span></span>

-   <span data-ttu-id="49d11-141">Automatische WIA- \_ Kategorie \_</span><span class="sxs-lookup"><span data-stu-id="49d11-141">WIA\_CATEGORY\_AUTO</span></span>
-   <span data-ttu-id="49d11-142">Kategorie- \_ \_ Feeder WIA</span><span class="sxs-lookup"><span data-stu-id="49d11-142">WIA\_CATEGORY\_FEEDER</span></span>
-   <span data-ttu-id="49d11-143">Film der Kategorie "WIA" \_ \_</span><span class="sxs-lookup"><span data-stu-id="49d11-143">WIA\_CATEGORY\_FILM</span></span>
-   <span data-ttu-id="49d11-144">Datei der WIA- \_ Kategorie \_ abgeschlossen \_</span><span class="sxs-lookup"><span data-stu-id="49d11-144">WIA\_CATEGORY\_FINISHED\_FILE</span></span>
-   <span data-ttu-id="49d11-145">WIA- \_ Kategorie \_</span><span class="sxs-lookup"><span data-stu-id="49d11-145">WIA\_CATEGORY\_FLATBED</span></span>

<span data-ttu-id="49d11-146">Beispielsweise kann für das Element des Typs für einen Scanner die [**WIA \_ IPA \_ - \_ elementflags**](-wia-wiaitempropcommonitem.md) auf [**wiaitemtypeimage**](-wia-wia-item-type-flags.md), **wiaitemtypetransfer** und **wiaitemtypeprogrammiabledatasource** festgelegt werden, und die **WIA \_ IPA \_ Item \_ Category** -Eigenschaft ist auf die WIA-Kategorie "vereinfacht" festgelegt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="49d11-146">For example, a scanner's flatbed item may have the [**WIA\_IPA\_ITEM\_FLAGS**](-wia-wiaitempropcommonitem.md) set to [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer**, and **WiaItemTypeProgrammableDataSource**, and the **WIA\_IPA\_ITEM\_CATEGORY** property set to WIA\_CATEGORY\_FLATBED.</span></span>

<span data-ttu-id="49d11-147">Die folgende Tabelle zeigt die WIA-kategoriengruppierung mit elementflags und WIA-Elementen.</span><span class="sxs-lookup"><span data-stu-id="49d11-147">The following table shows WIA category grouping with item flags and WIA items.</span></span> <span data-ttu-id="49d11-148">Diese Tabelle enthält keine vollständige Liste der WIA-elementflags, die von WIA definiert werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-148">This table does not include a full list of the WIA item flags defined by WIA.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49d11-149">WIA-Kategorie</span><span class="sxs-lookup"><span data-stu-id="49d11-149">WIA Category</span></span></th>
<th><span data-ttu-id="49d11-150">Gültige WIA-elementflags</span><span class="sxs-lookup"><span data-stu-id="49d11-150">Valid WIA Item Flags</span></span></th>
<th><span data-ttu-id="49d11-151">WIA-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="49d11-151">WIA Property Set</span></span></th>
<th><span data-ttu-id="49d11-152">WIA-Elemente</span><span class="sxs-lookup"><span data-stu-id="49d11-152">WIA Items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49d11-153">WIA_CATEGORY_AUTO</span><span class="sxs-lookup"><span data-stu-id="49d11-153">WIA_CATEGORY_AUTO</span></span></td>
<td><ul>
<li><span data-ttu-id="49d11-154"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-154"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="49d11-155"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-155"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="49d11-156"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-156"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="49d11-157"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefile</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-157"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="49d11-158">Der Eigenschaften Satz umfasst automatisch konfigurierte Scanner-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49d11-158">Property set includes auto-configured scanner properties.</span></span></td>
<td><span data-ttu-id="49d11-159">Ein automatisches Element, das die automatisch konfigurierten Überprüfungs Einstellungen des Scanners darstellt.</span><span class="sxs-lookup"><span data-stu-id="49d11-159">WIA auto item that represents the scanner's auto-configured scanning settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49d11-160">WIA_CATEGORY_FEEDER</span><span class="sxs-lookup"><span data-stu-id="49d11-160">WIA_CATEGORY_FEEDER</span></span></td>
<td><ul>
<li><span data-ttu-id="49d11-161"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-161"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="49d11-162"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-162"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="49d11-163"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypedocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-163"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="49d11-164"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-164"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="49d11-165"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-165"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="49d11-166">Der Eigenschaften Satz umfasst Eigenschaften des feedscannersteuerelements (normalerweise Bild-und Dokument spezifischer Eigenschaften Satz).</span><span class="sxs-lookup"><span data-stu-id="49d11-166">Property set includes feeder scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="49d11-167">WIA-feeselemente, einschließlich untergeordneter Elemente, die die Vorder-und Hintergrund Seiten eines Dokuments darstellen.</span><span class="sxs-lookup"><span data-stu-id="49d11-167">WIA Feeder items, including child items that represent the front and back pages of a document.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49d11-168">WIA_CATEGORY_FILM</span><span class="sxs-lookup"><span data-stu-id="49d11-168">WIA_CATEGORY_FILM</span></span></td>
<td><ul>
<li><span data-ttu-id="49d11-169"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-169"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="49d11-170"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-170"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="49d11-171"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-171"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="49d11-172"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-172"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="49d11-173">Der Eigenschaften Satz umfasst die Eigenschaften für den Filmscanner-Steuerelement (normalerweise Bild-und Dokument spezifischer Eigenschaften Satz)</span><span class="sxs-lookup"><span data-stu-id="49d11-173">Property set includes film scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="49d11-174">WIA-Film Elemente, einschließlich untergeordneter Elemente, die die einzelnen scanungs Rahmen darstellen.</span><span class="sxs-lookup"><span data-stu-id="49d11-174">WIA Film items, including child items that represent the individual scanning frames.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49d11-175">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="49d11-175">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><ul>
<li><span data-ttu-id="49d11-176"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-176"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></span></span></li>
<li><span data-ttu-id="49d11-177"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-177"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="49d11-178"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeaudiodatei</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-178"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></span></span></li>
<li><span data-ttu-id="49d11-179"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypevideo</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-179"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></span></span></li>
<li><span data-ttu-id="49d11-180"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypedocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-180"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="49d11-181"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-181"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="49d11-182">Die für dieses Element festgelegte Eigenschaft hängt vom Typ des gemeldeten Elements ab.</span><span class="sxs-lookup"><span data-stu-id="49d11-182">The property set on this item depends on the item type reported.</span></span> <span data-ttu-id="49d11-183">Beispielsweise sollte <a href="-wia-wia-item-type-flags.md"><strong>wiaitemtypeimage</strong></a> einige Bildelement Eigenschaften wie Bits pro Pixel usw. enthalten.</span><span class="sxs-lookup"><span data-stu-id="49d11-183">For example, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> should include some image item properties, like bits per pixel and so forth.</span></span></td>
<td><span data-ttu-id="49d11-184">WIA-Speicherelemente, einschließlich untergeordneter Elemente, die den fertiggestellten Dateiinhalt darstellen (Datendateien wie JPEG, HTML, txt usw.).</span><span class="sxs-lookup"><span data-stu-id="49d11-184">WIA storage items, including child items that represent finished file content (data files like JPEG, HTML, TXT, and so forth).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49d11-185">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="49d11-185">WIA_CATEGORY_FLATBED</span></span></td>
<td><ul>
<li><span data-ttu-id="49d11-186"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeprogrammabledatasource</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-186"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></span></span></li>
<li><span data-ttu-id="49d11-187"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypeimage</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-187"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></span></span></li>
<li><span data-ttu-id="49d11-188"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypedocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-188"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></span></span></li>
<li><span data-ttu-id="49d11-189"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypetransfer</strong></a></span><span class="sxs-lookup"><span data-stu-id="49d11-189"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></span></span></li>
<li><span data-ttu-id="49d11-190"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypefolder</strong></a>– kann vorhanden sein, wenn der Scanner das Scannen von mehreren Elementen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="49d11-190"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—may be present if the scanner supports multi-item scanning.</span></span></li>
<li><span data-ttu-id="49d11-191"><a href="-wia-wia-item-type-flags.md"><strong>Wiaitemtypegenerated</strong></a>– kann vorhanden sein, wenn die Anwendung während einer Scan Sitzung mit mehreren Elementen ein WIA-Element generiert.</span><span class="sxs-lookup"><span data-stu-id="49d11-191"><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>—may be present if the application generates a WIA item during a multi-item scanning session.</span></span></li>
</ul></td>
<td><span data-ttu-id="49d11-192">Der Eigenschaften Satz umfasst Eigenschaften für das Überprüfung des über prüfbilds (normalerweise Bild-und Dokument spezifischer Eigenschaften Satz).</span><span class="sxs-lookup"><span data-stu-id="49d11-192">The property set includes flatbed scanner control properties (usually image and document specific property set).</span></span></td>
<td><span data-ttu-id="49d11-193">Elemente mit einem flachen Element, einschließlich untergeordneter Elemente, die Bereiche darstellen, die auf der Registerkarte "Flatbed" des Scanners gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-193">WIA flatbed items, including child items that represent regions being scanned on the scanner's flatbed platen.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="49d11-194">Die folgende Abbildung zeigt ein Beispiel für eine WIA-Elementstruktur und die verschiedenen Kategorien, die jedem Element zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="49d11-194">The following graphic shows an example of a WIA item tree and the various categories that might be associated with each item.</span></span>

![Beispiele für Element Kategorien für Elemente in einem Baum](images/scannertree2.jpg)

## <a name="root-item"></a><span data-ttu-id="49d11-196">Stamm Element</span><span class="sxs-lookup"><span data-stu-id="49d11-196">Root Item</span></span>

<span data-ttu-id="49d11-197">Ein WIA-Stamm Element ist ein Ordner Element, das mit [**wiaitemtyperoot**](-wia-wia-item-type-flags.md) -und **wiaitemtypedevice** -Flags gekennzeichnet ist, die das Gerät selbst darstellen.</span><span class="sxs-lookup"><span data-stu-id="49d11-197">A WIA root item is a folder item marked with [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) and **WiaItemTypeDevice** flags that represents the device itself.</span></span> <span data-ttu-id="49d11-198">Sie enthält Geräte Attribute wie Hersteller, Gerätename und Treiber Attribute wie Treiber Version und Benutzeroberflächen-Klassen Bezeichner (CLSID).</span><span class="sxs-lookup"><span data-stu-id="49d11-198">It contains device attributes like manufacturer, device name, and driver attributes like driver version and user interface class identifier (CLSID).</span></span> <span data-ttu-id="49d11-199">Abbild Erstellungs Anwendungen rufen den Stamm der WIA-Elementstruktur auf, indem Sie die [**IWiaDevMgr2:: createdevice**](-wia-iwiadevmgr2-createdevice.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="49d11-199">Imaging applications get the root to the WIA item tree by calling [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) method.</span></span> <span data-ttu-id="49d11-200">Die Anwendung verwendet das root-Element, um Zugriff auf die einzelnen untergeordneten WIA-Elemente zu erhalten, indem die Struktur aufgelistet wird (siehe [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span><span class="sxs-lookup"><span data-stu-id="49d11-200">The application uses the root item to gain access to the individual child WIA items by enumerating the tree (see [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).</span></span>

## <a name="data-item"></a><span data-ttu-id="49d11-201">Datenelement</span><span class="sxs-lookup"><span data-stu-id="49d11-201">Data Item</span></span>

<span data-ttu-id="49d11-202">Alle Elemente, die zum Übertragen von Daten verwendet werden können, werden als Datenelement betrachtet.</span><span class="sxs-lookup"><span data-stu-id="49d11-202">Any item that can be use to transfer data is considered a data item.</span></span> <span data-ttu-id="49d11-203">Dies schließt Elemente ein, die mit dem [**wiaitemtypeprogrammiabledatasource**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="49d11-203">This includes items marked with the [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) flag.</span></span>

<span data-ttu-id="49d11-204">Ordner Elemente und nicht Ordner Elemente können die Möglichkeit zur Übertragung von Daten verfügbar machen, indem Sie mit dem [**wiaitemtypetransfer**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="49d11-204">Folder items and nonfolder items can expose the ability to transfer data by being marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag.</span></span> <span data-ttu-id="49d11-205">Jedes Element, für das dieses Flag festgelegt ist, muss die folgenden WIA-Element Eigenschaften bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="49d11-205">Any item with this flag set has to provide the following WIA item properties:</span></span>

-   [<span data-ttu-id="49d11-206">**WIA \_ IPA- \_ Zugriffs \_ Rechte**</span><span class="sxs-lookup"><span data-stu-id="49d11-206">**WIA\_IPA\_ACCESS\_RIGHTS**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="49d11-207">**WIA \_ IPA- \_ Element \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="49d11-207">**WIA\_IPA\_ITEM\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="49d11-208">**WIA \_ IPA- \_ Puffer \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="49d11-208">**WIA\_IPA\_BUFFER\_SIZE**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="49d11-209">**WIA \_ IPA- \_ Format**</span><span class="sxs-lookup"><span data-stu-id="49d11-209">**WIA\_IPA\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="49d11-210">**WIA \_ IPA- \_ bevorzugtes \_ Format**</span><span class="sxs-lookup"><span data-stu-id="49d11-210">**WIA\_IPA\_PREFERRED\_FORMAT**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="49d11-211">**WIA \_ IPA \_ TYMED**</span><span class="sxs-lookup"><span data-stu-id="49d11-211">**WIA\_IPA\_TYMED**</span></span>](-wia-wiaitempropcommonitem.md)
-   [<span data-ttu-id="49d11-212">**WIA \_ IPA- \_ Dateinamen \_ Erweiterung**</span><span class="sxs-lookup"><span data-stu-id="49d11-212">**WIA\_IPA\_FILENAME\_EXTENSION**</span></span>](-wia-wiaitempropcommonitem.md)

<span data-ttu-id="49d11-213">Programmierbare Datenquellen Elemente, die mit dem [**wiaitemtypetransfer**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet sind, müssen außerdem die erforderliche Eigenschaft für das Datenelement angeben.</span><span class="sxs-lookup"><span data-stu-id="49d11-213">Programmable data source items marked with the [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) flag must also supply the data item required property set.</span></span>

<span data-ttu-id="49d11-214">WIA-Datenelemente haben möglicherweise zusätzliche Eigenschaften, abhängig von den Flag-Einstellungen des Elements.</span><span class="sxs-lookup"><span data-stu-id="49d11-214">WIA data items may have additional properties depending on the item's flag settings.</span></span> <span data-ttu-id="49d11-215">Beispielsweise sollten WIA-Elemente, die mit dem [**wiaitemtypeimage**](-wia-wia-item-type-flags.md) -Flag gekennzeichnet sind, über Bild spezifische Informations Eigenschaften verfügen, wie [**WIA \_ IPA- \_ Tiefe**](-wia-wiaitempropcommonitem.md) und **WIA \_ IPA- \_ Anzahl \_ von \_ Zeilen**.</span><span class="sxs-lookup"><span data-stu-id="49d11-215">For example, WIA items marked with the [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) flag should have image specific information properties, like [**WIA\_IPA\_DEPTH**](-wia-wiaitempropcommonitem.md) and **WIA\_IPA\_NUMBER\_OF\_LINES**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49d11-216">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49d11-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="49d11-217">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="49d11-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49d11-218">**IWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="49d11-218">**IWiaItem2**</span></span>](-wia-iwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="49d11-219">**IEnumWiaItem2**</span><span class="sxs-lookup"><span data-stu-id="49d11-219">**IEnumWiaItem2**</span></span>](-wia-ienumwiaitem2.md)
</dt> <dt>

[<span data-ttu-id="49d11-220">**IWiaDevMgr2**</span><span class="sxs-lookup"><span data-stu-id="49d11-220">**IWiaDevMgr2**</span></span>](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



