---
description: Zeigt, wie eine verschlüsselte Nachricht gesendet wird.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Manueller Austausch von Sitzungs Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556173"
---
# <a name="manual-session-key-exchanges"></a>Manueller Austausch von Sitzungs Schlüsseln

> [!Note]  
> Bei dem in diesem Abschnitt beschriebenen Verfahren wird davon ausgegangen, dass die Benutzer (oder CryptoAPI-Clients) bereits über einen eigenen Satz von [*öffentlichen/privaten Schlüsselpaaren*](../secgloss/p-gly.md) verfügen und auch die [*öffentlichen Schlüssel*](../secgloss/p-gly.md)der anderen abgerufen haben.

 

In der folgenden Abbildung wird gezeigt, wie Sie mit diesem Verfahren eine verschlüsselte Nachricht senden.

![Senden einer verschlüsselten Nachricht](images/capi04.png)

Diese Vorgehensweise ist anfällig für mindestens eine gängige Angriffs Form. Ein eavesdroppergerät kann Kopien von mindestens einer verschlüsselten Nachricht und den verschlüsselten Schlüsseln abrufen. Zu einem späteren Zeitpunkt kann der eavesdropperdienst eine dieser Nachrichten an den Empfänger senden, und der Empfänger hat keine Möglichkeit zu wissen, dass die Nachricht nicht direkt vom ursprünglichen Absender stammt. Dieses Risiko kann durch ein Zeitstempel aller Nachrichten oder durch die Verwendung von Seriennummern verringert werden.

Die einfachste Möglichkeit zum Senden verschlüsselter Nachrichten an einen anderen Benutzer besteht darin, die Nachricht, die mit einem zufälligen Sitzungsschlüssel verschlüsselt ist, zusammen mit dem Sitzungsschlüssel zu senden, der mit dem [*öffentlichen Schlüsselaustausch*](../secgloss/k-gly.md)Schlüssel des Empfängers verschlüsselt ist

Im folgenden werden die Schritte zum Senden eines verschlüsselten Sitzungsschlüssels beschrieben.

**So senden Sie einen verschlüsselten Sitzungsschlüssel**

1.  Erstellen Sie einen zufälligen [*Sitzungsschlüssel*](../secgloss/s-gly.md) mithilfe der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion.
2.  Verschlüsseln Sie die Nachricht mit dem Sitzungsschlüssel. Dieses Verfahren wird unter [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md)erläutert.
3.  Exportieren Sie den Sitzungsschlüssel in ein [*Schlüssel-BLOB*](../secgloss/k-gly.md) mit der [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion, und geben Sie dabei an, dass der Schlüssel mit dem öffentlichen Schlüsselaustausch Schlüssel des Ziel Benutzers verschlüsselt werden soll.
4.  Senden Sie sowohl die verschlüsselte Nachricht als auch das verschlüsselte Schlüsselblob an den Ziel Benutzer.
5.  Der Ziel Benutzer importiert das Schlüsselblob mithilfe der [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) -Funktion in seinen CSP. Dadurch wird der Sitzungsschlüssel automatisch entschlüsselt, sofern der öffentliche Schlüssel für den Schlüsselaustausch des Ziel Benutzers in Schritt 3 angegeben wurde.
6.  Der Ziel Benutzer kann die Nachricht anschließend mithilfe des Sitzungsschlüssels entschlüsseln. Befolgen Sie hierzu das unter [Datenverschlüsselung und Entschlüsselung](data-encryption-and-decryption.md)beschriebene Verfahren.

 

 
