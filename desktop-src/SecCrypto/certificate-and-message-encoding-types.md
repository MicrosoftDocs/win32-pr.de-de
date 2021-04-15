---
description: Für viele der Funktionen sind Zertifikat-oder Nachrichten Codierungs Typen erforderlich.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Zertifikat-und Nachrichten Codierungs Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3193b321d27892f8df9535ef81b8a988bf558e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484694"
---
# <a name="certificate-and-message-encoding-types"></a><span data-ttu-id="41cc4-103">Zertifikat-und Nachrichten Codierungs Typen</span><span class="sxs-lookup"><span data-stu-id="41cc4-103">Certificate and Message Encoding Types</span></span>

<span data-ttu-id="41cc4-104">Für viele der Funktionen sind Zertifikat-oder [*Nachrichten Codierungs Typen*](../secgloss/m-gly.md)erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41cc4-104">Many of the functions require certificate or [*message encoding types*](../secgloss/m-gly.md).</span></span> <span data-ttu-id="41cc4-105">Dieser Codierungstyp ist ein **DWORD**, das möglicherweise sowohl den Zertifikat-als auch den Nachrichten Codierungstyp enthält.</span><span class="sxs-lookup"><span data-stu-id="41cc4-105">This encoding type is a **DWORD**, possibly containing both the certificate and message encoding types.</span></span> <span data-ttu-id="41cc4-106">Der zertifikatcodierungstyp wird im nieder wertigen Wort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="41cc4-106">The certificate encoding type is stored in the low-order word.</span></span> <span data-ttu-id="41cc4-107">Der Nachrichten Codierungstyp wird im hohen Bestell Wort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="41cc4-107">The message encoding type is stored in the high-order word.</span></span> <span data-ttu-id="41cc4-108">Für einige Funktionen oder Struktur Felder ist nur einer der Codierungs Typen erforderlich, aber es ist immer akzeptabel, beide Codierungs Typen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41cc4-108">Some functions or structure fields require only one of the encoding types, but it is always acceptable to specify both encoding types.</span></span> <span data-ttu-id="41cc4-109">Ein Beispiel für die Angabe beider Codierungs Typen finden Sie unter [ \# includes und \# Definitionen](-includes-and--defines.md).</span><span class="sxs-lookup"><span data-stu-id="41cc4-109">For an example specifying both encoding types, see [\#includes and \#defines](-includes-and--defines.md).</span></span>

<span data-ttu-id="41cc4-110">Die folgende Parameter Benennungs Konvention wird verwendet, um die erforderlichen Codierungs Typen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41cc4-110">The following parameter naming convention is used to indicate the encoding types required.</span></span>



| <span data-ttu-id="41cc4-111">Name</span><span class="sxs-lookup"><span data-stu-id="41cc4-111">Name</span></span>                       | <span data-ttu-id="41cc4-112">Kommentare</span><span class="sxs-lookup"><span data-stu-id="41cc4-112">Comments</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cc4-113">*dwmsgandcertencodingtype*</span><span class="sxs-lookup"><span data-stu-id="41cc4-113">*dwMsgAndCertEncodingType*</span></span> | <span data-ttu-id="41cc4-114">Beide Codierungs Typen sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41cc4-114">Both encoding types are required.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="41cc4-115">*dwmsgencodingtype*</span><span class="sxs-lookup"><span data-stu-id="41cc4-115">*dwMsgEncodingType*</span></span>        | <span data-ttu-id="41cc4-116">Nur der Nachrichten Codierungstyp ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41cc4-116">Only the message encoding type is required.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="41cc4-117">*dwcertencodingtype*</span><span class="sxs-lookup"><span data-stu-id="41cc4-117">*dwCertEncodingType*</span></span>       | <span data-ttu-id="41cc4-118">Nur der zertifikatcodierungstyp ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41cc4-118">Only the certificate encoding type is required.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="41cc4-119">*dwencodingtype*</span><span class="sxs-lookup"><span data-stu-id="41cc4-119">*dwEncodingType*</span></span>           | <span data-ttu-id="41cc4-120">Es ist entweder ein Nachrichten-oder zertifikatcodierungstyp erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41cc4-120">Either a message or certificate encoding type is required.</span></span> <span data-ttu-id="41cc4-121">Wenn das nieder wertige Wort, das den Zertifikat Codierungstyp enthält, nicht NULL ist, wird es verwendet.</span><span class="sxs-lookup"><span data-stu-id="41cc4-121">If the low-order word containing the certificate encoding type is nonzero, then it is used.</span></span> <span data-ttu-id="41cc4-122">Andernfalls wird das höchst wertige Wort verwendet, das den Nachrichten Codierungstyp enthält.</span><span class="sxs-lookup"><span data-stu-id="41cc4-122">Otherwise, the high-order word containing the message encoding type is used.</span></span> <span data-ttu-id="41cc4-123">Wenn beide angegeben werden, wird der Zertifikat Codierungstyp in der nieder wertigen Word verwendet.</span><span class="sxs-lookup"><span data-stu-id="41cc4-123">If both are specified, the certificate encoding type in the low-order word is used.</span></span> |



 

<span data-ttu-id="41cc4-124">Die in der folgenden Tabelle aufgeführten aktuellen Codierungs Typen sind aktuell definiert.</span><span class="sxs-lookup"><span data-stu-id="41cc4-124">Currently defined encoding types are shown in the following table.</span></span>



| <span data-ttu-id="41cc4-125">Codierungstyp</span><span class="sxs-lookup"><span data-stu-id="41cc4-125">Encoding type</span></span>          | <span data-ttu-id="41cc4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="41cc4-126">Value</span></span>      |
|------------------------|------------|
| <span data-ttu-id="41cc4-127">Crypt- \_ ASN- \_ Codierung</span><span class="sxs-lookup"><span data-stu-id="41cc4-127">CRYPT\_ASN\_ENCODING</span></span>   | <span data-ttu-id="41cc4-128">0x00000001</span><span class="sxs-lookup"><span data-stu-id="41cc4-128">0x00000001</span></span> |
| <span data-ttu-id="41cc4-129">X509- \_ ASN- \_ Codierung</span><span class="sxs-lookup"><span data-stu-id="41cc4-129">X509\_ASN\_ENCODING</span></span>    | <span data-ttu-id="41cc4-130">0x00000001</span><span class="sxs-lookup"><span data-stu-id="41cc4-130">0x00000001</span></span> |
| <span data-ttu-id="41cc4-131">PKCS \_ 7- \_ ASN- \_ Codierung</span><span class="sxs-lookup"><span data-stu-id="41cc4-131">PKCS\_7\_ASN\_ENCODING</span></span> | <span data-ttu-id="41cc4-132">0x00010000</span><span class="sxs-lookup"><span data-stu-id="41cc4-132">0x00010000</span></span> |



 

 

 
