---
description: Listet die von Den Zertifikatdiensten unterstützten Zertifikatformate auf.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Unterstützte Zertifikatformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ae0c4d638e957df5ddcf251ca64578a67a58b98890401c68593dd7a12c3952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897631"
---
# <a name="supported-certificate-formats"></a>Unterstützte Zertifikatformate

Zertifikatdienste können die folgenden Arten von Zertifikaten ausstellen.



| Begriff                                                                                                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) Version 3 SSL-kompatibles Clientauthentifizierungszertifikat<br/> | Dieses Clientauthentifizierungszertifikat identifiziert einen Client und wird von Servern verwendet, um einen Client zu authentifizieren, der Serverzugriff anfordert.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-kompatibles Serverauthentifizierungszertifikat<br/>                                                                                         | Dieses Serverauthentifizierungszertifikat identifiziert einen Server und wird von Clients verwendet, um einen Server zu authentifizieren, auf den der Client zugreifen möchte.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME-Zertifikat*](../secgloss/s-gly.md)<br/>                                                                                                           | Dieses Zertifikat wird von Clients für sichere E-Mails unter dem S/MIME-Protokoll (Secure/Multipurpose Internet Mail Extensions) verwendet.<br/>              |



 

Zusätzlich zu diesen Zertifikaten können Zertifikatdienste auch zum Ausstellen anderer X.509-Zertifikate verwendet werden, indem ein benutzerdefiniertes Richtlinienmodul geschrieben wird.

> [!Note]  
> "Serverauthentifizierungszertifikat" und "Serverzertifikat" sowie "Clientauthentifizierungszertifikat" und "Clientzertifikat" sind austauschbare Begriffe.

 

Darüber hinaus enthalten Zertifikatdienste Zertifikatvorlagen in der Konfiguration der Microsoft-Unternehmenszertifizierungsstelle. Informationen zum Definieren von Zertifikatzwecken finden Sie in der Windows Hilfedokumentation zu Zertifikatvorlagen.

 

 
