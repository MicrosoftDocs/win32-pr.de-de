---
title: Sicherheitsanmeldeinformationen
description: Sicherheits Anmelde Informationen sind ein Beleg dafür, dass eine kommunizierende Partei über das verfügt, das verwendet werden kann, um ein Sicherheits Token zu erstellen oder abzurufen.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Sicherheits Anmelde Informationen Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106342174"
---
# <a name="security-credentials"></a><span data-ttu-id="7fa2b-106">Sicherheitsanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="7fa2b-106">Security Credentials</span></span>

<span data-ttu-id="7fa2b-107">Sicherheits Anmelde Informationen sind ein Beleg dafür, dass eine kommunizierende Partei über das verfügt, das verwendet werden kann, um ein Sicherheits Token zu erstellen oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="7fa2b-108">Daher sind Anmelde Informationen in der Regel länger als Sicherheits Token, und ein Sicherheits Token kann als Lauf Zeit Darstellung der Sicherheits Anmelde Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="7fa2b-109">Beispiele für Anmelde Informationen sind ein Computer Zertifikat, das zur Laufzeit in ein X. 509-Sicherheits Token konvertiert werden kann, oder ein Benutzername/Kennwort-Paar für eine Domäne (das zum Abrufen eines Kerberos-Sicherheits Tokens verwendet werden kann).</span><span class="sxs-lookup"><span data-stu-id="7fa2b-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="7fa2b-110">Anmelde Informationen werden als Teil der [Sicherheits Bindungen](security-bindings.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="7fa2b-111">Die folgenden API-Elemente werden mit Sicherheits Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="7fa2b-112">Rückruf</span><span class="sxs-lookup"><span data-stu-id="7fa2b-112">Callback</span></span>                                                                  | <span data-ttu-id="7fa2b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fa2b-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="7fa2b-114">**WS \_ get \_ CERT- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="7fa2b-115">Stellt ein Zertifikat für die Security Runtime bereit.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="7fa2b-116">**WS \_ Validate \_ password \_ Callback**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="7fa2b-117">Überprüft ein paar aus Benutzername und Kennwort auf Empfängerseite.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="7fa2b-118">Enumeration</span><span class="sxs-lookup"><span data-stu-id="7fa2b-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="7fa2b-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fa2b-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="7fa2b-120">**WS \_ CERT-Anmelde \_ \_ Informationstyp**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="7fa2b-121">Der Typ der Zertifikat Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="7fa2b-122">**WS \_ username \_ Credential \_ Type**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="7fa2b-123">Der Typ der Anmelde Informationen für Benutzername und Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="7fa2b-124">**Anmelde \_ \_ \_ \_ \_ Informationstyp der integrierten WS Windows-Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="7fa2b-125">Der Typ der Anmelde Informationen für die integrierte Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="7fa2b-126">Struktur</span><span class="sxs-lookup"><span data-stu-id="7fa2b-126">Structure</span></span>                                                                                                   | <span data-ttu-id="7fa2b-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fa2b-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fa2b-128">**WS CERT-Anmelde Informationen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="7fa2b-129">Der abstrakte Basistyp für alle Typen von Zertifikat Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="7fa2b-130">**WS \_ Custom \_ CERT \_ Credential**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="7fa2b-131">Der Typ zum Angeben von Zertifikat Anmelde Informationen, die von einem Rückruf an die Anwendung bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="7fa2b-132">**WS-Standard Anmelde Informationen für die \_ \_ \_ integrierte Windows \_ \_ -Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="7fa2b-133">Geben Sie ein, um die Anmelde Informationen für die integrierte Windows-Authentifizierung basierend auf dem aktuellen Thread Token bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="7fa2b-134">**WS-nicht transparente Anmelde Informationen für die \_ \_ \_ integrierte Windows \_ \_ -Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="7fa2b-135">Typ für die Bereitstellung von Anmelde Informationen für die integrierte Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="7fa2b-136">**WS \_ String \_ username \_ Credential**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="7fa2b-137">Der Typ, der ein Benutzername/Kennwort-Paar als Zeichen folgen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="7fa2b-138">**WS \_ String \_ Windows \_ Integrated \_ auth \_ Credential**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="7fa2b-139">Typ zum Bereitstellen von Windows-Anmelde Informationen als Benutzername, Kennwort und Domänen Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="7fa2b-140">**WS-Antragsteller \_ \_ Name \_ CERT \_ Credential**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="7fa2b-141">Der Typ zum Angeben von Zertifikat Anmelde Informationen mit dem Antragsteller Namen des Zertifikats, dem Speicherort und dem Speicher Namen.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="7fa2b-142">**WS \_ Thumbprint \_ CERT \_ Credential**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="7fa2b-143">Der Typ zum Angeben von Zertifikat Anmelde Informationen unter Verwendung des Fingerabdrucks des Zertifikats, des Speicher Orts und des Speicher namens.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="7fa2b-144">**WS \_ username \_ Credential**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="7fa2b-145">Der abstrakte Basistyp für alle Anmelde Informationen für Benutzername und Kennwort.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="7fa2b-146">**Anmelde Informationen für die integrierte WS Windows-Authentifizierung \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7fa2b-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="7fa2b-147">Der abstrakte Basistyp für alle Anmelde Informationstypen, die mit der integrierten Windows-Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fa2b-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 




