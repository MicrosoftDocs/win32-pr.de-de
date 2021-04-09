---
title: XML-Kanonisierung
description: Die XML-Kanonisierung löst das Problem der Umwandlung eines Satzes von XML-Knoten in Bytes auf eine Weise aus, dass triviale Änderungen an der XML-Datei (z. b. das Ändern der Reihenfolge von Attributen in einem Element) das resultierende Byte Formular nicht ändern.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- XML-kanonisierungsweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858558"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="3e49c-106">XML-Kanonisierung</span><span class="sxs-lookup"><span data-stu-id="3e49c-106">XML Canonicalization</span></span>

<span data-ttu-id="3e49c-107">Die XML-Kanonisierung löst das Problem der Umwandlung eines Satzes von XML-Knoten in Bytes auf eine Weise aus, dass triviale Änderungen an der XML-Datei (z. b. das Ändern der Reihenfolge von Attributen in einem Element) das resultierende Byte Formular nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="3e49c-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="3e49c-108">Die von der Kanonisierung erhaltenen Bytes werden häufig verwendet, um eine kryptografische Signatur über XML-Inhalt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3e49c-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="3e49c-109">Die häufig verwendeten XML-Kanonisierungsalgorithmen standardisieren die folgenden Aspekte:</span><span class="sxs-lookup"><span data-stu-id="3e49c-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="3e49c-110">Zeichencodierung (UTF-8 ohne Präambel)</span><span class="sxs-lookup"><span data-stu-id="3e49c-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="3e49c-111">Zeilenvorschub und andere Zeichen Formulare</span><span class="sxs-lookup"><span data-stu-id="3e49c-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="3e49c-112">Attribut Reihenfolge in einem Element</span><span class="sxs-lookup"><span data-stu-id="3e49c-112">Attribute order in an element</span></span>
-   <span data-ttu-id="3e49c-113">Leeres Element Formular</span><span class="sxs-lookup"><span data-stu-id="3e49c-113">Empty element form</span></span>
-   <span data-ttu-id="3e49c-114">Rendering von Namespace Deklarationen</span><span class="sxs-lookup"><span data-stu-id="3e49c-114">Rendering namespace declarations</span></span>

<span data-ttu-id="3e49c-115">Die APIs [**wsstartreadercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) und [**wsendreadercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) stellen die XML-kanonisierungsfunktionalität beim Lesen eines Dokuments bereit.</span><span class="sxs-lookup"><span data-stu-id="3e49c-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="3e49c-116">Die APIs [**wsstartwritercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) und [**wsendwritercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) stellen die XML-kanonisierungsfunktionalität beim Schreiben eines Dokuments bereit.</span><span class="sxs-lookup"><span data-stu-id="3e49c-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="3e49c-117">Die folgenden Enumerationen werden bei der Kanonisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="3e49c-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="3e49c-118">**WS- \_ XML- \_ Kanonisierungsalgorithmus \_**</span><span class="sxs-lookup"><span data-stu-id="3e49c-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="3e49c-119">**Eigenschaften-ID der WS- \_ XML- \_ Kanonisierung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e49c-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="3e49c-120">Die folgenden Funktionen werden bei der Kanonisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="3e49c-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="3e49c-121">**Wsendreadercanonicalization**</span><span class="sxs-lookup"><span data-stu-id="3e49c-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="3e49c-122">**Wsendschreiterkanonisierung**</span><span class="sxs-lookup"><span data-stu-id="3e49c-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="3e49c-123">**Wsstartreadercanonicalization**</span><span class="sxs-lookup"><span data-stu-id="3e49c-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="3e49c-124">**Wsstartschreitercanonicalization**</span><span class="sxs-lookup"><span data-stu-id="3e49c-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="3e49c-125">Die folgenden Strukturen werden bei der Kanonisierung verwendet:</span><span class="sxs-lookup"><span data-stu-id="3e49c-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="3e49c-126">**\_XML- \_ Kanonisierung \_ inklusive \_ Präfixe**</span><span class="sxs-lookup"><span data-stu-id="3e49c-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="3e49c-127">**WS \_ XML \_ Canonicalization ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="3e49c-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




