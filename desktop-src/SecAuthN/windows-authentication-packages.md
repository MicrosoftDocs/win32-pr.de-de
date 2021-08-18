---
description: Windows Authentifizierungspakete stellen Authentifizierungsdienste bereit, indem paketspezifische Funktionen für die LsaLogonUser- und LsaCallAuthenticationPackage-Funktionen implementiert werden, die vom LSA bereitgestellt werden.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Authentifizierungspakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915079"
---
# <a name="windows-authentication-packages"></a>Windows Authentifizierungspakete

Windows Authentifizierungspakete stellen Authentifizierungsdienste bereit, indem paketspezifische Funktionen für die funktionen [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) und [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) implementiert werden, die vom LSA bereitgestellt werden.

MSV1 \_ 0 ist ein Beispiel für ein Windows [*Authentifizierungspaket.*](../secgloss/a-gly.md) Das MSV1 \_ 0-Paket akzeptiert einen Benutzernamen und ein Hashkennwort, das in der SAM-Datenbank [*(Security Accounts Manager)*](../secgloss/s-gly.md) gesucht wird. [](../secgloss/h-gly.md) Abhängig von den Ergebnissen der Suche akzeptiert oder lehnt das MSV1 \_ 0-Authentifizierungspaket den Authentifizierungsversuch ab.

Eine Liste der Vom LSA zur Verwendung durch Windows Authentifizierungspakete, die Systemdienste erfordern, bietet, finden Sie unter [Von Authentifizierungspaketen aufgerufene LSA-Funktionen.](authentication-functions.md)

Windows Authentifizierungspakete müssen eine Reihe von Funktionen implementieren, die vom LSA aufgerufen werden. Eine vollständige Liste der Funktionen finden Sie unter [Von Authentifizierungspaketen implementierte Funktionen.](authentication-functions.md)

 

 
