---
description: Zeigt, wie eine verschlüsselte Nachricht gesendet wird.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Manueller Sitzungsschlüsselaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c9f7338b40ed1675b2186e478c8c124719b376889ce691d305e246016e0d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425594"
---
# <a name="manual-session-key-exchanges"></a>Manueller Sitzungsschlüsselaustausch

> [!Note]  
> Bei der in diesem Abschnitt beschriebenen Vorgehensweise wird davon ausgegangen, dass [](../secgloss/p-gly.md) die Benutzer (oder CryptoAPI-Clients) bereits über einen eigenen Satz von Paaren aus öffentlichem und privatem Schlüssel verfügen und auch die öffentlichen Schlüssel des jeweils anderen erhalten [*haben.*](../secgloss/p-gly.md)

 

Die folgende Abbildung zeigt, wie Sie dieses Verfahren verwenden, um eine verschlüsselte Nachricht zu senden.

![Senden einer verschlüsselten Nachricht](images/capi04.png)

Dieser Ansatz ist anfällig für mindestens eine gängige Angriffsform. Ein Lauschangriff kann Kopien einer oder mehrere verschlüsselter Nachrichten und der verschlüsselten Schlüssel erhalten. Zu einem späteren Zeitpunkt kann der Lauschangriff dann eine dieser Nachrichten an den Empfänger senden, und der Empfänger kann nicht wissen, dass die Nachricht nicht direkt vom ursprünglichen Absender stammt. Dieses Risiko kann verringert werden, indem alle Nachrichten mit einem Zeitstempel versehen oder Seriennummern verwendet werden.

Die einfachste Möglichkeit, verschlüsselte Nachrichten an einen anderen Benutzer zu senden, ist das Senden der Nachricht, die mit einem zufälligen Sitzungsschlüssel verschlüsselt ist, zusammen mit dem Sitzungsschlüssel, der mit dem öffentlichen Schlüsselaustauschschlüssel des Empfängers [*verschlüsselt ist.*](../secgloss/k-gly.md)

Im Folgenden finden Sie die Schritte zum Senden eines verschlüsselten Sitzungsschlüssels.

**So senden Sie einen verschlüsselten Sitzungsschlüssel**

1.  Erstellen Sie [*mithilfe der*](../secgloss/s-gly.md) [**CryptGenKey-Funktion einen zufälligen Sitzungsschlüssel.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
2.  Verschlüsseln Sie die Nachricht mithilfe des Sitzungsschlüssels. Dieses Verfahren wird unter [Datenverschlüsselung und -entschlüsselung erläutert.](data-encryption-and-decryption.md)
3.  Exportieren Sie den [](../secgloss/k-gly.md) Sitzungsschlüssel mit der [**CryptExportKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) in ein Schlüsselblob, und geben Sie dabei an, dass der Schlüssel mit dem öffentlichen Schlüsselaustauschschlüssel des Zielbenutzers verschlüsselt werden soll.
4.  Senden Sie sowohl die verschlüsselte Nachricht als auch das verschlüsselte Schlüssel-BLOB an den Zielbenutzer.
5.  Der Zielbenutzer importiert das Schlüsselblob mithilfe der [**CryptImportKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) in seinen CSP. Dadurch wird der Sitzungsschlüssel automatisch entschlüsselt, sofern der öffentliche Schlüsselaustauschschlüssel des Zielbenutzers in Schritt 3 angegeben wurde.
6.  Der Zielbenutzer kann die Nachricht dann mithilfe des Sitzungsschlüssels entschlüsseln, indem er das unter Datenverschlüsselung und -entschlüsselung [erläuterte Verfahren verwendet.](data-encryption-and-decryption.md)

 

 
