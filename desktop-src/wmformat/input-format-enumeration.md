---
title: Eingabe Format-Enumeration
description: Eingabe Format-Enumeration
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media-Format-SDK, Eingabe Format-Enumerationen
- Windows Media-Format-SDK, Aufzählen von Eingabe Formaten
- Advanced Systems Format (ASF), Eingabe Format-Enumerationen
- ASF (Advanced Systems Format), Eingabe formatenumerationen
- Advanced Systems Format (ASF), Aufzählen von Eingabe Formaten
- ASF (Advanced Systems Format), Aufzählen von Eingabe Formaten
- Eingabe formatenumerationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471693"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="4af99-110">Eingabe Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4af99-110">Input Format Enumeration</span></span>

<span data-ttu-id="4af99-111">Das Writer-Objekt ruft streamformatinformationen aus dem Profil ab, das Sie ihm vergeben.</span><span class="sxs-lookup"><span data-stu-id="4af99-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="4af99-112">Die Datenstrom-Konfigurationsinformationen in einem Profil geben dem Writer alle Informationen, die er benötigt, um zu erfahren, wie die Daten in die Datei geschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4af99-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="4af99-113">Das Profil stellt dem Writer keine Informationen über das Format der Eingabe Beispiele zur Verfügung, die von der Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4af99-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="4af99-114">Eingabeformate sind nur für Datenströme unbekannt, die mit einem der Windows Media-Codecs komprimiert werden. Eingaben für beliebige Streamtypen sind auf der Grundlage der Informationen im Profil vorhersagbar.</span><span class="sxs-lookup"><span data-stu-id="4af99-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="4af99-115">Das Writer-Objekt kann mit dem Codec für einen Stream kommunizieren, um die Eingabetypen zu bestimmen, die verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="4af99-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="4af99-116">Zum Auflisten der möglichen Eingabetypen werden Methoden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4af99-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="4af99-117">Sie sollten immer den Eingabetyp ermitteln, der mit den Eingabemedien übereinstimmt, indem Sie die unterstützten Typen auflisten, anstatt die Eingabemedien Eigenschaften manuell festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4af99-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="4af99-118">Weitere Informationen finden [Sie unter so zählen Sie Eingabeformate auf](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="4af99-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4af99-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4af99-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4af99-120">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="4af99-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="4af99-121">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="4af99-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




