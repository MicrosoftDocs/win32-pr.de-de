---
description: XML ist ein Industriestandard, mit dem strukturierte Daten beschrieben werden. Eine digitale XML-Signatur ist eine XML-Darstellung einer digitalen Signatur, die die Möglichkeit bietet, den Ursprung und die Integrität von XML-Dokumenten und extern referenzierten Daten zu überprüfen.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Übersicht über die digitale XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367973"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="1480f-104">Übersicht über die digitale XML-Signatur</span><span class="sxs-lookup"><span data-stu-id="1480f-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="1480f-105">XML ist ein Industriestandard, mit dem strukturierte Daten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1480f-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="1480f-106">Eine digitale XML-Signatur ist eine XML-Darstellung einer [*digitalen Signatur*](../secgloss/d-gly.md) , die die Möglichkeit bietet, den Ursprung und die Integrität von XML-Dokumenten und extern referenzierten Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1480f-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="1480f-107">Digitale XML-Signaturen können verwendet werden, um beliebige Daten zu signieren, einschließlich XML-Dokument oder-Fragment, HTML-Seite, nur-Text oder binär codierte Daten, z. b. eine JPEG-Datei.</span><span class="sxs-lookup"><span data-stu-id="1480f-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="1480f-108">Das von der kryptotxml Digital Signature-API unterstützte XML-Format der digitalen Signatur wird durch die W3C-Empfehlung XML-Signatur Syntax und-Verarbeitung (Second Edition) angegeben.</span><span class="sxs-lookup"><span data-stu-id="1480f-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="1480f-109">Die digitale Signatur von cryptxml implementiert die Unterstützung für die erforderlichen Signatur Typen, Kryptografiealgorithmen, Kanonisierungsalgorithmen und die angegebene eingeschlossene Transformation.</span><span class="sxs-lookup"><span data-stu-id="1480f-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="1480f-110">Entwickler können den von cryptxml unterstützten Standardsatz von Kryptografiealgorithmen durch Erstellen von kryptografieerweiterungs-DLLs erweitern.</span><span class="sxs-lookup"><span data-stu-id="1480f-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="1480f-111">Entwickler können auch Ihre eigenen benutzerdefinierten Transformationen und Kanonisierungsalgorithmen zusätzlich zur cryptxml-API erstellen.</span><span class="sxs-lookup"><span data-stu-id="1480f-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="1480f-112">Entwickler können die cryptxml-APIs mit den Windows-Zertifikat-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="1480f-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
