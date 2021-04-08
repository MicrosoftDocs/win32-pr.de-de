---
title: Eingabeformate, Eingabeeinstellungen und Dateneinheiten Erweiterungen
description: Eingabeformate, Eingabeeinstellungen und Dateneinheiten Erweiterungen
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media-Format-SDK, Eingabeformate und-Einstellungen
- Windows Media-Format-SDK, Dateneinheiten Erweiterungen
- Windows Media-Format-SDK, Nutz Last Erweiterungs Systeme
- Advanced Systems Format (ASF), Eingabeformate und Einstellungen
- ASF (Advanced Systems Format), Eingabeformate und Einstellungen
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Advanced Systems Format (ASF), Nutz Last Erweiterungs Systeme
- ASF (Advanced Systems Format), Nutz Last Erweiterungs Systeme
- Dateneinheiten Erweiterungen, Informationen zu
- Nutz Last Erweiterungs Systeme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947959"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="31e6c-114">Eingabeformate, Eingabeeinstellungen und Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="31e6c-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="31e6c-115">Das Writer-Objekt unterstützt Eingabeeinstellungen, Eingabeformate und Dateneinheiten Erweiterungen, die Ihnen alle die Steuerung der Funktionen des Writers ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="31e6c-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="31e6c-116">Es ist nicht immer offensichtlich, welche Methoden verwendet werden, um ein bestimmtes Feature zu steuern.</span><span class="sxs-lookup"><span data-stu-id="31e6c-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="31e6c-117">Eingabeformate sind Medienformate, in denen die grundlegenden Eigenschaften der Medien beschrieben werden, die Sie für die Codierung an den Writer übergeben.</span><span class="sxs-lookup"><span data-stu-id="31e6c-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="31e6c-118">So werden z. b. die Frame Größe und der Farbraum der Eingabe Videos durch das Eingabeformat beschrieben.</span><span class="sxs-lookup"><span data-stu-id="31e6c-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="31e6c-119">Eingabeeinstellungen sind Merkmale der Eingabedaten, die über die Grundlagen hinausgehen, oder Informationen zu Transformationen, die für die Daten durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="31e6c-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="31e6c-120">Einsprung-Videoeinstellungen und Informationen zu einem Wasserzeichen System sind Beispiele für Eingabeeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="31e6c-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="31e6c-121">Dateneinheiten Erweiterungen, die auch als Nutz Last Erweiterungs Systeme bezeichnet werden, sind Werte, die an einzelne Beispiele im Daten Abschnitt der Datei angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="31e6c-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="31e6c-122">SMPTE-Zeit Codes und nicht-quadratische Pixel Informationen sind Beispiele für Dateneinheiten Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="31e6c-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31e6c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31e6c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31e6c-124">**Konfigurieren von Dateneinheitserweiterung en**</span><span class="sxs-lookup"><span data-stu-id="31e6c-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="31e6c-125">**Dateneinheiten Erweiterungen**</span><span class="sxs-lookup"><span data-stu-id="31e6c-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="31e6c-126">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="31e6c-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="31e6c-127">**Eingabe Format-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="31e6c-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="31e6c-128">**Eingabeeinstellungen**</span><span class="sxs-lookup"><span data-stu-id="31e6c-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="31e6c-129">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="31e6c-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




