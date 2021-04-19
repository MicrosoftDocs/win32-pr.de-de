---
description: Einige Sicherheitspakete unterstützen erweiterte Fehlermeldungen, die es den Seiten eines Kommunikations Links ermöglichen, mögliche Ursachen für einen Fehler zu kommunizieren.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Erweiterte Fehlerinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360623"
---
# <a name="extended-error-information"></a>Erweiterte Fehlerinformationen

Einige [*Sicherheitspakete*](/windows/desktop/SecGloss/s-gly) unterstützen erweiterte Fehlermeldungen, die es den Seiten eines Kommunikations Links ermöglichen, mögliche Ursachen für einen Fehler zu kommunizieren. Das [*Kerberos-Protokoll*](/windows/desktop/SecGloss/k-gly) könnte z. b. aufgrund einer Zeit Abweichung zwischen dem Zeitpunkt der Anforderung für ein Kerberos-Ticket und dem Zeitpunkt des Ticket Fehlers fehlschlagen. Mit Informationen aus zurückgegebenen erweiterten Fehlerinformationen kann ein Client seine Uhr neu synchronisieren und eine neue Verbindungs Nachricht generieren.

Ein Sicherheitspaket, das das \_ Flag erweiterter Fehler für das secpkg-Flag \_ \_ im **ffunktionsmember** einer [**secpkginfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) -Struktur festlegt, gibt an, dass das Sicherheitspaket Erweiterte Fehlermeldungen unterstützt.

Client Anwendungen, die Erweiterte Fehlermeldungen erfordern, geben \_ \_ \_ beim Aufrufen der Funktion [**InitializeSecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) das Flag "ISC req Extended Error" an. Server Anwendungen, die Erweiterte Fehlermeldungen erfordern, legen \_ \_ beim Aufrufen von "Accept- \_ [**SecurityContext (allgemein)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)" das Flag "ASC req Extended Error" fest.

 

 
