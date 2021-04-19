---
description: Cryptographic Message Syntax (CMS), abgeleitet von PKCS \# 7 Version 1,5, ist die Syntax, die zum Hashen, digitalen Signieren, authentifizieren und verschlüsseln beliebiger Nachrichten verwendet wird.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: CMS-Ergänzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372959"
---
# <a name="cms-additions"></a>CMS-Ergänzungen

Cryptographic Message Syntax (CMS), abgeleitet von PKCS \# 7 Version 1,5, ist die Syntax, die zum [*Hashen*](../secgloss/h-gly.md), [*digitalen Signieren*](../secgloss/d-gly.md), authentifizieren und verschlüsseln beliebiger Nachrichten verwendet wird. Wenn möglich, wird die Abwärtskompatibilität beibehalten. Es wurden jedoch Änderungen vorgenommen, um Attribut Zertifikat Übertragung und Schlüssel Übereinstimmungs Verfahren für die Schlüsselverwaltung zu ermöglichen. CMS ermöglicht mehrere Kapselung, sodass ein Kapselungs Umschlag in einen anderen geschachtelt werden kann. Außerdem kann eine Partei zuvor gekapselte Daten digital signieren. beliebige Attribute, z. b. die Signatur Zeit, können zusammen mit dem Nachrichten Inhalt signiert werden. das-Attribut und das-Attribut, wie z. b. [*countersignaturen*](../secgloss/c-gly.md), können einer Signatur zugeordnet werden. CMS kann eine Vielzahl von Architekturen für die Zertifikat basierte Schlüsselverwaltung unterstützen.

Um zusätzliche CMS-Funktionen zu unterstützen, wurden den zugrunde liegenden Datenstrukturen neue Felder zugewiesen. Neue Flags und Parameterwerte wurden ebenfalls hinzugefügt. Alle Datenstrukturen und alle APIs, die CMS verwenden, sind 100 Prozent abwärts kompatibel mit PKCS \# 7, Version 1,5.

Zu den Ergänzungen zählen eingeschlossene [Daten Ergänzungen](enveloped-data-additions.md) und [signierte Daten Ergänzungen](signed-data-additions.md).

 

 
