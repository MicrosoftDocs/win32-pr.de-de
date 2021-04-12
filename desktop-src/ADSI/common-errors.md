---
title: Häufige Fehler (ADSI)
description: Alle ADSI-spezifischen Fehler haben eine hexadezimale Form von 80005xxx. Die häufigsten Fehlercodes sind in der folgenden Tabelle aufgeführt.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "104314021"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="cfed1-104">Häufige Fehler (ADSI)</span><span class="sxs-lookup"><span data-stu-id="cfed1-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="cfed1-105">Alle ADSI-spezifischen Fehler haben eine hexadezimale Form von 80005xxx.</span><span class="sxs-lookup"><span data-stu-id="cfed1-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="cfed1-106">Die häufigsten Fehlercodes sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfed1-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="cfed1-107">ADSI Hex-Fehlercode</span><span class="sxs-lookup"><span data-stu-id="cfed1-107">ADSI hex error code</span></span> | <span data-ttu-id="cfed1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfed1-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfed1-109">80005000</span><span class="sxs-lookup"><span data-stu-id="cfed1-109">80005000</span></span><br/> | <span data-ttu-id="cfed1-110">Es wurde ein ungültiger ADSI-Pfadname übermittelt.</span><span class="sxs-lookup"><span data-stu-id="cfed1-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="cfed1-111">Dieser Fehler ergibt sich aus der Übergabe eines schlecht formatierten ADsPath an **GetObject** beim Binden an ein-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cfed1-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="cfed1-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="cfed1-112">8000500D</span></span><br/> | <span data-ttu-id="cfed1-113">Die ADSI-Eigenschaft wurde im Eigenschaften Cache nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="cfed1-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="cfed1-114">8000500e</span><span class="sxs-lookup"><span data-stu-id="cfed1-114">8000500E</span></span><br/> | <span data-ttu-id="cfed1-115">Das ADSI-Objekt ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cfed1-115">The ADSI object exists.</span></span> <span data-ttu-id="cfed1-116">Wenn Sie versuchen, ein ADSI-Objekt mit dem gleichen Namen wie ein vorhandenes ADSI-Objekt zu erstellen, tritt dieser Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cfed1-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="cfed1-117">Eine umfassende Liste der ADSI-Fehlercodes finden Sie unter [generische ADSI-Fehlercodes](generic-adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cfed1-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="cfed1-118">COM-Fehler</span><span class="sxs-lookup"><span data-stu-id="cfed1-118">COM Errors</span></span>

<span data-ttu-id="cfed1-119">Da ADSI aus COM-Objekten besteht, werden Standard-COM-Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfed1-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="cfed1-120">In der folgenden Tabelle sind die com-Fehlercodes aufgelistet, die in der ADSI-Programmierung am häufigsten auftreten.</span><span class="sxs-lookup"><span data-stu-id="cfed1-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="cfed1-121">COM-Hex-Fehlercode</span><span class="sxs-lookup"><span data-stu-id="cfed1-121">COM hex error code</span></span>  | <span data-ttu-id="cfed1-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cfed1-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfed1-123">80004005</span><span class="sxs-lookup"><span data-stu-id="cfed1-123">80004005</span></span><br/> | <span data-ttu-id="cfed1-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cfed1-124">Unspecified error.</span></span> <span data-ttu-id="cfed1-125">Die Ursache des COM-Objekt Fehlers ist von ADSI unbestimmt.</span><span class="sxs-lookup"><span data-stu-id="cfed1-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="cfed1-126">800041e4</span><span class="sxs-lookup"><span data-stu-id="cfed1-126">800041E4</span></span><br/> | <span data-ttu-id="cfed1-127">Objekt konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="cfed1-127">Object not found.</span></span> <span data-ttu-id="cfed1-128">Dieser Fehler tritt hauptsächlich auf, wenn die ADsPath-Zeichenfolge beim Binden an ein-Objekt falsch geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cfed1-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="cfed1-129">Weitere Beispiele für COM-Fehler, die möglicherweise bei der ADSI-Programmierung auftreten, finden Sie unter [generische com-Fehler Codes](generic-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cfed1-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="cfed1-130">Win32-Fehler</span><span class="sxs-lookup"><span data-stu-id="cfed1-130">Win32 Errors</span></span>

<span data-ttu-id="cfed1-131">Jeder Fehlercode der hexadezimalen Form 8007xxxx ist ein standardmäßiger Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cfed1-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="cfed1-132">Wenn Sie die letzten vier Ziffern von "hexadezimal" in "Decimal" konvertieren, können Sie über die Windows 2000-Befehlszeile auf den Fehler zugreifen:</span><span class="sxs-lookup"><span data-stu-id="cfed1-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="cfed1-133">**net helpmsg <number>**</span><span class="sxs-lookup"><span data-stu-id="cfed1-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="cfed1-134">In der obigen Befehlszeile ist " &lt; Number &gt; " die Dezimalzahl, die durch die typumrechnung der letzten vier Ziffern des Fehlercodes aus dem Hexadezimalwert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cfed1-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="cfed1-135">Diese Befehlszeile enthält eine ausführlichere Beschreibung des Win32-Fehlers, der beim Debuggen des Skripts sehr hilfreich sein kann.</span><span class="sxs-lookup"><span data-stu-id="cfed1-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





