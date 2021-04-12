---
title: Sicherheit der Anwendungsverzeichnis Partition
description: Das Sicherheits-und Zugriffs Steuerungsmodell für Anwendungsverzeichnis Partitionen ist das gleiche wie bei anderen Partitionen in Active Directory Domain Services.
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- Sicherheits-AD für Anwendungsverzeichnis Partition
- Anwendungsverzeichnis Partitionen AD, Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da4ce1b8d4e3604b8e546d79003f4d3719223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948592"
---
# <a name="application-directory-partition-security"></a>Sicherheit der Anwendungsverzeichnis Partition

Das Sicherheits-und Zugriffs Steuerungsmodell für Anwendungsverzeichnis Partitionen ist das gleiche wie bei anderen Partitionen in Active Directory Domain Services. Normale Benutzer können auf Objekte in einer Anwendungsverzeichnis Partition zugreifen, die den ACLs unterliegen, die für diese Objekte platziert werden. Weitere Informationen finden Sie unter [Steuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Da Anwendungsverzeichnis Partitionen jedoch mehrere Sicherheits Domänen in einem Verzeichnisdienst umfassen können, besteht die Frage, wie Domänen relative bekannte SID-Zeichen folgen Konstanten im [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) der Schema Klasse eines Objekts zum Zeitpunkt der Objekt Erstellung in einer Anwendungsverzeichnis Partition interpretiert werden können. Wenn "da" z. b. auf die Gruppe "Domänen Administratoren" verweist, aber in einer Anwendungsverzeichnis Partition ist nicht bekannt, auf welche Domäne sich die Gruppe "da" bezieht.

Um dieses Problem zu beheben, verfügt das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt einer Anwendungsverzeichnis Partition über ein [**msDS-sdreferencedomain-**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) Attribut, das den Distinguished Name der Referenz Domäne für diese Anwendungsverzeichnis Partition enthält. Das Sicherheitssystem verwendet die angegebene Domäne, um lokale Domänen Verweise für Standard Sicherheits Deskriptoren zu interpretieren, die an in dieser Anwendungsverzeichnis Partition erstellte Objekte angefügt sind. Die Verweis Domäne kann angegeben werden, wenn das **CrossRef** -Objekt für eine Anwendungsverzeichnis Partition erstellt wird. Dies erfordert jedoch, dass ein **CrossRef** -Objekt für die Anwendungsverzeichnis Partition vorab erstellt wird. Wenn keine Verweis Domäne angegeben ist, legt das System die Verweis Domäne automatisch basierend auf einer der folgenden Bedingungen fest:

-   Wenn das übergeordnete Element des Anwendungsverzeichnis-Partitions Objekts eine andere Anwendungsverzeichnis Partition ist, wird das [**msDS-sdreferencedomain-**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) Attribut der übergeordneten Anwendungsverzeichnis Partition für die Verweis Domäne verwendet.
-   Wenn das übergeordnete Objekt eine Domäne ist, wird diese Domäne für die Verweis Domäne verwendet.
-   Wenn kein übergeordnetes Objekt vorhanden ist, wird die Stamm Domäne der Gesamtstruktur für die Verweis Domäne verwendet.

Das **CrossRef** -Attribut kann auch nach dem Erstellen der Partition in die Verweis Domäne geändert werden. Dies wird jedoch nicht empfohlen.

Ein ähnliches Problem tritt auf, wenn eine lokale Gruppe in einer ACL für ein Objekt in einer Anwendungsverzeichnis Partition angegeben wird. In diesem Fall kann das Attribut [**msDS-sdreferencedomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) nicht zum Interpretieren der Verweis Domäne für eine lokale Gruppe verwendet werden. Um dieses Problem zu vermeiden, sollten lokale Gruppen nicht in den ACLs von Anwendungsverzeichnis-Partitions Objekten verwendet werden.

 

 