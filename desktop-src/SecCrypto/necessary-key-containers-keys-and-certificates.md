---
description: Beispielprogramme in den folgenden Abschnitten führen Vorgänge aus, bei denen öffentlich-private Schlüsselpaare zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen verfügbar sein müssen.
ms.assetid: b03528ff-0170-4dde-ae35-f5c3951d6b1f
title: Erforderliche Schlüsselcontainer, Schlüssel und Zertifikate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee5f86f887050d0d7abe440c89cc9c9444dba26854645d5ad6d16279af91e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992720"
---
# <a name="necessary-key-containers-keys-and-certificates"></a>Erforderliche Schlüsselcontainer, Schlüssel und Zertifikate

Beispielprogramme in den folgenden Abschnitten führen Vorgänge aus, bei denen [*öffentlich-private*](../secgloss/p-gly.md) Schlüsselpaare zum Verschlüsseln und Entschlüsseln von Dateien, Nachrichten und Signaturen verfügbar sein müssen. Viele dieser Programme kompilieren, verknüpfen und werden ausgeführt, führen [](../secgloss/k-gly.md)aber zur Laufzeit zu einem Fehler, ohne dass geeignete Schlüsselcontainer, [*Schlüssel,*](../secgloss/c-gly.md)Zertifikatspeicher und Zertifikate in diesen Speichern vorliegen.

Darüber hinaus müssen einige der Zertifikate im MY-Speicher einige ihrer erweiterten Eigenschaften festgelegt haben.

Sie können den erforderlichen Standardschlüsselcontainer erstellen, indem Sie das Programm im Beispiel [C-Programm: Erstellen](example-c-program-creating-a-key-container-and-generating-keys.md)eines Schlüsselcontainers und Generieren von Schlüsseln ausführen. Beachten Sie, dass bei der Erstellung eines Schlüsselcontainers nicht automatisch Paare aus öffentlichem und privatem Schlüssel generiert werden. Das Beispielprogramm erstellt jedoch sowohl den Schlüsselcontainer als auch die Paare aus öffentlichem und privatem Schlüssel.

Nachdem Paare aus öffentlichem und privatem Schlüssel generiert wurden, können Testzertifikate, die diese Schlüssel verwenden, von einer [*Zertifizierungsstelle (Certification Authority,*](../secgloss/c-gly.md) CA) erhalten werden.

Bei einigen Programmen wird davon ausgegangen, dass Zertifikate mit bestimmten Betreffnamen im MY-Systemspeicher vorhanden sind. Insbesondere suchen mehrere Programme nach Zertifikaten mit den Betreffnamen "Full Test Cert" und "Hortense". Die Betreffnamen für die Zertifikate können im Code so geändert werden, dass sie mit den Betreffnamen von Zertifikaten übereinstimmen, die im MY-Zertifikatspeicher vorhanden sind.

Beim Ausführen des Beispielprogramms in [Beispiel C-Programm:](example-c-program-listing-the-certificates-in-a-store.md) Auflisten der Zertifikate in einem Store werden alle Zertifikate in einem Speicher und alle erweiterten Eigenschaften angezeigt, die für diese Zertifikate festgelegt sind.

 

 
