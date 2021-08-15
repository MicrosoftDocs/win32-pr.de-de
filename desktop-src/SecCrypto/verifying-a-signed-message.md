---
description: Mit diesen Schritten wird die Signatur von signierten Daten überprüft.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Überprüfen einer signierten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7bfdac1b16351d51197a84c15688b0724340af34681312b9cb9865900b8dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970978"
---
# <a name="verifying-a-signed-message"></a>Überprüfen einer signierten Nachricht

Mit diesen Schritten wird die Signatur von signierten Daten überprüft. Die folgende Abbildung zeigt die einzelnen Aufgaben, die ausgeführt werden müssen, wie in der darauf folgenden Liste dargestellt.

![Überprüfen einer signierten Nachricht](images/verifmsg.png)

**So überprüfen Sie die Signatur einer signierten Nachricht**

1.  Abrufen eines Zeigers auf die signierte Nachricht.
2.  Öffnen Sie einen [*Zertifikatspeicher.*](../secgloss/c-gly.md)
3.  Verwenden Sie die in der Nachricht enthaltene Signer-ID, um das Zertifikat des Absenders abzurufen und ein Handle für seinen [*öffentlichen Schlüssel*](../secgloss/p-gly.md)abzurufen.

    Als Alternative zu den Schritten 2 und 3 können Sie das in der Nachricht enthaltene Zertifikat verwenden, um den öffentlichen Schlüssel des Signierers abzurufen.

4.  Entschlüsseln Sie mithilfe des öffentlichen Schlüssels des Signaturgebers die digitale Signatur, und erzeugen Sie den ursprünglichen Digest der Daten in der Nachricht.
5.  Verwenden Sie den in der Nachricht enthaltenen Hashalgorithmus, [*und hashen*](../secgloss/h-gly.md) Sie die in der Nachricht enthaltenen Daten, und erhalten Sie einen neuen Digest.
6.  Vergleichen Sie den aus der Nachricht abgerufenen Digest mit dem soeben erstellten neuen Digest.
7.  Wenn die beiden Digests übereinstimmen, wird die Signatur überprüft. Dies bedeutet, dass der [*private Schlüssel,*](../secgloss/p-gly.md) der zum Signieren der Daten verwendet wurde, mit dem öffentlichen Schlüssel übereinstimmt, der soeben zum Entschlüsseln der Signatur verwendet wurde, und dass sich die Daten seit dem Signieren der Daten nicht geändert haben.

    Wenn die beiden Digests nicht übereinstimmen, wird die Signatur nicht überprüft, und entweder stimmen die privaten/öffentlichen Schlüssel nicht überein, oder die Daten wurden geändert, seit die Daten signiert wurden, oder beides.

Eine einzelne Funktion, [**CryptVerifyMessageSignature,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)kann verwendet werden, um eine Signatur zu überprüfen, wie im folgenden Verfahren gezeigt.

**So überprüfen Sie eine signierte Nachricht**

1.  Abrufen eines Zeigers auf die signierte Nachricht.
2.  Abrufen der Größe der signierten Nachricht.
3.  Abrufen eines Handles für einen Kryptografieanbieter.
4.  Initialisieren Sie die [**CRYPT \_ VERIFY MESSAGE \_ \_ PARA-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para)
5.  Rufen Sie [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) auf, um die Signatur zu überprüfen.

Code, der diese Prozedur implementiert, ist im [C-Beispielprogramm: Signieren einer Nachricht und Überprüfen einer Nachrichtensignatur](example-c-program-signing-a-message-and-verifying-a-message-signature.md)enthalten.

 

 
