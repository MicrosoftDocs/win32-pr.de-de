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
# <a name="supported-certificate-formats"></a>Unterstützte Zertifikat Formate

Die Zertifikat Dienste können die folgenden Arten von Zertifikaten ausstellen.



| Begriff                                                                                                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X. 509*](../secgloss/x-gly.md) , Version 3, SSL-kompatibles Client Authentifizierungszertifikat<br/> | Dieses Client Authentifizierungszertifikat identifiziert einen Client und wird von Servern zum Authentifizieren eines Clients verwendet, der Server Zugriffe anfordert.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>SSL-kompatibles X. 509 v3-Server Authentifizierungszertifikat<br/>                                                                                         | Dieses Server Authentifizierungszertifikat identifiziert einen Server und wird von Clients verwendet, um einen Server zu authentifizieren, auf den der Client zugreifen möchte.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME-*](../secgloss/s-gly.md) Zertifikat<br/>                                                                                                           | Dieses Zertifikat wird von Clients für sichere e-Mails unter dem S/MIME (Secure/Multipurpose Internet Mail Extensions)-Protokoll verwendet.<br/>              |



 

Zusätzlich zu diesen Zertifikaten können Zertifikat Dienste auch verwendet werden, um andere X. 509-Zertifikate auszugeben, indem Sie ein benutzerdefiniertes Richtlinien Modul schreiben.

> [!Note]  
> "Server Authentifizierungszertifikat" und "Serverzertifikat" sowie "Client Authentifizierungszertifikat" und "Client Zertifikat" sind austauschbare Begriffe.

 

Außerdem enthalten Zertifikat Dienste Zertifikat Vorlagen in der Konfiguration der Microsoft-Unternehmens Zertifizierungsstelle. In der Windows-Hilfe Dokumentation finden Sie Zertifikat Vorlagen, um zu verstehen, wie Sie Zertifikat Zwecke definieren.

 

 
