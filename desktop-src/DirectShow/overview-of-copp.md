---
description: Übersicht über COPP
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Übersicht über COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342726"
---
# <a name="overview-of-copp"></a><span data-ttu-id="57c59-103">Übersicht über COPP</span><span class="sxs-lookup"><span data-stu-id="57c59-103">Overview of COPP</span></span>

<span data-ttu-id="57c59-104">Im folgenden finden Sie die grundlegenden Schritte, die eine Anwendung ausführen muss, um das Certified Output Protection Protocol (COPP) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="57c59-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="57c59-105">**Zertifikat Kette des Treibers erhalten**</span><span class="sxs-lookup"><span data-stu-id="57c59-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="57c59-106">Erstellen Sie ein DirectShow-Wiedergabe Diagramm, das Video mit dem Video Mischungs-Renderer (VMR-7 oder VMR-9) oder dem [**erweiterten Videorenderer**](enhanced-video-renderer-filter.md) -Filter (EVR) rendert.</span><span class="sxs-lookup"><span data-stu-id="57c59-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="57c59-107">Fragen Sie den VMR für die [**iamcertifiedoutputprotection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="57c59-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="57c59-108">Nennen Sie [**iamcertifiedoutputprotection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="57c59-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="57c59-109">Diese Methode gibt eine 128-Bit-Zufallszahl aus dem Treiber zusammen mit einer Zertifikat Kette zurück, die den öffentlichen 2048-Bit-RSA-Schlüssel des Treibers enthält.</span><span class="sxs-lookup"><span data-stu-id="57c59-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="57c59-110">**Überprüfen der Zertifikat Kette**</span><span class="sxs-lookup"><span data-stu-id="57c59-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="57c59-111">Überprüfen Sie die Zertifikat Kette.</span><span class="sxs-lookup"><span data-stu-id="57c59-111">Validate the certificate chain.</span></span> <span data-ttu-id="57c59-112">Wenn die Zertifikatskette ungültig ist, wird beendet.</span><span class="sxs-lookup"><span data-stu-id="57c59-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="57c59-113">Überprüfen Sie die Zertifikat Sperr Liste.</span><span class="sxs-lookup"><span data-stu-id="57c59-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="57c59-114">Wenn eines der Zertifikate in der Zertifikat Kette in der Sperr Liste angezeigt wird, wird beendet.</span><span class="sxs-lookup"><span data-stu-id="57c59-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="57c59-115">Den öffentlichen RSA-Schlüssel aus der Zertifikat Kette erhalten.</span><span class="sxs-lookup"><span data-stu-id="57c59-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="57c59-116">**Initialisieren der COPP-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="57c59-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="57c59-117">Generieren Sie einen 128-Bit-AES-Sitzungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="57c59-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="57c59-118">Dieser Schlüssel wird verwendet, um Daten zu signieren und zu überprüfen, ob signierte Daten nicht manipuliert wurden.</span><span class="sxs-lookup"><span data-stu-id="57c59-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="57c59-119">Generieren Sie zwei kryptografisch sichere 32-Bit-Zufallszahlen.</span><span class="sxs-lookup"><span data-stu-id="57c59-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="57c59-120">Der erste ist eine Status Sequenznummer, die zweite eine Befehlssequenz Nummer.</span><span class="sxs-lookup"><span data-stu-id="57c59-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="57c59-121">Jedes Mal, wenn die Anwendung einen Befehl oder eine Status Anforderung sendet, erhöht Sie die entsprechende Sequenznummer und schließt diese Zahl in den COPP-Befehl oder die Anforderungs Daten ein.</span><span class="sxs-lookup"><span data-stu-id="57c59-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="57c59-122">Verketten Sie die Zufallszahl 128-Bit aus dem Grafiktreiber, dem AES-Sitzungsschlüssel, der Status Sequenznummer und der Befehlssequenz Nummer.</span><span class="sxs-lookup"><span data-stu-id="57c59-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="57c59-123">Verschlüsseln Sie dieses Bytearray mit dem öffentlichen Schlüssel des Treibers, und übergeben Sie das Ergebnis an [**iamcertifiedoutputprotection:: sessionsequencestart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span><span class="sxs-lookup"><span data-stu-id="57c59-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="57c59-124">**COPP-Befehle und-Status Anforderungen senden**</span><span class="sxs-lookup"><span data-stu-id="57c59-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="57c59-125">Fragen Sie die verfügbaren Schutz Typen und andere Informationen ab, indem Sie [**iamcertifiedoutputprotection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="57c59-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="57c59-126">Legen Sie die gewünschten Schutz Ebenen durch Aufrufen von [**iamcertifiedoutputprotection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)fest.</span><span class="sxs-lookup"><span data-stu-id="57c59-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="57c59-127">Fragen Sie regelmäßig die aktuelle lokale Schutz Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="57c59-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="57c59-128">Wiedergabe wird beendet, wenn die lokale Schutz Ebene unerwartet geändert wird oder wenn ein Problem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="57c59-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57c59-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57c59-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57c59-130">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="57c59-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



