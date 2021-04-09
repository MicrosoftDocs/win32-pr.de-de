---
title: Security Support Provider (SSPs)
description: Ab Windows 2000 unterstützt RPC eine Vielzahl von Sicherheitsanbietern und-Paketen.
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102230"
---
# <a name="security-support-providers-ssps"></a>Security Support Provider (SSPs)

Ab Windows 2000 unterstützt RPC eine Vielzahl von Sicherheitsanbietern und-Paketen. Dazu gehören:

-   **Sicherheitspaket für das Kerberos-Protokoll.** Das Kerberos V5-Protokoll ist ein Sicherheitspaket nach Industriestandard. Er verwendet vollständigen Prinzipal Namen.
-   **Schannel SSP.** Dieser SSP implementiert das Microsoft Unified Protocol Provider-Sicherheitspaket, das SSL, private Kommunikationstechnologie (PCT) und Transport Level Security (TLS) in einem Sicherheitspaket vereinheitlicht. Er erkennt msstd-und fullsic-Prinzipal Namen.
-   **NTLM-Sicherheitspaket.** Dies war das primäre Sicherheitspaket für NTLM-Netzwerke vor Windows 2000.

Außerdem bietet Microsoft RPC einen *Pseudo-SSP* , mit dem Anwendungen zwischen der Verwendung von echten SSPs aushandeln können. Dieser Pseudo-SSP, der als Simple GSS-API Aushandlungs Mechanismus (snego) SSP bezeichnet wird, bietet keine tatsächlichen Authentifizierungs Features. Die einzige Verwendung besteht darin, Anwendungen bei der Auswahl eines echten SSP zu unterstützen. Derzeit können Client-und Serverprogramme den snego SSP verwenden, um zwischen der Verwendung des NTLM-Sicherheitspakets und des Kerberos-Protokoll Sicherheitspakets zu verhandeln. Weitere Informationen zum Auswählen von SSPs finden Sie unter [Authentication-Service-Konstanten](authentication-service-constants.md).

Alle SSPs, die von Microsoft bereitgestellt werden, mit Ausnahme von SChannel, erkennen Anmelde Informationen für die Authentifizierung in dem Formular, das von der [**\_ \_ \_ Identitäts**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) Struktur der SEC-Authentifizierung bereitgestellt wird. Weitere Informationen finden Sie unter Anmelde Informationen für die [Client Authentifizierung](client-authentication-credentials.md). Informationen zur Verwendung spezifischer SSPs finden Sie unter [SSPI-Funktionen](/windows/desktop/SecMgmt/management-functions) und [Verwenden des SChannel-Sicherheits Anbieters](/windows/desktop/SecAuthN/secure-channel) in der Sicherheits Dokumentation des Platform Software Development Kit (SDK).

 

 