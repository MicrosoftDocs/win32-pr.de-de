---
title: Daten werden von einem Format in ein anderes Format umgerechnet
description: Daten werden von einem Format in ein anderes Format umgerechnet
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Audiokomprimierungs-Manager (ACM), Daten werden umgerechnet
- ACM (Audiokomprimierungs-Manager), Daten werden umgerechnet
- ACM-Beispiele, Daten werden umgerechnet
- Konvertieren von Daten
- acmstreamopen-Funktion
- acmstreamsize-Funktion
- acmStreamPrepareHeader-Funktion
- acmStreamConvert-Funktion
- acmstreamunprepareheader-Funktion
- acmstreamclose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309919"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="d1c77-113">Daten werden von einem Format in ein anderes Format umgerechnet</span><span class="sxs-lookup"><span data-stu-id="d1c77-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="d1c77-114">Der ACM verwendet Stream-Funktionen, um die Datenformat Konvertierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="d1c77-115">Konverter im ACM ändern das Format, jedoch nicht den Datentyp.</span><span class="sxs-lookup"><span data-stu-id="d1c77-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="d1c77-116">Ein Konvertermodul kann z. b. 44-kHz-16-Bit-Daten in 44-kHz-, 8-Bit-Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="d1c77-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="d1c77-117">Die folgenden ACM-Funktionen unterstützen die Datenformat Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="d1c77-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="d1c77-118">Sie werden in der Reihenfolge aufgelistet, in der Sie normalerweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1c77-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="d1c77-119">Die [**acmstreamopen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) -Funktion öffnet einen konvertierungsstream.</span><span class="sxs-lookup"><span data-stu-id="d1c77-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="d1c77-120">Die [**acmstreamsize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) -Funktion berechnet die entsprechende Größe des Quell-oder Ziel Puffers.</span><span class="sxs-lookup"><span data-stu-id="d1c77-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="d1c77-121">Die [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) -Funktion bereitet Quell-und Ziel Puffer vor, die bei einer Konvertierung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="d1c77-122">Die [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) -Funktion konvertiert Daten in einem Quell Puffer in das Zielformat und schreibt die konvertierten Daten in den Ziel Puffer.</span><span class="sxs-lookup"><span data-stu-id="d1c77-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="d1c77-123">Die [**acmstreamunprepareheader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) -Funktion bereinigt den Quell-und Ziel Puffer, der von **acmStreamPrepareHeader** vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1c77-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="d1c77-124">Sie müssen diese Funktion vor dem Freigeben des Quell-und Ziel Puffers abrufen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="d1c77-125">Die [**acmstreamclose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) -Funktion schließt einen konvertierungsstream.</span><span class="sxs-lookup"><span data-stu-id="d1c77-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="d1c77-126">Wenn Sie Daten umrechnen, ermitteln Sie zunächst das Quellformat, und wählen Sie dann das Zielformat aus.</span><span class="sxs-lookup"><span data-stu-id="d1c77-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="d1c77-127">Die einfachste Möglichkeit hierfür ist die Verwendung der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion, die ein Dialogfeld für die Format Auswahl anzeigt und die Format Auswahl des Benutzers zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d1c77-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="d1c77-128">Wenn Sie das Quell-und das Zielformat kennen, können Sie mit [**acmstreamopen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) einen konvertierungsstream öffnen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="d1c77-129">Anschließend können Sie die [**acmstreamsize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) -Funktion verwenden, um die entsprechenden Puffergrößen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="d1c77-130">Der nächste Schritt besteht in der Vorbereitung der Puffer, die bei der Konvertierung mithilfe von [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="d1c77-131">Verwenden Sie zum Ausführen der Konvertierung [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) , bis alle Puffer verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="d1c77-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="d1c77-132">Wenn die Konvertierung abgeschlossen ist, verwenden Sie [**acmstreamunprepareheader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) , um die Puffer zu bereinigen, und verwenden Sie dann [**acmstreamclose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) , um den Konvertierungsdaten Strom zu schließen.</span><span class="sxs-lookup"><span data-stu-id="d1c77-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




