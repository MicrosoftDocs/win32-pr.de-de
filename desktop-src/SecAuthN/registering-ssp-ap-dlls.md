---
description: Nachdem Sie eine SSP/AP DLL (Security Support Provider/Authentication Package Dynamic Link Library) mit einem oder mehrere benutzerdefinierten Sicherheitspaketen entwickelt haben, müssen Sie sie registrieren.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrieren von SSP/AP-DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6405dc5ddce32ad5e4d87ed44f9344240b491fdc0ea789c30d5475ac6e73aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919500"
---
# <a name="registering-sspap-dlls"></a>Registrieren von SSP/AP-DLLs

Nachdem Sie ein [*Authentifizierungspaket*](../secgloss/s-gly.md)für den Sicherheitsunterstützungsanbieter entwickelt haben, das eine / [](../secgloss/a-gly.md) Dynamic Link Library (SSP/AP DLL) mit mindestens einem benutzerdefinierten Sicherheitspaket enthält, müssen Sie es [](../secgloss/s-gly.md)registrieren. Fügen Sie dazu den Daten des folgenden Registrierungswerts den Namen Ihrer benutzerdefinierten SSP/AP-DLL hinzu:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Lsa** \\ **Security Packages**

Die Daten für diesen Registrierungswert sind eine Liste der Namen von SSP/AP-DLLs ohne die Erweiterung ".dll". Der Datentyp für diese Liste ist **REG \_ MULTI \_ SZ,** sodass zwischen jedem DLL-Namen in der Liste ein NULL-Zeichen (' \\ 0' ) enthalten sein muss.

In der Regel werden SSP/AP-DLLs im Verzeichnis %systemroot%/system32 gespeichert. Wenn dies der Pfad zu Ihrer benutzerdefinierten SSP/AP-DLL ist, schließen Sie den Pfad nicht als Teil des DLL-Namens ein. Wenn sich die DLL jedoch in einem anderen Pfad befindet, schließen Sie den vollständigen Pfad zur DLL in den Namen ein.

Bei jedem Systemstart lädt das LSA die SSP/AP-DLLs in dieser Liste und führt die in [Initialisierung im LSA-Modus beschriebene Initialisierungssequenz aus.](lsa-mode-initialization.md)

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registrieren eines benutzerdefinierten Sicherheitspakets als TLS-Standard-SSP

Nachdem Sie einen benutzerdefinierten TLS-Sicherheitssupportanbieter entwickelt und wie oben beschrieben registriert haben, müssen Sie ihn auch als "Tls-Standard-SSP" registrieren. Füllen Sie dazu den Paketnamen Ihres benutzerdefinierten SSP mit den Daten des folgenden Registrierungswerts auf:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Lsa** \\ **Standard TLS SSP**

Die Daten für diesen Registrierungswert sind der Paketname von SSP, nicht der DLL-Name. Der Datentyp dafür ist **REG \_ SZ.**

Benutzermodusanwendungen, die "Standard-TLS-SSP" verwenden, verwenden die hier registrierte Standardeinstellung. Kernelmodusanwendungen oder Benutzermodusanwendungen, die "Microsoft Unified Security Protocol Provider" oder andere spezifische TLS-SSP-Namen verwenden, sind von dieser Änderung nicht beeinflussen.

> [!Note]  
> Diese Registrierungsinformationen beziehen sich nur auf SSP-/AP-DLLs. Informationen zum Registrieren von Sicherheitssupportanbietern (Security Support Providers, SSPs) finden Sie unter Schreiben und [Installieren eines Sicherheitssupportanbieters.](writing-and-installing-a-security-support-provider.md) Informationen zu den Unterschieden zwischen SSP/AP- und SSP-DLLs finden Sie unter [SSP/APs im Vergleich zu SSPs.](ssp-aps-versus-ssps.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Registrieren und Installieren eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
