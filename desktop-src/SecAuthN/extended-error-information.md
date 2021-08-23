---
description: Einige Sicherheitspakete unterstützen erweiterte Fehlermeldungen, die es den Seiten eines Kommunikationslinks ermöglichen, alle Gründe für einen Fehler zu kommunizieren.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Erweiterte Fehlerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd93de1691a01802f65397abb1607612f5b7e61a311c9f801854a00c1ab4f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008218"
---
# <a name="extended-error-information"></a>Erweiterte Fehlerinformationen

Einige [*Sicherheitspakete unterstützen*](/windows/desktop/SecGloss/s-gly) erweiterte Fehlermeldungen, die es den Seiten eines Kommunikationslinks ermöglichen, alle Gründe für einen Fehler zu kommunizieren. Beispielsweise kann das [*Kerberos-Protokoll*](/windows/desktop/SecGloss/k-gly) aufgrund einer Zeitabweichung zwischen dem Zeitpunkt der Anforderung eines Kerberos-Tickets und dem Zeitpunkt der Ticketausgabe fehlschlagen. Mit Informationen aus zurückgegebenen erweiterten Fehlerinformationen kann ein Client seine Uhr neusynchronisieren und eine neue Verbindungsmeldung generieren.

Ein Sicherheitspaket, das das FLAG SECPKG FLAG EXTENDED ERROR im \_ \_ \_ **fCapabilities-Member** einer [**SecPkgInfo-Struktur**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) angibt, dass das Sicherheitspaket erweiterte Fehlermeldungen unterstützt.

Clientanwendungen, die erweiterte Fehlermeldungen erfordern, geben das ISC \_ REQ \_ EXTENDED ERROR-Flag \_ an, wenn die [**InitializeSecurityContext (General)-Funktion aufgerufen**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) wird. Serveranwendungen, die erweiterte Fehlermeldungen erfordern, legen das ASC \_ REQ \_ EXTENDED ERROR-Flag \_ fest, wenn [**AcceptSecurityContext (Allgemein) aufgerufen wird.**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

 

 
