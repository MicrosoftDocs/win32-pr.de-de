---
description: Das Windows-Betriebssystem unterstützt die Authentifizierung mithilfe von Sicherheitspaketen, die als Anbieter für Sicherheitsunterstützung und als Authentifizierungs Pakete fungieren.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Anbieter für Sicherheitsunterstützung/Authentifizierungs Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347343"
---
# <a name="security-support-providerauthentication-packages"></a>Anbieter für Sicherheitsunterstützung/Authentifizierungs Pakete

Das Windows-Betriebssystem unterstützt die Authentifizierung mithilfe von [*Sicherheitspaketen*](../secgloss/s-gly.md) , die als [*Anbieter für Sicherheitsunterstützung*](../secgloss/s-gly.md) und als [*Authentifizierungs Pakete*](../secgloss/a-gly.md)fungieren. Sicherheitspakete stellen die Dienst Unterstützungsdienste für den Anmeldeprozess eines Windows-Authentifizierungs Pakets bereit und bieten Authentifizierungsdienste für Anwendungen an, indem Sie eine Reihe von Funktionen implementieren, die der [Security Support Provider-Schnittstelle](sspi.md) (SSPI) zugeordnet sind.

Ein Sicherheitspaket, das als Authentifizierungs Paket fungiert und die von [*SSPI*](../secgloss/s-gly.md) benötigte Funktionalität implementiert, wird als Security Support Provider-/Authentifizierungspaket (SSP/AP) bezeichnet.

Weitere Informationen zu Sicherheitspaketen finden Sie unter [von Microsoft bereitgestellte SSP-Pakete](ssp-packages-provided-by-microsoft.md). Weitere Informationen zum Entwickeln von benutzerdefinierten SSP/APS finden Sie unter [benutzerdefinierte Sicherheitspakete](custom-security-packages.md).

 

 
