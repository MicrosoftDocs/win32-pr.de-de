---
description: In diesem Thema werden Überlegungen zur Verwendung der XPS-API für digitale Signaturen zum Hinzufügen digitaler Signaturen zu einem XPS-Dokument aufgeführt.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Verwenden der XPS Digital-Signatur-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864955"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="9f8ff-103">Verwenden der XPS Digital-Signatur-API</span><span class="sxs-lookup"><span data-stu-id="9f8ff-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="9f8ff-104">In diesem Thema werden Überlegungen zur Verwendung der XPS-API für digitale Signaturen zum Hinzufügen digitaler Signaturen zu einem XPS-Dokument aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="9f8ff-105">Die XPS Digital Signature-API ermöglicht es Anwendungen, Benutzer aufzufordern, XPS-Dokumente zu signieren und Signaturen zu überprüfen, die in XPS-Dokumenten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="9f8ff-106">Die XPS Digital Signature-API kann auf ein XPS-Dokument angewendet werden, ohne Sie in ein XPS-OM zu laden, und kann für XPS-dokumentstreams verwendet werden, die aus einem XPS-OM serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="9f8ff-107">Der Abschnitt " [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) " enthält Themen, in denen beschrieben wird, wie Sie mit der XPS Digital Signature-API programmieren.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="9f8ff-108">In diesem Thema werden die folgenden Überlegungen für die Verwendung der XPS Digital Signature-API beim Hinzufügen von digitaler Signatur Unterstützung zu einer Anwendung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="9f8ff-109">XPS Digital Signature API-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="9f8ff-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="9f8ff-110">Besondere Hinweise zum Programmieren von XPS Digital Signature API</span><span class="sxs-lookup"><span data-stu-id="9f8ff-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="9f8ff-111">Überprüfen digitaler Signaturen in einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="9f8ff-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="9f8ff-112">Signatur Richtlinie für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="9f8ff-113">Einbetten einer Zertifikat Kette</span><span class="sxs-lookup"><span data-stu-id="9f8ff-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="9f8ff-114">Verwenden der CERT- \_ Kontext Struktur</span><span class="sxs-lookup"><span data-stu-id="9f8ff-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="9f8ff-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="9f8ff-116">XPS Digital Signature API-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="9f8ff-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="9f8ff-117">Dieser Abschnitt enthält Themen, in denen beschrieben wird, wie Programmieraufgaben mithilfe der XPS Digital Signature-API ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="9f8ff-118">Allgemeine Programmieraufgaben für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="9f8ff-119">Initialisieren des Signatur-Managers</span><span class="sxs-lookup"><span data-stu-id="9f8ff-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="9f8ff-120">Signieren eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="9f8ff-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="9f8ff-121">Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="9f8ff-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="9f8ff-122">Überprüfen von Dokument Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="9f8ff-123">Weitere Programmieraufgaben für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="9f8ff-124">Laden eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="9f8ff-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="9f8ff-125">Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f8ff-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="9f8ff-126">Überprüfen, ob das System eine Digest-Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f8ff-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="9f8ff-127">Einbinden von Zertifikat Ketten in ein Dokument</span><span class="sxs-lookup"><span data-stu-id="9f8ff-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="9f8ff-128">Besondere Hinweise zum Programmieren von XPS Digital Signature API</span><span class="sxs-lookup"><span data-stu-id="9f8ff-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="9f8ff-129">Die folgenden Themen erfordern einige besondere Überlegungen, wenn Sie die XPS Digital Signature-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="9f8ff-130">Überprüfen digitaler Signaturen in einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="9f8ff-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="9f8ff-131">Signatur Richtlinie für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="9f8ff-132">Einbetten einer Zertifikat Kette</span><span class="sxs-lookup"><span data-stu-id="9f8ff-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="9f8ff-133">Verwenden der CERT- \_ Kontext Struktur</span><span class="sxs-lookup"><span data-stu-id="9f8ff-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="9f8ff-134">Überprüfen digitaler Signaturen in einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="9f8ff-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="9f8ff-135">[**Ixpssignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) überprüft nur den signierten Inhalt, um zu bestimmen, dass er sich seit der Signierung nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="9f8ff-136">**Ixpssignature:: Verify** überprüft keines der Zertifikate, die zum Signieren des Dokument Inhalts verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="9f8ff-137">Weitere Informationen zu Zertifikaten und Kryptografie finden Sie unter Informationen [zur Kryptografie](/windows/desktop/SecCrypto/about-cryptography).</span><span class="sxs-lookup"><span data-stu-id="9f8ff-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="9f8ff-138">Ein Beispiel für die Überprüfung von Dokument Signaturen in einem Programm finden Sie unter [Überprüfen von Dokument Signaturen und Zertifikaten](verify-document-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="9f8ff-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="9f8ff-139">Signatur Richtlinie für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="9f8ff-140">Die Signatur Richtlinie für digitale Signaturen bestimmt, welche Teile eines XPS-Dokuments signiert sind.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="9f8ff-141">Eine Signatur Richtlinien Option besteht darin, die Signatur Beziehungen zu signieren, die mit dem Signatur Ursprungs Teil beginnen.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="9f8ff-142">Da sich die Signatur Beziehungen mit jeder hinzugefügten Signatur ändern, werden Signaturen, die unter dieser Richtlinie vorgenommen werden, beim Hinzufügen neuer Signaturen unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="9f8ff-143">Stellen Sie sicher, dass Sie die Auswirkungen und Auswirkungen der Einstellung dieser Richtlinie kennen. Andernfalls kann es zu unerwartetem oder unerwünschtem Verhalten kommen.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="9f8ff-144">Weitere Informationen zum Signieren von Richtlinien finden Sie unter [**XPS \_ Sign \_ Policy**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span><span class="sxs-lookup"><span data-stu-id="9f8ff-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="9f8ff-145">Einbetten einer Zertifikat Kette</span><span class="sxs-lookup"><span data-stu-id="9f8ff-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="9f8ff-146">Die Zertifikate, die die Vertrauenskette eines bestimmten Zertifikats bilden, können einem XPS-Dokument hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="9f8ff-147">Das Einbetten dieser Zertifikate kann es in Offline Szenarios vereinfachen, dass eine Anwendung die Zertifikate überprüft, die von einer digitalen Signatur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="9f8ff-148">Weitere Informationen zum Einbetten von Zertifikaten in ein XPS-Dokument finden Sie unter [Einbetten von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="9f8ff-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="9f8ff-149">Verwenden der CERT- \_ Kontext Struktur</span><span class="sxs-lookup"><span data-stu-id="9f8ff-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="9f8ff-150">Der [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) und die [**CERT \_ Info**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) -Strukturen sind die Hauptdaten Strukturen, die Zertifikat Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="9f8ff-151">Weitere Informationen zur Verwendung dieser Strukturen finden Sie unter [Verwenden einer Zertifikat \_ Info-Datenstruktur](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span><span class="sxs-lookup"><span data-stu-id="9f8ff-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="9f8ff-152">[**Zertifikat \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Strukturen, die von kryptografieapi-Funktionen zurückgegeben werden, müssen freigegeben werden, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="9f8ff-153">Um eine **CERT- \_ Kontext** Struktur freizugeben, nennen Sie die [**certfreecertifikatecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9f8ff-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f8ff-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f8ff-155">Allgemeine Programmieraufgaben für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="9f8ff-156">Weitere Programmieraufgaben für digitale Signaturen</span><span class="sxs-lookup"><span data-stu-id="9f8ff-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="9f8ff-157">**CERT- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="9f8ff-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="9f8ff-158">**Zertifikat \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="9f8ff-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="9f8ff-159">**Certfreecertififeecontext**</span><span class="sxs-lookup"><span data-stu-id="9f8ff-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="9f8ff-160">**XPS- \_ Signatur \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="9f8ff-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="9f8ff-161">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="9f8ff-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
