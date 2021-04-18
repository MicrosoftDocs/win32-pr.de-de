---
title: EAP-Attribute
description: Ist eine EAP- \_ Attribut Struktur, die einen vordefinierten Datentyp enthält, der sich auf eine Authentifizierungs Sitzung bezieht.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106338701"
---
# <a name="eap-attributes"></a><span data-ttu-id="4ff5f-103">EAP-Attribute</span><span class="sxs-lookup"><span data-stu-id="4ff5f-103">EAP Attributes</span></span>

<span data-ttu-id="4ff5f-104">Ein EAP-Attribut ist eine [**EAP- \_ Attribut**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) Struktur, die einen vordefinierten Datentyp enthält, der sich auf eine Authentifizierungs Sitzung bezieht.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="4ff5f-105">Attribute werden verwendet, um Informationen zwischen EAP-Methoden und Supplicants oder zwischen EAP-Methoden und Authentifikatoren zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="4ff5f-106">Peer-und Authenticator-Implementierungen einer EAP-Methode können diese Attribute über ein Netzwerk austauschen.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="4ff5f-107">Eine komplette Liste der unterstützten Attributtypen wird im Thema [**EAP \_ - \_ Attributtyp**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="4ff5f-108">Von Supplicants verbrauchte Attribute</span><span class="sxs-lookup"><span data-stu-id="4ff5f-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="4ff5f-109">Die folgenden Attributtypen werden von 802.1 x-Supplicants genutzt.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="4ff5f-110">**eatvendorspecific**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="4ff5f-111">Die folgenden Attributtypen werden von PPP-Client Supplicants genutzt.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="4ff5f-112">**eatminimal**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-112">**eatMinimum**</span></span>
-   <span data-ttu-id="4ff5f-113">**eateaptlv**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-113">**eatEAPTLV**</span></span>

<span data-ttu-id="4ff5f-114">Die folgenden Attributtypen werden von PPP-Server Supplicants genutzt.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="4ff5f-115">**eatusername**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-115">**eatUserName**</span></span>
-   <span data-ttu-id="4ff5f-116">**eatreplymess**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="4ff5f-117">**eatstate**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-117">**eatState**</span></span>
-   <span data-ttu-id="4ff5f-118">**eatsessiontimeout**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="4ff5f-119">**eateapmessage**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="4ff5f-120">Durch Methoden exportierte Attribute</span><span class="sxs-lookup"><span data-stu-id="4ff5f-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="4ff5f-121">Die folgenden Attributtypen können von EAP-Methoden exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="4ff5f-122">**eatcleartextpassword**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="4ff5f-123">**eatquarantinesoh**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="4ff5f-124">**eatmethodid**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-124">**eatMethodId**</span></span>

<span data-ttu-id="4ff5f-125">Der folgende Attributtyp wird von EAP-TLS ( [Transport Level Security](/previous-versions/windows/embedded/ms885336(v=msdn.10)) )-Methoden (EAP-TLS) exportiert.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="4ff5f-126">**eatcertifialisieoid**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-126">**eatCertificateOID**</span></span>

<span data-ttu-id="4ff5f-127">Die folgenden Attributtypen werden von der [Microsoft Challenge Handshake Authentication Protocol Version 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2)-Methode exportiert.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="4ff5f-128">**eatusername**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-128">**eatUserName**</span></span>
-   <span data-ttu-id="4ff5f-129">**eatkredentialschge**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="4ff5f-130">Der folgende Attributtyp wird von Netzwerk Richtlinien Server (Network Policy Server, NPS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="4ff5f-131">**eatcertifialisieoid**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-131">**eatCertificateOID**</span></span>

<span data-ttu-id="4ff5f-132">Die folgenden Attributtypen werden von den [PAP-Methoden (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) exportiert.</span><span class="sxs-lookup"><span data-stu-id="4ff5f-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="4ff5f-133">**eatusername**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-133">**eatUserName**</span></span>
-   <span data-ttu-id="4ff5f-134">**eatapapembeddebug-ID**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="4ff5f-135">**eatpinapfastroamedsession**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="4ff5f-136">**eatquarantinesoh**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ff5f-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ff5f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ff5f-138">**EAP- \_ Attribut**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="4ff5f-139">**EAP \_ - \_ Attributtyp**</span><span class="sxs-lookup"><span data-stu-id="4ff5f-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 