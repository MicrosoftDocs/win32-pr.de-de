---
description: Dvinfo-Feld Einstellungen im msdv-Treiber
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Dvinfo-Feld Einstellungen im msdv-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746665"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="e5131-103">Dvinfo-Feld Einstellungen im msdv-Treiber</span><span class="sxs-lookup"><span data-stu-id="e5131-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="e5131-104">In diesem Abschnitt wird beschrieben, wie der msdv-Treiber die [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur füllt.</span><span class="sxs-lookup"><span data-stu-id="e5131-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="e5131-105">Die `DVINFO` -Struktur definiert den Format Block für PIN-Verbindungen zwischen msdv und anderen Filtern.</span><span class="sxs-lookup"><span data-stu-id="e5131-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="e5131-106">Standardmäßig wird der DV-Splitter Filter bei der Erfassung von einem DV-Gerät verwendet, und der DV-MUX-Filter wird bei der Übertragung an das Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5131-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="e5131-107">Allerdings können Anwendungen ihre eigenen benutzerdefinierten Filter bereitstellen, daher ist es hilfreich zu verstehen, wie msdv den `DVINFO` Format Block auffüllt.</span><span class="sxs-lookup"><span data-stu-id="e5131-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="e5131-108">Die- `DVINFO` Struktur enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="e5131-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="e5131-109">Zwei audiohilfsquelle (Aaux)-Quellpakete für den ersten und zweiten Audioblock.</span><span class="sxs-lookup"><span data-stu-id="e5131-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="e5131-110">Zwei Aaux-Quell Code Verwaltungs Pakete für den ersten und zweiten Audioblock.</span><span class="sxs-lookup"><span data-stu-id="e5131-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="e5131-111">Ein Video-Hilfsquelle (Vaux).</span><span class="sxs-lookup"><span data-stu-id="e5131-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="e5131-112">Ein Vaux-Quell Code Verwaltungspaket.</span><span class="sxs-lookup"><span data-stu-id="e5131-112">A VAUX source control pack.</span></span>

<span data-ttu-id="e5131-113">Jeder Frame in einem DV-Stream enthält Aaux-und Vaux-Pakete.</span><span class="sxs-lookup"><span data-stu-id="e5131-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="e5131-114">Der `DVINFO` Format Block ist jedoch statisch und wird nur zum Einrichten der Pin-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5131-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="e5131-115">Wenn der msdv-Treiber eine Verbindung herstellt, prüft er keines der Aaux-oder Vaux-Pakete im Stream.</span><span class="sxs-lookup"><span data-stu-id="e5131-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="e5131-116">Stattdessen wird ein Satz von Standardwerten basierend auf den folgenden Merkmalen des DV-Geräts verwendet:</span><span class="sxs-lookup"><span data-stu-id="e5131-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="e5131-117">Gibt an, ob das Gerät ein consumerformat (dvcr) oder ein Professional-Format (DVCPRO) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5131-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="e5131-118">Der Signaltyp</span><span class="sxs-lookup"><span data-stu-id="e5131-118">The signal type</span></span>
-   <span data-ttu-id="e5131-119">Ob das Format ' NTSC ' oder ' PAL ' ist.</span><span class="sxs-lookup"><span data-stu-id="e5131-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="e5131-120">(Wenn das Gerät diese Informationen nicht meldet, werden standardmäßig die NTSC-Einstellungen von msdv verwendet.)</span><span class="sxs-lookup"><span data-stu-id="e5131-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="e5131-121">Sobald das Streaming beginnt, liegt es in der Verantwortung der benutzermodusfilter, z. b. des DV-Splitters, den tatsächlichen Inhalt der einzelnen DV-Frames zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e5131-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="e5131-122">Da sich die Informationen von Frame zu Frame ändern können, muss der Filter möglicherweise eine dynamische Formatänderung durchführen.</span><span class="sxs-lookup"><span data-stu-id="e5131-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="e5131-123">Wenn sich die Audiorate z. b. ändert, muss der Filter möglicherweise den Audiotyp erneut aushandeln.</span><span class="sxs-lookup"><span data-stu-id="e5131-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="e5131-124">Wenn Sie eine DV-Datei vom Typ "Type-1" erfassen, `DVINFO` wird die Struktur in die Datei als Datenstrom Format ("strauf") geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5131-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="e5131-125">Diese Daten werden direkt aus dem von msdv bereitgestellten Format Block entnommen.</span><span class="sxs-lookup"><span data-stu-id="e5131-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="e5131-126">Wie bereits erwähnt, kann sich der tatsächliche Inhalt des Streams unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e5131-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="e5131-127">Es liegt in der Verantwortung der Anwendung, die Aaux-und Vaux-Pakete in jedem Frame zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="e5131-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="e5131-128">In den folgenden Themen finden Sie Tabellen, in denen alle von msdv verwendeten Felder aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e5131-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="e5131-129">Aaux-Quelle (as)-Paket</span><span class="sxs-lookup"><span data-stu-id="e5131-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="e5131-130">Aaux Source Control (ASC) Pack</span><span class="sxs-lookup"><span data-stu-id="e5131-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="e5131-131">Vaux-Quelle (VS)</span><span class="sxs-lookup"><span data-stu-id="e5131-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="e5131-132">Vaux-Quell Code Verwaltungspaket (VSC)</span><span class="sxs-lookup"><span data-stu-id="e5131-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="e5131-133">Beachten Sie beim Lesen dieser Tabellen die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="e5131-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="e5131-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="e5131-134">IEC 61834</span></span>
-   <span data-ttu-id="e5131-135">SMPTE 314m</span><span class="sxs-lookup"><span data-stu-id="e5131-135">SMPTE 314M</span></span>
-   <span data-ttu-id="e5131-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="e5131-136">SMPTE 370</span></span>

<span data-ttu-id="e5131-137">In jeder Tabelle gibt die erste Spalte den Feldcode an, gefolgt von der Anzahl der Bits (in Klammern).</span><span class="sxs-lookup"><span data-stu-id="e5131-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="e5131-138">Die restlichen Spalten gibt die Feldwerte an.</span><span class="sxs-lookup"><span data-stu-id="e5131-138">The remaining columns give the field values.</span></span> <span data-ttu-id="e5131-139">Viele der Felder Aaux und Vaux sind für die PIN-Verbindung nicht relevant. in diesem Fall legt msdv einen Dummy-Wert fest.</span><span class="sxs-lookup"><span data-stu-id="e5131-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="e5131-140">Der numerische Wert des gesamten Pakets wird unten in jeder Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5131-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="e5131-141">In den Hinweisen nach den einzelnen Tabellen finden Sie weitere Informationen über ausgewählte Felder.</span><span class="sxs-lookup"><span data-stu-id="e5131-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="e5131-142">Ausführliche Beschreibungen finden Sie unter Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="e5131-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="e5131-143">Außerdem haben einige Felder in SMPTE 314m/SMPTE 370 nicht dieselbe Bedeutung wie in IEC 61834.</span><span class="sxs-lookup"><span data-stu-id="e5131-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="e5131-144">Derzeit werden von DirectShow keine DVCPRO-Formate unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5131-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="e5131-145">Die für das DVCPRO-Formate aufgelisteten Werte werden für die zukünftige Verwendung definiert.</span><span class="sxs-lookup"><span data-stu-id="e5131-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e5131-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5131-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5131-147">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e5131-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="e5131-148">DV-Daten im AVI-Datei Format</span><span class="sxs-lookup"><span data-stu-id="e5131-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="e5131-149">Msdv-Treiber</span><span class="sxs-lookup"><span data-stu-id="e5131-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 



