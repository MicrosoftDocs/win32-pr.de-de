---
description: In einer Microsoft-PKI werden Zertifikat Anforderungen von Client Computern an Zertifizierungsstellen (CAS) als binäre Zeichenfolge gesendet, die eine Sequenz von codierten Datenstrukturen enthält.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Zertifikat Anforderungs Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756546"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="4e602-103">Zertifikat Anforderungs Codierung</span><span class="sxs-lookup"><span data-stu-id="4e602-103">Certificate Request Encoding</span></span>

<span data-ttu-id="4e602-104">In einer Microsoft-PKI werden Zertifikat Anforderungen von Client Computern an Zertifizierungsstellen (CAS) als binäre Zeichenfolge gesendet, die eine Sequenz von codierten Datenstrukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="4e602-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="4e602-105">Die Zertifikatregistrierungs-API verwendet die abstrakte Syntax Notation One (ASN. 1), um diese Strukturen zu beschreiben und zu codieren.</span><span class="sxs-lookup"><span data-stu-id="4e602-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="4e602-106">Im Rahmen dieser Dokumentation kann ASN. 1 konzeptionell in die Syntax Regeln (ISO 8824) unterteilt werden, die die Datenstrukturen und Codierungsregeln (ISO 8825) beschreiben, die angeben, wie die Daten für die Netzwerkübertragung codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4e602-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="4e602-107">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4e602-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4e602-108">Einführung in die ASN. 1-Syntax und-Codierung</span><span class="sxs-lookup"><span data-stu-id="4e602-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="4e602-109">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="4e602-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="4e602-110">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="4e602-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="4e602-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e602-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e602-112">Informationen zur Zertifikatregistrierungs-API</span><span class="sxs-lookup"><span data-stu-id="4e602-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



