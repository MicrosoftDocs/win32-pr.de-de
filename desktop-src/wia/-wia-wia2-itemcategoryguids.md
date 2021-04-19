---
description: Windows-Abbild Erfassungs Elemente (WIA) 2,0 sind in Kategorien unterteilt, die definieren, wie ein IWiaItem2 behandelt oder verwendet werden soll.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: WIA 2,0-Element Kategorie-GUIDs (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348412"
---
# <a name="wia-20-item-category-guids"></a><span data-ttu-id="11b72-103">WIA 2,0-Element Kategorie-GUIDs</span><span class="sxs-lookup"><span data-stu-id="11b72-103">WIA 2.0 Item Category GUIDs</span></span>

<span data-ttu-id="11b72-104">Windows-Abbild Erfassungs Elemente (WIA) 2,0 sind in Kategorien unterteilt, die definieren, wie ein [**IWiaItem2**](-wia-iwiaitem2.md) behandelt oder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11b72-104">Windows Image Acquisition (WIA) 2.0 items are grouped into categories that define how a [**IWiaItem2**](-wia-iwiaitem2.md) is to be treated or used.</span></span> <span data-ttu-id="11b72-105">Wenn das Element z. b. einen feedvorgang darstellt, sollte die Anwendung erwarten, dass Sie die erforderlichen Eigenschaften für die Dokument feederstellung enthält und wie ein Dokument-feedvorgang funktioniert.</span><span class="sxs-lookup"><span data-stu-id="11b72-105">For example, if the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="11b72-106">Wenn das Element eine fertige Datei darstellt, sollte eine WIA 2,0-Anwendung diese auf diese Weise behandeln, wobei angenommen wird, dass die Daten statisch sind und sich auf dem Gerät befinden.</span><span class="sxs-lookup"><span data-stu-id="11b72-106">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="11b72-107">(Die Regeln für jedes Element werden in den einzelnen Spezifikations Dokumenten definiert.) Jede Kategorie verfügt über eine GUID-typkonstante.</span><span class="sxs-lookup"><span data-stu-id="11b72-107">(The rules for each item will be defined in their individual specification documents.) Each category has a GUID type constant.</span></span>



| <span data-ttu-id="11b72-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="11b72-108">Constant</span></span>                                                                                                                                                                                               | <span data-ttu-id="11b72-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11b72-109">Description</span></span>                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <span data-ttu-id="11b72-110"><dt>**Automatische WIA- \_ Kategorie \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-110"><dt>**WIA\_CATEGORY\_AUTO**</dt></span></span> </dl>                             | <span data-ttu-id="11b72-111">Ein Element, das die automatischen Konfigurationseinstellungen für ein WIA 2,0-Überprüfungs Gerät darstellt, das die automatisch konfigurierte Überprüfung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11b72-111">An item that represents the automatic configuration settings for a WIA 2.0 scanner device that supports auto-configured scanning.</span></span><br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <span data-ttu-id="11b72-112"><dt>**Kategorie- \_ \_ Feeder WIA**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-112"><dt>**WIA\_CATEGORY\_FEEDER**</dt></span></span> </dl>                       | <span data-ttu-id="11b72-113">Ein feedreement, bei dem es sich um eine programmierbare Datenquelle handelt und die Standardregeln und-Eigenschaften Sätze befolgt, die zur Unterstützung von Dokumenten</span><span class="sxs-lookup"><span data-stu-id="11b72-113">A feeder item that is a programmable data source and follows the standard rules and property sets required to support document feeders.</span></span><br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <span data-ttu-id="11b72-114"><dt>**Zurücksetzen \_ der \_ Kategorie \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-114"><dt>**WIA\_CATEGORY\_FEEDER\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="11b72-115">Eine programmierbare Datenquelle, die die Back-End-Datenquelle eines Duplex-Basis-feederelements beschreibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-115">A programmable data source describing the back side data source of a duplex base feeder item.</span></span><br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <span data-ttu-id="11b72-116"><dt>**\_ \_ \_ Vorschub**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-116"><dt>**WIA\_CATEGORY\_FEEDER\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="11b72-117">Eine programmierbare Datenquelle, die die Datenquelle auf der Vorderseite eines Duplex-Basis-feederelements beschreibt.</span><span class="sxs-lookup"><span data-stu-id="11b72-117">A programmable data source describing the front side data source of a duplex base feeder item.</span></span><br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <span data-ttu-id="11b72-118"><dt>**Film der Kategorie "WIA" \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-118"><dt>**WIA\_CATEGORY\_FILM**</dt></span></span> </dl>                             | <span data-ttu-id="11b72-119">Ein Film Element, bei dem es sich um eine programmierbare Datenquelle handelt und die Standardregeln und-Eigenschaften Sätze befolgt, die für die Unterstützung von Einheiten zur</span><span class="sxs-lookup"><span data-stu-id="11b72-119">A film item that is a programmable data source and follows the standard rules and property sets required to support film scanning units.</span></span><br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <span data-ttu-id="11b72-120"><dt>**Datei der WIA- \_ Kategorie \_ abgeschlossen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-120"><dt>**WIA\_CATEGORY\_FINISHED\_FILE**</dt></span></span> </dl> | <span data-ttu-id="11b72-121">Ein Element, das keine programmierbare Datenquelle ist, oder ein Element, das Daten in einem fertigen Dateiformat bereitstellt, oder ein Ordner Element, das fertige Dateiformat Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="11b72-121">An item that is not a programmable data source, or an item that provides data in a finished file format, or a folder item that contains finished file format items.</span></span><br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <span data-ttu-id="11b72-122"><dt>**WIA- \_ Kategorie \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-122"><dt>**WIA\_CATEGORY\_FLATBED**</dt></span></span> </dl>                    | <span data-ttu-id="11b72-123">Ein Element, das eine programmierbare Datenquelle ist und den Standardregeln und-Eigenschafts Sätzen folgt, die zur Unterstützung von pllans-Scanvorgängen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="11b72-123">A flatbed item that is a programmable data source and follows the standard rules and property sets required to support flatbed platen scanning.</span></span><br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <span data-ttu-id="11b72-124"><dt>**Ordner "WIA \_ Category" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-124"><dt>**WIA\_CATEGORY\_FOLDER**</dt></span></span> </dl>                       | <span data-ttu-id="11b72-125">Ein Ordner Speicher Element (keine programmierbare Datenquelle), das andere Ordner Elemente oder abgeschlossene Dateien oder beides enthält.</span><span class="sxs-lookup"><span data-stu-id="11b72-125">A folder storage item (not a programmable data source) containing other folder items or finished files or both.</span></span><br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <span data-ttu-id="11b72-126"><dt>**WIA \_ - \_ kategorienroot**</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-126"><dt>**WIA\_CATEGORY\_ROOT**</dt></span></span> </dl>                             | <span data-ttu-id="11b72-127">Das Stamm Element für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="11b72-127">The root item for the device.</span></span> <br/>                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="11b72-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11b72-128">Requirements</span></span>



| <span data-ttu-id="11b72-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11b72-129">Requirement</span></span> | <span data-ttu-id="11b72-130">Wert</span><span class="sxs-lookup"><span data-stu-id="11b72-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11b72-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11b72-131">Minimum supported client</span></span><br/> | <span data-ttu-id="11b72-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11b72-132">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="11b72-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11b72-133">Minimum supported server</span></span><br/> | <span data-ttu-id="11b72-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11b72-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11b72-135">Header</span><span class="sxs-lookup"><span data-stu-id="11b72-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="11b72-136"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="11b72-136"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




