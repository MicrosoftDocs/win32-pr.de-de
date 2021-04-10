---
description: Nachdem Sie ein Security Support Provider-/Authentifizierungspaket (Dynamic Link Library, SSP/AP-dll) mit einem oder mehreren benutzerdefinierten Sicherheitspaketen entwickelt haben, müssen Sie diese registrieren.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrieren von SSP/AP-DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756426"
---
# <a name="registering-sspap-dlls"></a>Registrieren von SSP/AP-DLLs

Nach der Entwicklung eines [*Security Support Provider*](../secgloss/s-gly.md) / -[*Authentifizierungs Pakets*](../secgloss/a-gly.md) Dynamic Link Library (SSP/AP dll), das ein oder mehrere benutzerdefinierte [*Sicherheitspakete*](../secgloss/s-gly.md)enthält, müssen Sie diese registrieren. Fügen Sie zu diesem Zweck den Namen Ihrer benutzerdefinierten SSP/AP-dll den Daten des folgenden Registrierungs Werts hinzu:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **Security Packages**

Die Daten für diesen Registrierungs Wert sind eine Liste der Namen von SSP/AP-DLLs ohne die Erweiterung ". dll". Der Datentyp für diese Liste ist **" \_ reg \_ MultiSZ** ", sodass \\ zwischen den einzelnen DLL-Namen in der Liste ein NULL-Zeichen ("0") vorhanden sein muss.

SSP/AP-DLLs werden in der Regel im Verzeichnis "% SystemRoot%/System32" gespeichert. Wenn dies der Pfad zu Ihrer benutzerdefinierten SSP/AP-dll ist, schließen Sie den Pfad nicht als Teil des DLL-namens ein. Wenn sich die dll jedoch in einem anderen Pfad befindet, schließen Sie den gesamten Pfad zur dll in den Namen ein.

Jedes Mal, wenn das System gestartet wird, lädt die LSA die SSP/AP-DLLs in diese Liste und führt die Initialisierungs Sequenz aus, die im [LSA-Modus Initialisierung](lsa-mode-initialization.md)beschrieben wird.

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a>Registrieren eines benutzerdefinierten Sicherheitspakets als Standard-TLS-SSP

Nachdem Sie eine benutzerdefinierte TLS-Security Support Provider entwickelt und wie oben beschrieben registriert haben, müssen Sie Sie auch als "Standard TLS-SSP" registrieren. Füllen Sie hierzu den Paketnamen Ihres benutzerdefinierten SSP mit den Daten des folgenden Registrierungs Werts:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **Standard TLS SSP**

Die Daten für diesen Registrierungs Wert sind der Paketname von SSP, nicht der Name der dll. Der Datentyp hierfür ist **reg \_ SZ**.

Benutzermodusanwendungen, die "Standard-TLS-SSP" verwenden, verwenden den hier registrierten Standard. Kernelmodusanwendungen oder Benutzermodusanwendungen, die "Microsoft Unified Security Protocol Provider" oder andere spezifische TLS-SSP-Namen verwenden, sind von dieser Änderung nicht betroffen.

> [!Note]  
> Diese Registrierungsinformationen beziehen sich ausschließlich auf SSP/AP-dll. Weitere Informationen zum Registrieren von SSPs (Security Support Providers) finden Sie unter [schreiben und Installieren eines Sicherheits Unterstützungs Anbieters](writing-and-installing-a-security-support-provider.md). Informationen zu den Unterschieden zwischen SSP/AP und SSP-DLLs finden Sie unter [SSP/APS im Vergleich zu SSPs](ssp-aps-versus-ssps.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
