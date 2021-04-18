---
description: Windows-Authentifizierungs Pakete stellen Authentifizierungsdienste bereit, indem Paket spezifische Funktionen für die LsaLogonUser-und lsacallauthenticationpackage-Funktionen implementiert werden, die von der LSA bereitgestellt werden.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows-Authentifizierungs Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525844"
---
# <a name="windows-authentication-packages"></a>Windows-Authentifizierungs Pakete

Windows-Authentifizierungs Pakete stellen Authentifizierungsdienste bereit, indem Paket spezifische Funktionen für die [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) -und [**lsacallauthenticationpackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) -Funktionen implementiert werden, die von der LSA bereitgestellt werden.

MSV1 \_ 0 ist ein Beispiel für ein Windows- [*Authentifizierungs Paket*](../secgloss/a-gly.md). Das \_ Paket MSV1 0 akzeptiert einen Benutzernamen und ein [](../secgloss/h-gly.md) Hash Kennwort, das in der [*Security Accounts Manager*](../secgloss/s-gly.md) (Sam)-Datenbank nachgeschlagen ist. Abhängig von den Ergebnissen der Suche \_ akzeptiert das Authentifizierungs Paket MSV1 0 den Authentifizierungs Versuch oder lehnt ihn ab.

Eine Liste der Unterstützungsfunktionen, die von der LSA zur Verwendung durch Windows-Authentifizierungs Pakete bereitgestellt werden, die Systemdienste erfordern, finden Sie unter [LSA Functions called by Authentication Packages](authentication-functions.md).

Windows-Authentifizierungs Pakete müssen eine Reihe von Funktionen implementieren, die von der LSA aufgerufen werden. Eine umfassende Liste der Funktionen finden Sie unter [von Authentifizierungs Paketen implementierte Funktionen](authentication-functions.md).

 

 
