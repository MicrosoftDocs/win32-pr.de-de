---
description: Das Windows Betriebssystem unterstützt die Authentifizierung mithilfe von Sicherheitspaketen, die sowohl als Anbieter der Sicherheitsunterstützung als auch als Authentifizierungspakete fungieren.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Anbieter/Authentifizierungspakete für den Sicherheitssupport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62f634d0571eab43652485f8ca1313f78fd157ca202d5d78369552db648de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918339"
---
# <a name="security-support-providerauthentication-packages"></a>Anbieter/Authentifizierungspakete für den Sicherheitssupport

Das Windows Betriebssystem unterstützt die Authentifizierung mithilfe von [*Sicherheitspaketen,*](../secgloss/s-gly.md) die sowohl als Anbieter der [*Sicherheitsunterstützung*](../secgloss/s-gly.md) als auch als [*Authentifizierungspakete*](../secgloss/a-gly.md)fungieren. Sicherheitspakete bieten die Unterstützungsdienste für den Anmeldeprozess eines Windows Authentifizierungspakets sowie Authentifizierungsdienste für Anwendungen, indem sie eine Reihe von Funktionen implementieren, die der [Security Support Provider Interface](sspi.md) (SSPI) zugeordnet sind.

Ein Sicherheitspaket, das als Authentifizierungspaket fungiert und die für [*SSPI*](../secgloss/s-gly.md) erforderlichen Funktionen implementiert, wird als Sicherheitsunterstützungsanbieter/-authentifizierungspaket (SSP/AP) bezeichnet.

Weitere Informationen zu Sicherheitspaketen finden Sie unter [Von Microsoft bereitgestellte SSP-Pakete.](ssp-packages-provided-by-microsoft.md) Informationen zum Entwickeln von benutzerdefinierten SSP/APs finden Sie unter [Benutzerdefinierte Sicherheitspakete.](custom-security-packages.md)

 

 
