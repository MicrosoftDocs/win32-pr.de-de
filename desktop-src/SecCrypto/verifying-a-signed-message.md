---
description: Mit diesen Schritten wird die Signatur der signierten Daten überprüft.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Überprüfen einer signierten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366165"
---
# <a name="verifying-a-signed-message"></a>Überprüfen einer signierten Nachricht

Mit diesen Schritten wird die Signatur der signierten Daten überprüft. In der folgenden Abbildung werden die einzelnen Aufgaben dargestellt, die durchgeführt werden müssen, wie in der nachfolgenden Liste gezeigt.

![Überprüfen einer signierten Nachricht](images/verifmsg.png)

**So überprüfen Sie die Signatur einer signierten Nachricht**

1.  Einen Zeiger auf die signierte Nachricht erhalten.
2.  Öffnen Sie einen [*Zertifikat Speicher*](../secgloss/c-gly.md).
3.  Verwenden Sie die in der Nachricht enthaltene Signatur Geber-ID, um das Zertifikat des Absenders zu erhalten und ein Handle für seinen [*öffentlichen Schlüssel*](../secgloss/p-gly.md)zu erhalten.

    Als Alternative zu den Schritten 2 und 3 können Sie das in der Nachricht enthaltene Zertifikat verwenden, um den öffentlichen Schlüssel des Signatur Gebers abzurufen.

4.  Entschlüsseln Sie die digitale Signatur mithilfe des öffentlichen Schlüssels des Signatur Gebers, und erzeugen Sie den ursprünglichen Digest der Daten in der Nachricht.
5.  Verwenden Sie den in der Nachricht enthaltenen Hash Algorithmus, um einen [*Hashwert*](../secgloss/h-gly.md) für die in der Nachricht enthaltenen Daten zu erhalten, wodurch ein neuer Digest ergibt.
6.  Vergleichen Sie den Digest, der aus der Nachricht abgerufen wurde, mit dem neuen soeben erstellten Digest.
7.  Wenn die beiden Digests Stimmen, wird die Signatur überprüft. Dies bedeutet, dass der [*private Schlüssel*](../secgloss/p-gly.md) , der zum Signieren der Daten verwendet wurde, mit dem öffentlichen Schlüssel übereinstimmt, der nur zum Entschlüsseln der Signatur verwendet wurde, und dass die Daten seit der Signierung der Daten nicht geändert wurden.

    Wenn die beiden Digests nicht stimmen, wird die Signatur nicht überprüft, und entweder Stimmen die privaten/öffentlichen Schlüssel nicht ab, oder die Daten wurden seit der Signierung der Daten geändert.

Eine einzelne Funktion ( [**cryptverifymessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)) kann zum Überprüfen einer Signatur verwendet werden, wie im folgenden Verfahren gezeigt.

**So überprüfen Sie eine signierte Nachricht**

1.  Einen Zeiger auf die signierte Nachricht erhalten.
2.  Gibt die Größe der signierten Nachricht an.
3.  Erhalten Sie ein Handle für einen Kryptografieanbieter.
4.  Initialisieren Sie die " [**crypt \_ Verify \_ Message \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) "-Struktur.
5.  Um die Signatur zu überprüfen, können Sie [**cryptverifymessagesignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) aufrufen.

Code, der diese Prozedur implementiert, ist im [Beispiel C-Programm: Signieren einer Nachricht und Überprüfen einer Nachrichten Signatur](example-c-program-signing-a-message-and-verifying-a-message-signature.md)enthalten.

 

 
