---
title: Registrierungs Werte für die System-Wide Sicherheit
description: Registrierungs Werte für die System-Wide Sicherheit
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947577"
---
# <a name="registry-values-for-system-wide-security"></a>Registrierungs Werte für die System-Wide Sicherheit

Es wird nicht empfohlen, die systemweiten Sicherheitseinstellungen zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren. Wenn Sie die systemweiten Sicherheitseinstellungen ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Setting Process-Wide Security](setting-processwide-security.md).

Bestimmte Werte in der Registrierung werden verwendet, um Sicherheitseinstellungen für Anwendungen zu ermitteln, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen. Sie können Dcomcnfg.exe verwenden, um diese Standard Sicherheitseinstellungen für einen Computer zu ändern. Schritt-für-Schritt-Anleitungen, in denen beschrieben wird, wie Sie Dcomcnfg.exe zu diesem Zweck verwenden, finden [Sie unter Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Eine andere Möglichkeit zum Ändern der systemweiten Standardeinstellungen besteht darin, Registrierungs Werte direkt zu bearbeiten. Allerdings verfügen nur Administratoren und das System über Vollzugriff auf den Teil der Registrierung, der die Standardeinstellungen für das systemweite Aufrufen der Sicherheit enthält. Alle anderen Benutzer verfügen nur über Lesezugriff.

Die benannten Werte, die sich auf systemweite Sicherheitsstandards auswirken, lauten wie folgt:

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [Legacyauthenticationlevel](legacyauthenticationlevel.md)
-   [Legacyidentitäts ationlevel](legacyimpersonationlevel.md)
-   [Legacysecurereferences](legacysecurereferences.md)
-   [Srprunningobjectchecks](srprunningobjectchecks.md)
-   [Srpactivateasactivatorchecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen Process-Wide Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




