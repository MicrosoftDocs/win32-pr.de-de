---
title: Sicherheits Bindungen
description: Eine Sicherheitsbindung ist die Spezifikation eines Sicherheits Tokens und teilt der Laufzeit mit, wie Sie ein Sicherheits Token für die Kanal Sicherheit abrufen und verwenden können.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Sicherheitsbindungs-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102562"
---
# <a name="security-bindings"></a><span data-ttu-id="6ae74-106">Sicherheits Bindungen</span><span class="sxs-lookup"><span data-stu-id="6ae74-106">Security Bindings</span></span>

<span data-ttu-id="6ae74-107">Eine Sicherheitsbindung ist die Spezifikation eines Sicherheits Tokens und teilt der Laufzeit mit, wie Sie ein Sicherheits Token für die Kanal Sicherheit abrufen und verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6ae74-107">A security binding is the specification of a security token, and tells the runtime how to obtain and use a security token for channel security.</span></span> <span data-ttu-id="6ae74-108">Das-Sicherheits Token enthält Informationen, die für den Zugriff auf Ressourcen bürgt.</span><span class="sxs-lookup"><span data-stu-id="6ae74-108">The security token contains information that vouches for the right to access resources.</span></span> <span data-ttu-id="6ae74-109">Es kann auch ein zugeordneter kryptografischer Schlüssel zum Durchführen von Signaturen und Verschlüsselung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6ae74-109">It may also have an associated cryptographic key for performing signatures and encryption.</span></span>


<span data-ttu-id="6ae74-110">Jede Sicherheitsbindung enthält eine eigene Auflistung Optionaler [sicherheitsbindungs Einstellungen](security-binding-settings.md) , die auf das Sicherheits Token beschränkt sind, das Sie definiert.</span><span class="sxs-lookup"><span data-stu-id="6ae74-110">Each security binding contains its own collection of optional [security binding settings](security-binding-settings.md) that are scoped to the security token it defines.</span></span> <span data-ttu-id="6ae74-111">Sie enthält auch [Sicherheits Anmelde](security-credentials.md)Informationen, die die Sicherheits Beweise darstellen (z. b. Benutzername und Kennwort oder Zertifikate), die zum Erstellen von Sicherheits Token benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6ae74-111">It also contains [security credentials](security-credentials.md), representing the security evidence (such as username and passwords, or certificates) needed to create security tokens.</span></span>

<span data-ttu-id="6ae74-112">Die folgenden Rückrufe sind Teil der Sicherheitsbindung:</span><span class="sxs-lookup"><span data-stu-id="6ae74-112">The following callbacks are part of the security binding:</span></span>

-   [<span data-ttu-id="6ae74-113">**WS-Überprüfungs- \_ \_ SAML- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="6ae74-113">**WS\_VALIDATE\_SAML\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

<span data-ttu-id="6ae74-114">Die folgenden Enumerationen sind Teil der Sicherheitsbindung:</span><span class="sxs-lookup"><span data-stu-id="6ae74-114">The following enumerations are part of the security binding:</span></span>

-   [<span data-ttu-id="6ae74-115">**WS- \_ Nachrichten \_ Sicherheits \_ Verwendung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-115">**WS\_MESSAGE\_SECURITY\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [<span data-ttu-id="6ae74-116">**WS \_ SAML \_ Authenticator- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="6ae74-116">**WS\_SAML\_AUTHENTICATOR\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [<span data-ttu-id="6ae74-117">**WS \_ - \_ Sicherheits \_ Bindungstyp**</span><span class="sxs-lookup"><span data-stu-id="6ae74-117">**WS\_SECURITY\_BINDING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [<span data-ttu-id="6ae74-118">**Typ des WS- \_ Sicherheits \_ Schlüssel \_ Handles \_**</span><span class="sxs-lookup"><span data-stu-id="6ae74-118">**WS\_SECURITY\_KEY\_HANDLE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

<span data-ttu-id="6ae74-119">Die folgenden Funktionen sind Teil der Sicherheitsbindung:</span><span class="sxs-lookup"><span data-stu-id="6ae74-119">The following functions are part of the security binding:</span></span>

-   [<span data-ttu-id="6ae74-120">**Wscreatexmlsecuritytoken**</span><span class="sxs-lookup"><span data-stu-id="6ae74-120">**WsCreateXmlSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [<span data-ttu-id="6ae74-121">**Wsfreesecuritytoken**</span><span class="sxs-lookup"><span data-stu-id="6ae74-121">**WsFreeSecurityToken**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

<span data-ttu-id="6ae74-122">Die folgenden Strukturen sind Teil der Sicherheitsbindung:</span><span class="sxs-lookup"><span data-stu-id="6ae74-122">The following structures are part of the security binding:</span></span>

-   [<span data-ttu-id="6ae74-123">**WS \_ CAPI \_ asymmetrisches \_ Sicherheits \_ Schlüssel \_ handle**</span><span class="sxs-lookup"><span data-stu-id="6ae74-123">**WS\_CAPI\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [<span data-ttu-id="6ae74-124">**WS- \_ CERT- \_ \_ SAML- \_ Authentifikator mit Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="6ae74-124">**WS\_CERT\_SIGNED\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [<span data-ttu-id="6ae74-125">**WS-HTTP-Header Authentifizierung- \_ \_ \_ \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-125">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [<span data-ttu-id="6ae74-126">**WS- \_ Kerberos- \_ apreq- \_ Nachrichten \_ \_ Sicherheitsbindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-126">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [<span data-ttu-id="6ae74-127">**WS \_ NamedPipe \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-127">**WS\_NAMEDPIPE\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [<span data-ttu-id="6ae74-128">**\_asymmetrischer WS NCrypt- \_ \_ Sicherheits \_ Schlüssel \_ handle**</span><span class="sxs-lookup"><span data-stu-id="6ae74-128">**WS\_NCRYPT\_ASYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [<span data-ttu-id="6ae74-129">**WS \_ - \_ \_ \_ rohschlüssel Handle für symmetrischen Sicherheitsschlüssel \_**</span><span class="sxs-lookup"><span data-stu-id="6ae74-129">**WS\_RAW\_SYMMETRIC\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [<span data-ttu-id="6ae74-130">**WS- \_ SAML- \_ Authentifikator**</span><span class="sxs-lookup"><span data-stu-id="6ae74-130">**WS\_SAML\_AUTHENTICATOR**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [<span data-ttu-id="6ae74-131">**WS \_ SAML \_ Message- \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-131">**WS\_SAML\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [<span data-ttu-id="6ae74-132">**WS- \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-132">**WS\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [<span data-ttu-id="6ae74-133">**WS- \_ Sicherheits \_ Kontext Nachrichten- \_ \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-133">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [<span data-ttu-id="6ae74-134">**WS- \_ Sicherheits \_ Schlüssel \_ handle**</span><span class="sxs-lookup"><span data-stu-id="6ae74-134">**WS\_SECURITY\_KEY\_HANDLE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [<span data-ttu-id="6ae74-135">**WS \_ SSL- \_ Transport \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-135">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [<span data-ttu-id="6ae74-136">**WS \_ TCP- \_ SSPI- \_ Transport \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-136">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [<span data-ttu-id="6ae74-137">**WS \_ username \_ Message- \_ Sicherheits \_ Bindung**</span><span class="sxs-lookup"><span data-stu-id="6ae74-137">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [<span data-ttu-id="6ae74-138">**WS- \_ XML- \_ \_ tokennachrichtensicherheitsbindung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6ae74-138">**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




