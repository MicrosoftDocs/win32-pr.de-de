---
description: Cryptxml unterstützt nativ die unten aufgeführten URIs.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Kryptografiealgorithmen für die digitale XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349008"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="5a471-103">Kryptografiealgorithmen für die digitale XML-Signatur</span><span class="sxs-lookup"><span data-stu-id="5a471-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="5a471-104">Cryptxml unterstützt nativ die unten aufgeführten URIs.</span><span class="sxs-lookup"><span data-stu-id="5a471-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="5a471-105">Wenn für kryptografische Algorithmen und Transformationen, die nicht Teil der systemeigenen Unterstützung sind, Unterstützung benötigt wird, können Sie [kryptografieapi: Next Generation](../seccng/cng-portal.md) und [kryptografische Erweiterungen der XML-Signatur](xml-digital-signature-cryptographic-extensions.md) verwenden, um neue Algorithmen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5a471-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="5a471-106">Unterstützte URIs</span><span class="sxs-lookup"><span data-stu-id="5a471-106">Supported URIs</span></span>

<span data-ttu-id="5a471-107">Digest-Methoden</span><span class="sxs-lookup"><span data-stu-id="5a471-107">Digest Methods</span></span>



| <span data-ttu-id="5a471-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="5a471-108">Constant</span></span>                                 | <span data-ttu-id="5a471-109">URI-Wert</span><span class="sxs-lookup"><span data-stu-id="5a471-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5a471-110">wszuri \_ xmlns \_ digsig \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="5a471-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="5a471-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="5a471-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="5a471-112">wszuri \_ xmlns \_ digsig \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="5a471-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="5a471-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="5a471-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="5a471-114">wszuri \_ xmlns \_ digsig \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="5a471-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="5a471-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="5a471-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="5a471-116">wszuri \_ xmlns \_ digsig \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="5a471-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="5a471-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="5a471-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="5a471-118">Signatur Methoden</span><span class="sxs-lookup"><span data-stu-id="5a471-118">Signature Methods</span></span>



| <span data-ttu-id="5a471-119">Konstante</span><span class="sxs-lookup"><span data-stu-id="5a471-119">Constant</span></span>                                        | <span data-ttu-id="5a471-120">URI-Wert</span><span class="sxs-lookup"><span data-stu-id="5a471-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="5a471-121">wszuri \_ xmlns- \_ \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="5a471-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="5a471-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="5a471-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="5a471-123">wszuri \_ xmlns \_ digsig \_ DSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="5a471-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="5a471-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="5a471-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="5a471-125">wszuri \_ xmlns \_ digsig \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="5a471-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="5a471-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="5a471-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="5a471-127">wszuri \_ xmlns \_ digsig \_ RSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="5a471-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="5a471-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="5a471-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="5a471-129">wszuri \_ xmlns \_ digsig \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="5a471-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="5a471-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="5a471-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="5a471-131">wszuri \_ xmlns- \_ \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="5a471-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="5a471-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="5a471-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="5a471-133">wszuri \_ xmlns- \_ \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="5a471-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="5a471-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="5a471-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="5a471-135">wszuri \_ xmlns- \_ \_ ECDSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="5a471-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="5a471-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="5a471-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="5a471-137">wszuri \_ xmlns- \_ \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="5a471-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="5a471-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="5a471-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="5a471-139">wszuri \_ xmlns \_ \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="5a471-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="5a471-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="5a471-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="5a471-141">wszuri \_ xmlns \_ \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="5a471-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="5a471-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="5a471-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="5a471-143">wszuri \_ xmlns \_ \_ HMAC \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="5a471-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="5a471-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="5a471-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="5a471-145">wszuri \_ xmlns \_ \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="5a471-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="5a471-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="5a471-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
