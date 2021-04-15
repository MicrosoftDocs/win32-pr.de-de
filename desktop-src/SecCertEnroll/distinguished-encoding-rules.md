---
description: Abstract Syntax Notation One (ASN. 1) definiert die folgenden Regelsätze, die bestimmen, wie Datenstrukturen, die zwischen Computern gesendet werden, codiert und decodiert werden.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527002"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="a60e5-103">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="a60e5-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="a60e5-104">Abstract Syntax Notation One (ASN. 1) definiert die folgenden Regelsätze, die bestimmen, wie Datenstrukturen, die zwischen Computern gesendet werden, codiert und decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="a60e5-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="a60e5-105">Grundlegende Codierungsregeln (ber)</span><span class="sxs-lookup"><span data-stu-id="a60e5-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="a60e5-106">Kanonische Codierungsregeln (CER)</span><span class="sxs-lookup"><span data-stu-id="a60e5-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="a60e5-107">Distinguished Encoding Rules (der)</span><span class="sxs-lookup"><span data-stu-id="a60e5-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="a60e5-108">Gepackte Codierungsregeln (pro)</span><span class="sxs-lookup"><span data-stu-id="a60e5-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="a60e5-109">Der ursprüngliche Regelsatz wurde von der ber-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="a60e5-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="a60e5-110">CER und der wurden später als spezialisierte Teilmengen von ber entwickelt.</span><span class="sxs-lookup"><span data-stu-id="a60e5-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="a60e5-111">Pro wurde als Reaktion auf Kritik in Bezug auf die Menge an Bandbreite entwickelt, die zum Übertragen von Daten mit ber oder den zugehörigen Varianten erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="a60e5-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="a60e5-112">Pro bietet erhebliche Einsparungen.</span><span class="sxs-lookup"><span data-stu-id="a60e5-112">PER provides a significant savings.</span></span>

<span data-ttu-id="a60e5-113">Der wurde erstellt, um die Anforderungen der X. 509-Spezifikation für die sichere Datenübertragung zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a60e5-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="a60e5-114">Von der Zertifikatregistrierungs-API wird der exklusiv verwendet.</span><span class="sxs-lookup"><span data-stu-id="a60e5-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="a60e5-115">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="a60e5-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="a60e5-116">DER-Übertragungs Syntax</span><span class="sxs-lookup"><span data-stu-id="a60e5-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="a60e5-117">Der-Codierung von ASN. 1-Typen</span><span class="sxs-lookup"><span data-stu-id="a60e5-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="a60e5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a60e5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a60e5-119">ASN. 1-Typsystem</span><span class="sxs-lookup"><span data-stu-id="a60e5-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="a60e5-120">Zertifikat Anforderungs Codierung</span><span class="sxs-lookup"><span data-stu-id="a60e5-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="a60e5-121">Einführung in die ASN. 1-Syntax und-Codierung</span><span class="sxs-lookup"><span data-stu-id="a60e5-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



