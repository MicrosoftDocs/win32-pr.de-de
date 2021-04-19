---
description: Listet die von den Zertifikat Diensten unterstützten Zertifikat Formate auf.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Unterstützte Zertifikat Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357792"
---
# <a name="supported-certificate-formats"></a><span data-ttu-id="328bb-103">Unterstützte Zertifikat Formate</span><span class="sxs-lookup"><span data-stu-id="328bb-103">Supported Certificate Formats</span></span>

<span data-ttu-id="328bb-104">Die Zertifikat Dienste können die folgenden Arten von Zertifikaten ausstellen.</span><span class="sxs-lookup"><span data-stu-id="328bb-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="328bb-105">Begriff</span><span class="sxs-lookup"><span data-stu-id="328bb-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="328bb-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="328bb-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="328bb-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X. 509*](../secgloss/x-gly.md) , Version 3, SSL-kompatibles Client Authentifizierungszertifikat</span><span class="sxs-lookup"><span data-stu-id="328bb-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="328bb-108">Dieses Client Authentifizierungszertifikat identifiziert einen Client und wird von Servern zum Authentifizieren eines Clients verwendet, der Server Zugriffe anfordert.</span><span class="sxs-lookup"><span data-stu-id="328bb-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="328bb-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>SSL-kompatibles X. 509 v3-Server Authentifizierungszertifikat</span><span class="sxs-lookup"><span data-stu-id="328bb-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="328bb-110">Dieses Server Authentifizierungszertifikat identifiziert einen Server und wird von Clients verwendet, um einen Server zu authentifizieren, auf den der Client zugreifen möchte.</span><span class="sxs-lookup"><span data-stu-id="328bb-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="328bb-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME-*](../secgloss/s-gly.md) Zertifikat</span><span class="sxs-lookup"><span data-stu-id="328bb-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="328bb-112">Dieses Zertifikat wird von Clients für sichere e-Mails unter dem S/MIME (Secure/Multipurpose Internet Mail Extensions)-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="328bb-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="328bb-113">Zusätzlich zu diesen Zertifikaten können Zertifikat Dienste auch verwendet werden, um andere X. 509-Zertifikate auszugeben, indem Sie ein benutzerdefiniertes Richtlinien Modul schreiben.</span><span class="sxs-lookup"><span data-stu-id="328bb-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="328bb-114">"Server Authentifizierungszertifikat" und "Serverzertifikat" sowie "Client Authentifizierungszertifikat" und "Client Zertifikat" sind austauschbare Begriffe.</span><span class="sxs-lookup"><span data-stu-id="328bb-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="328bb-115">Außerdem enthalten Zertifikat Dienste Zertifikat Vorlagen in der Konfiguration der Microsoft-Unternehmens Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="328bb-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="328bb-116">In der Windows-Hilfe Dokumentation finden Sie Zertifikat Vorlagen, um zu verstehen, wie Sie Zertifikat Zwecke definieren.</span><span class="sxs-lookup"><span data-stu-id="328bb-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
