---
description: Cryptographic Message Syntax (CMS), abgeleitet von PKCS 7 Version 1.5, ist die Syntax, die zum Hashen, digitalen Signieren, Authentifizieren und Verschlüsseln beliebiger Nachrichten \# verwendet wird.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: CMS-Ergänzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce7c54867c1ee2a603e37751bf43a0abc65cee670c4a1fc994c9ace3f3404bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876960"
---
# <a name="cms-additions"></a>CMS-Ergänzungen

Cryptographic Message Syntax (CMS), abgeleitet von PKCS 7 Version \# 1.5, ist die Syntax, die zum Hashen, [*digitalen*](../secgloss/d-gly.md)Signieren, Authentifizieren und Verschlüsseln beliebiger Nachrichten verwendet wird. [](../secgloss/h-gly.md) Nach Möglichkeit wird die Abwärtskompatibilität beibehalten. Es wurden jedoch Änderungen vorgenommen, um Die Attributzertifikatübertragung und Schlüsselvereinbarungstechniken für die Schlüsselverwaltung zu bieten. CMS ermöglicht mehrere Kapselungen, sodass ein Kapselungsumschlag in einem anderen geschachtelt werden kann. Außerdem kann eine Partei zuvor gekapselte Daten digital signieren. beliebige Attribute, z. B. die Signierungszeit, können zusammen mit dem Nachrichteninhalt signiert werden. - und -Attribute, z. B. [*Gegensignaturen,*](../secgloss/c-gly.md)können einer Signatur zugeordnet werden. CMS kann eine Vielzahl von Architekturen für die zertifikatbasierte Schlüsselverwaltung unterstützen.

Um zusätzliche CMS-Funktionen zu unterstützen, wurden zugrunde liegende Datenstrukturen neue Felder erhalten. Neue Flags und Parameterwerte wurden ebenfalls hinzugefügt. Alle Datenstrukturen und alle APIs, die CMS verwenden, sind zu 100 Prozent abwärtskompatibel mit PKCS \# 7 Version 1.5.

Zu den Ergänzungen gehören [Umschlagdatener additionen](enveloped-data-additions.md) und [Signierte Datener additionen.](signed-data-additions.md)

 

 
