---
description: Stellt die Aufgaben dar, die zum Erstellen einer signierten Nachricht durchgeführt werden müssen.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Erstellen einer signierten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216715"
---
# <a name="creating-a-signed-message"></a>Erstellen einer signierten Nachricht

Die folgende Abbildung zeigt die Aufgaben, die zum Erstellen einer signierten Nachricht durchgeführt werden müssen. Die Schritte werden nach der Abbildung aufgeführt.

![Signieren einer Nachricht](images/signdmsg.png)

**So erstellen Sie eine signierte Nachricht**

1.  Erstellen Sie die Daten (falls erforderlich), und rufen Sie einen Zeiger darauf ab.
2.  Öffnen Sie einen [*Zertifikat Speicher*](../secgloss/c-gly.md) , der das Zertifikat des Signatur Gebers enthält.
3.  Den [*privaten Schlüssel*](../secgloss/p-gly.md) für das Zertifikat erhalten. Eine Eigenschaft muss für das Zertifikat festgelegt werden, bevor Sie verwendet werden kann, um ein Zertifikat mit einem bestimmten [*CSP*](../secgloss/c-gly.md)und innerhalb des CSP an einen bestimmten privaten Schlüssel zu binden. Diese muss einmal festgelegt werden.
4.  Wählen Sie einen Hash Algorithmus für den Digest-Vorgang aus. Es wird empfohlen, dass der Hash Algorithmus an einem konfigurierbaren Speicherort ausgewählt wird, der anschließend aktualisiert werden kann, ohne dass Codeänderungen erforderlich sind.
5.  Senden Sie die Daten über die Hash Funktion mithilfe des Hash Algorithmus, und erstellen Sie dadurch einen [*Hash*](../secgloss/h-gly.md) (Digest) der Daten.
6.  Verschlüsseln Sie den Digest mithilfe des [*privaten Schlüssels*](../secgloss/p-gly.md) , der über die-Eigenschaft des Zertifikats abgerufen wurde, und erstellen Sie die Signatur.
7.  Fügen Sie Folgendes in die signierte Nachricht ein:

    -   Die signierten Daten
    -   Der Hash Algorithmus
    -   Die Signatur
    -   Der Signatur Geber Bezeichner (Zertifikat Aussteller und Seriennummer)
    -   Zertifikat des Signatur Gebers (optional)

Ein ausführliches Verfahren und ein Beispiel finden Sie unter Vorgehensweise: [Signieren von Daten](procedure-for-signing-data.md) und [Beispiel-C-Programm: Signieren einer Nachricht und Überprüfen einer Nachrichten Signatur](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
