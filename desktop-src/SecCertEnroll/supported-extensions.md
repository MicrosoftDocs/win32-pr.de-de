---
description: Sie können die IX509Extension-Schnittstelle verwenden, um eine beliebige Erweiterung zu definieren.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Unterstützte Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752161"
---
# <a name="supported-extensions"></a><span data-ttu-id="5eae2-103">Unterstützte Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="5eae2-103">Supported Extensions</span></span>

<span data-ttu-id="5eae2-104">Sie können die [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle verwenden, um eine beliebige Erweiterung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5eae2-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="5eae2-105">Die Zertifikatregistrierungs-API bietet auch Schnittstellen, die von **IX509Extension** abgeleitet werden, damit Sie problemlos eine der gängigsten Erweiterungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="5eae2-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="5eae2-106">Die folgende Liste enthält die allgemeinen Erweiterungen, die von Microsoft-Zertifizierungsstellen unterstützt werden, sowie die Objekt Bezeichner und Schnittstellen, die Sie verwenden können, um Sie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5eae2-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="5eae2-107">Alternativenames</span><span class="sxs-lookup"><span data-stu-id="5eae2-107">AlternativeNames</span></span>

<span data-ttu-id="5eae2-108">Die Alternative Namen Erweiterung kann verwendet werden, um mindestens ein alternatives namens Formular für den Betreff der Zertifikat Anforderung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5eae2-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="5eae2-109">Beispiele für alternative Namen sind E-Mail-Adressen, DNS-Namen, IP-Adressen und URIs.</span><span class="sxs-lookup"><span data-stu-id="5eae2-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="5eae2-110">**Schnittstelle:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="5eae2-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="5eae2-111">**OID:** XCN- \_ OID- \_ Betreff \_ alt \_ name2 (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="5eae2-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="5eae2-112">Autorityinformationaccess</span><span class="sxs-lookup"><span data-stu-id="5eae2-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="5eae2-113">Die Erweiterung Authority Information Access gibt Aufschluss über den Zugriff auf Zertifizierungsstellen Informationen und-Dienste.</span><span class="sxs-lookup"><span data-stu-id="5eae2-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="5eae2-114">Der Erweiterungs Wert enthält eine Sequenz von URIs.</span><span class="sxs-lookup"><span data-stu-id="5eae2-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="5eae2-115">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-116">**OID:** Informationen zum Zugriff auf die XCN- \_ OID- \_ Autorität \_ \_ (1.3.6.1.5.5.7.1.1)</span><span class="sxs-lookup"><span data-stu-id="5eae2-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="5eae2-117">Autoritykeyidentifier</span><span class="sxs-lookup"><span data-stu-id="5eae2-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="5eae2-118">Die Zertifizierungsstellen-schlüsselbezeichnererweiterung ermöglicht die Identifizierung des öffentlichen Zertifizierungsstellen Schlüssels, der dem privaten Schlüssel der Zertifizierungsstelle entspricht, der ein ausgestelltes Zertifikat signiert hat</span><span class="sxs-lookup"><span data-stu-id="5eae2-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="5eae2-119">Sie wird von einem Zertifikat Pfad zum Entwickeln von Software auf einem Windows-Server verwendet, um das Zertifizierungsstellen Zertifikat zu finden.</span><span class="sxs-lookup"><span data-stu-id="5eae2-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="5eae2-120">Wenn eine Zertifizierungsstelle ein Zertifikat ausgibt, wird der Erweiterungs Wert auf die Erweiterung " **subjetkeyidentifier** " im Signaturzertifikat der Zertifizierungsstelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5eae2-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="5eae2-121">Der Wert ist in der Regel ein SHA-1-Hash des öffentlichen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="5eae2-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="5eae2-122">**Schnittstelle:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="5eae2-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="5eae2-123">**OID:** XCN \_ OID \_ Authority \_ Key \_ Bezeichner2 (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="5eae2-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="5eae2-124">Basiceinschränkungen</span><span class="sxs-lookup"><span data-stu-id="5eae2-124">BasicConstraints</span></span>

<span data-ttu-id="5eae2-125">Mithilfe der Basis Einschränkungs Erweiterung können Sie feststellen, ob die Entität als Zertifizierungsstelle (Certification Authority, ca) verwendet werden kann. wenn dies der Fall ist, wird die Anzahl der untergeordneten Zertifizierungsstellen in der Zertifikat Kette verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eae2-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="5eae2-126">**Schnittstelle:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="5eae2-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="5eae2-127">**OID:** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="5eae2-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="5eae2-128">Certificatepolicies</span><span class="sxs-lookup"><span data-stu-id="5eae2-128">CertificatePolicies</span></span>

<span data-ttu-id="5eae2-129">Die Zertifikat Richtlinien Erweiterung kann verwendet werden, um die Richtlinien zu identifizieren, unter denen das Zertifikat ausgestellt wurde, und die Zwecke dafür können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eae2-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="5eae2-130">Diese werden durch eine Auflistung von Objekt Bezeichner (OIDs) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5eae2-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="5eae2-131">Die Richtlinien sind an die Anforderungen einer Organisation angepasst.</span><span class="sxs-lookup"><span data-stu-id="5eae2-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="5eae2-132">**Schnittstelle:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="5eae2-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="5eae2-133">**OID:** XCN- \_ OID- \_ Zertifikat \_ Richtlinien (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="5eae2-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="5eae2-134">Crldistributionpoints</span><span class="sxs-lookup"><span data-stu-id="5eae2-134">CrlDistributionPoints</span></span>

<span data-ttu-id="5eae2-135">Die Erweiterung für die Zertifikat Sperr Listen-Verteilungs Punkte enthält den URI der Basiszertifikat Sperr Liste (CRL).</span><span class="sxs-lookup"><span data-stu-id="5eae2-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="5eae2-136">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-137">**OID:** XCN \_ OID \_ CRL- \_ dist- \_ Punkte (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="5eae2-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="5eae2-138">Felds EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="5eae2-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="5eae2-139">Die erweiterte Schlüssel Verwendungs Erweiterung kann verwendet werden, um eine oder mehrere Verwendungen des im Zertifikat enthaltenen öffentlichen Schlüssels zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5eae2-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="5eae2-140">**Schnittstelle:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="5eae2-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="5eae2-141">**OID:** Erweiterte XCN- \_ OID- \_ \_ Schlüssel \_ Verwendung (2.5.29.37)</span><span class="sxs-lookup"><span data-stu-id="5eae2-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="5eae2-142">Freshestcrl</span><span class="sxs-lookup"><span data-stu-id="5eae2-142">FreshestCRL</span></span>

<span data-ttu-id="5eae2-143">Die neueste CRL-Erweiterung enthält den URI der Delta-CRL.</span><span class="sxs-lookup"><span data-stu-id="5eae2-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="5eae2-144">Dieselbe ASN. 1-Syntax wird für diese Erweiterung und die **crldistributionpoints** -Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eae2-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="5eae2-145">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-146">**OID:** XCN \_ OID \_ Freshest \_ CRL (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="5eae2-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="5eae2-147">Endeinheits Zertifikaten der</span><span class="sxs-lookup"><span data-stu-id="5eae2-147">KeyUsage</span></span>

<span data-ttu-id="5eae2-148">Die Schlüssel Verwendungs Erweiterung kann verwendet werden, um Einschränkungen für die Vorgänge zu definieren, die von dem im Zertifikat enthaltenen öffentlichen Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5eae2-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="5eae2-149">Sie können z. b. angeben, dass der öffentliche Schlüssel nur zum Erstellen einer digitalen Signatur verwendet werden soll, eine Zertifikat Sperr Liste signiert oder einen anderen Schlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="5eae2-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="5eae2-150">**Schnittstelle:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="5eae2-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="5eae2-151">**OID:** Verwendung von XCN \_ OID \_ Key \_ (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="5eae2-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="5eae2-152">Msapplicationpolicies</span><span class="sxs-lookup"><span data-stu-id="5eae2-152">MSApplicationPolicies</span></span>

<span data-ttu-id="5eae2-153">Die Microsoft-Anwendungsrichtlinien Erweiterung kann von einer Anwendung verwendet werden, um Zertifikate auf der Grundlage der zulässigen Verwendung zu filtern.</span><span class="sxs-lookup"><span data-stu-id="5eae2-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="5eae2-154">Zulässige Verwendungen werden durch OIDs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5eae2-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="5eae2-155">Diese Erweiterung ähnelt der Erweiterung **EnhancedKeyUsage** , aber mit einer strengeren Semantik, die auf die übergeordnete Zertifizierungsstelle angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5eae2-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="5eae2-156">Die Erweiterung ist Microsoft-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="5eae2-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="5eae2-157">**Schnittstelle:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="5eae2-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="5eae2-158">**OID:** Richtlinien für die XCN- \_ OID- \_ Anwendungs \_ Zertifikat \_ (1.3.6.1.4.1.311.21.10)</span><span class="sxs-lookup"><span data-stu-id="5eae2-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="5eae2-159">Nameconstraints</span><span class="sxs-lookup"><span data-stu-id="5eae2-159">NameConstraints</span></span>

<span data-ttu-id="5eae2-160">Die Erweiterung namens Einschränkungen dient zum Identifizieren des Namespace, in dem alle Antragsteller Namen von Zertifikaten in einer Zertifikat Hierarchie gefunden werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5eae2-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="5eae2-161">Die Erweiterung wird lediglich in einem Zertifizierungsstellenzertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="5eae2-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="5eae2-162">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-163">**OID:** Einschränkungen für den XCN- \_ OID- \_ Namen \_ (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="5eae2-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="5eae2-164">Policyeinschränkungen</span><span class="sxs-lookup"><span data-stu-id="5eae2-164">PolicyConstraints</span></span>

<span data-ttu-id="5eae2-165">Die richtlinieneinschränkungs-Erweiterung wird Zertifizierungsstellen Zertifikaten hinzugefügt, um die Pfad Validierung einzuschränken, indem die Richtlinien Zuordnung untersagt wird oder dass jedes Zertifikat in der Hierarchie eine akzeptable Richtlinien Kennung enthält.</span><span class="sxs-lookup"><span data-stu-id="5eae2-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="5eae2-166">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-167">**OID:** Einschränkungen für XCN- \_ OID- \_ Richtlinien \_ (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="5eae2-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="5eae2-168">Policymappings</span><span class="sxs-lookup"><span data-stu-id="5eae2-168">PolicyMappings</span></span>

<span data-ttu-id="5eae2-169">Die Erweiterung Richtlinien Zuordnungen dient zum Identifizieren der Richtlinien in einer untergeordneten Zertifizierungsstelle, die den Richtlinien in der ausstellenden Zertifizierungsstelle entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5eae2-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="5eae2-170">Der Erweiterungs Wert enthält eine Sequenz von Richtlinien Zuordnungen für ausstellende Zertifizierungsstellen und untergeordnete Zertifizierungsstellen, die von Objekt Bezeichnern dargestellt werden</span><span class="sxs-lookup"><span data-stu-id="5eae2-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="5eae2-171">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-172">**OID:** Zuordnungen von XCN- \_ OID- \_ Richtlinien \_ (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="5eae2-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="5eae2-173">Privatekeyusageperiod</span><span class="sxs-lookup"><span data-stu-id="5eae2-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="5eae2-174">Die Erweiterung für den privaten Schlüssel Verwendungs Zeitraum wird verwendet, um eine andere Gültigkeitsdauer für den privaten Schlüssel anzugeben, als für das Zertifikat, dem der Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5eae2-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="5eae2-175">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-176">**OID:** Verwendungs Zeitraum für XCN \_ OID \_ PrivateKey \_ \_ (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="5eae2-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="5eae2-177">SMIME-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5eae2-177">SmimeCapabilities</span></span>

<span data-ttu-id="5eae2-178">Die Secure/Multipurpose Internet Mail Extensions (S/MIME)-Funktionserweiterung kann verwendet werden, um die Entschlüsselungs Funktionen eines e-Mail-Empfängers an den Absender der e-Mail-Nachricht zu melden, damit der Absender den sichersten Verschlüsselungsalgorithmus auswählen kann, der von beiden Parteien unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5eae2-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="5eae2-179">Der Erweiterungs Wert enthält eine Sammlung von symmetrischen Verschlüsselungsalgorithmus-OIDs und eine optionale Verschlüsselungsstärke.</span><span class="sxs-lookup"><span data-stu-id="5eae2-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="5eae2-180">**Schnittstelle:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="5eae2-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="5eae2-181">**OID:** XCN \_ OID \_ RSA \_ SMIME-Funktionen (1.2.840.113549.1.9.15)</span><span class="sxs-lookup"><span data-stu-id="5eae2-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="5eae2-182">Subjetdirectoriyattribute</span><span class="sxs-lookup"><span data-stu-id="5eae2-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="5eae2-183">Die Erweiterung "Subject Directory-Attribute" kann verwendet werden, um Identifikations Attribute wie die Nationalität des Zertifikat Antragstellers zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5eae2-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="5eae2-184">Der Erweiterungswert ist eine Folge von OID-Wertepaaren.</span><span class="sxs-lookup"><span data-stu-id="5eae2-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="5eae2-185">**Schnittstelle:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="5eae2-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="5eae2-186">**OID:** XCN \_ OID \_ Subject \_ dir \_ attrs (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="5eae2-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="5eae2-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="5eae2-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="5eae2-188">Mithilfe der Erweiterung "Subject Key Identifier" können Sie zwischen mehreren öffentlichen Schlüsseln unterscheiden, die vom Zertifikat Antragsteller aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="5eae2-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="5eae2-189">Der Erweiterungswert ist normalerweise ein SHA-1-Hash des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="5eae2-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="5eae2-190">**Schnittstelle:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="5eae2-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="5eae2-191">**OID:** Schlüssel Bezeichner für den XCN- \_ OID- \_ Betreff \_ \_ (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="5eae2-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="5eae2-192">Vorlage</span><span class="sxs-lookup"><span data-stu-id="5eae2-192">Template</span></span>

<span data-ttu-id="5eae2-193">Mithilfe der Vorlagen Erweiterung kann die Vorlage Version 2 identifiziert werden, die beim ausstellen oder Erneuern eines Zertifikats verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eae2-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="5eae2-194">Der Erweiterungs Wert enthält die Vorlagen-OID und optionale Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="5eae2-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="5eae2-195">Die Erweiterung ist Microsoft-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="5eae2-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="5eae2-196">**Schnittstelle:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="5eae2-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="5eae2-197">**OID:** XCN \_ OID- \_ Zertifikat \_ Vorlage (1.3.6.1.4.1.311.21.7)</span><span class="sxs-lookup"><span data-stu-id="5eae2-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="5eae2-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="5eae2-198">TemplateName</span></span>

<span data-ttu-id="5eae2-199">Mithilfe der Vorlagen Namen Erweiterung kann die Vorlage Version 1 identifiziert werden, die beim ausstellen oder Erneuern eines Zertifikats verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eae2-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="5eae2-200">Der Erweiterungs Wert enthält den Namen der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="5eae2-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="5eae2-201">Die Erweiterung ist Microsoft-spezifisch.</span><span class="sxs-lookup"><span data-stu-id="5eae2-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="5eae2-202">**Schnittstelle:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="5eae2-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="5eae2-203">**OID:** XCN \_ OID \_ ENROLL \_ certtype- \_ Erweiterung (1.3.6.1.4.1.311.20.2)</span><span class="sxs-lookup"><span data-stu-id="5eae2-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eae2-204">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5eae2-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eae2-205">Extensions (Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="5eae2-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



