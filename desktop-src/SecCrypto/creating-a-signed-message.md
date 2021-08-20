---
description: Stellt die Aufgaben dar, die ausgeführt werden müssen, um eine signierte Nachricht zu erstellen.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Erstellen einer signierten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645509c140168267bf48915f68a884b51dee6e7f5a19b2a153e3fd6ff7d5afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769247"
---
# <a name="creating-a-signed-message"></a>Erstellen einer signierten Nachricht

Die folgende Abbildung zeigt die Aufgaben, die ausgeführt werden müssen, um eine signierte Nachricht zu erstellen. Die Schritte sind im Anschluss an die Abbildung aufgeführt.

![Signieren einer Nachricht](images/signdmsg.png)

**So erstellen Sie eine signierte Nachricht**

1.  Erstellen Sie die Daten (falls erforderlich), und erhalten Sie einen Zeiger darauf.
2.  Öffnen Sie einen [*Zertifikatspeicher,*](../secgloss/c-gly.md) der das Zertifikat des Signierers enthält.
3.  Abrufen des [*privaten Schlüssels*](../secgloss/p-gly.md) für das Zertifikat. Eine Eigenschaft muss für das Zertifikat festgelegt werden, bevor es verwendet wird, um ein Zertifikat an einen bestimmten [*CSP*](../secgloss/c-gly.md)und innerhalb dieses CSP an einen bestimmten privaten Schlüssel zu binden. Dies muss einmal festgelegt werden.
4.  Wählen Sie einen Hashalgorithmus für den Digestvorgang aus. Es wird empfohlen, den Hashalgorithmus an einem konfigurierbaren Speicherort auszuwählen, der anschließend ohne Codeänderungen aktualisiert werden kann.
5.  Senden Sie die Daten über die Hashfunktion, indem Sie den Hashalgorithmus verwenden, um einen [*Hash*](../secgloss/h-gly.md) (Digest) der Daten zu erstellen.
6.  Verschlüsseln Sie den Digest mithilfe des [*privaten Schlüssels,*](../secgloss/p-gly.md) der über die -Eigenschaft des Zertifikats abgerufen wurde, und erstellen Sie die Signatur.
7.  Fügen Sie Folgendes in die signierte Nachricht ein:

    -   Die signierten Daten
    -   Der Hashalgorithmus
    -   Die Signatur
    -   Der Signiererbezeichner (Zertifikataussteller und Seriennummer)
    -   Das Zertifikat des Signierers (optional)

Eine ausführliche Vorgehensweise und ein Beispiel finden Sie unter [Prozedur zum Signieren von Daten](procedure-for-signing-data.md) und [C-Beispielprogramm: Signieren einer Nachricht und Überprüfen einer Nachrichtensignatur.](example-c-program-signing-a-message-and-verifying-a-message-signature.md)

 

 
