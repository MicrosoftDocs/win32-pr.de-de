---
description: Cryptxml bietet einen Low-Level-Satz an APIs, mit denen Anwendungen eingehüllte, umhüllende und getrennte Signaturen erstellen und überprüfen können. Sie können cryptxml zum Erstellen und Überprüfen von Inhalten verwenden, die in Signatur Objekt Elementen, einschließlich Manifesten, gespeichert sind.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: XML-Funktionen der digitalen Signatur-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362502"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="ad9b7-104">XML-Funktionen der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="ad9b7-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="ad9b7-105">Cryptxml bietet einen Low-Level-Satz an APIs, mit denen Anwendungen eingehüllte, umhüllende und getrennte Signaturen erstellen und überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="ad9b7-106">Sie können cryptxml zum Erstellen und Überprüfen von Inhalten verwenden, die in Signatur Objekt Elementen, einschließlich Manifesten, gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="ad9b7-107">Ein öffentlicher/privater, gemeinsam verwendeter Schlüssel oder ein [*X. 509*](../secgloss/x-gly.md) -Zertifikat oder eine Zertifikat Kette kann zum Signieren und Überprüfen der digitalen XML- [*Signatur*](../secgloss/d-gly.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="ad9b7-108">Anwendungen, die cryptxml zum Überprüfen externer Verweise verwenden (Verweise, die auf ein externes Dokument oder eine externe Datei außerhalb des Dokument Kontexts abzielen), müssen die externen URIs auflösen und die zu verdauenden Daten abrufen.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="ad9b7-109">Informationen zu den kryptografischen Algorithmen, die von cryptxml unterstützt werden, finden Sie unter [Kryptografiealgorithmen für die digitale XML-Signatur](xml-digital-signature-cryptographic-algorithms.md)</span><span class="sxs-lookup"><span data-stu-id="ad9b7-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="ad9b7-110">Cryptxml bietet Unterstützung für Kanonisierungsalgorithmen mit den folgenden bezeichlern.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="ad9b7-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="ad9b7-111">Constant</span></span>                                              | <span data-ttu-id="ad9b7-112">URI-Wert</span><span class="sxs-lookup"><span data-stu-id="ad9b7-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ad9b7-113">wszuri- \_ Kanonisierung \_ C14N</span><span class="sxs-lookup"><span data-stu-id="ad9b7-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="ad9b7-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="ad9b7-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="ad9b7-115">wszuri- \_ Kanonisierung \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="ad9b7-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="ad9b7-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="ad9b7-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="ad9b7-117">wszuri \_ Canonicalization \_ exslusive \_ C14N</span><span class="sxs-lookup"><span data-stu-id="ad9b7-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="ad9b7-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="ad9b7-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="ad9b7-119">wszuri \_ Canonicalization \_ exslusive \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="ad9b7-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="ad9b7-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="ad9b7-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="ad9b7-121">Cryptxml bietet Unterstützung für die Transformation für eingeschlossene Signaturen.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="ad9b7-122">Konstante</span><span class="sxs-lookup"><span data-stu-id="ad9b7-122">Constant</span></span>                                       | <span data-ttu-id="ad9b7-123">URI-Wert</span><span class="sxs-lookup"><span data-stu-id="ad9b7-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ad9b7-124">wszuri \_ xmlns- \_ Transformation \_</span><span class="sxs-lookup"><span data-stu-id="ad9b7-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="ad9b7-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="ad9b7-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="ad9b7-126">Standardmäßig unterstützt cryptxml keine XPath-oder XSLT-Transformationen.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="ad9b7-127">Wenn dies erforderlich ist, können Anwendungen diese Transformationen zusätzlich zu "cryptxml" implementieren.</span><span class="sxs-lookup"><span data-stu-id="ad9b7-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
