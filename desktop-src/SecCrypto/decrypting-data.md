---
description: Zeigt die Schritte zum Entschlüsseln einer verschlüsselten Nachricht an.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Entschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600903d7a3060c83cd7cd0a85e92f96efe4fb0cfa30c2936c5546f71138b6854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875690"
---
# <a name="decrypting-data"></a>Entschlüsseln von Daten

In diesem Abschnitt werden die Schritte zum Entschlüsseln einer verschlüsselten Nachricht beschrieben.

**So entschlüsseln Sie eine verschlüsselte Nachricht**

1.  Abrufen eines Zeigers auf die digital umschlagete Nachricht.
2.  Öffnen Sie einen Zertifikatspeicher.
3.  Rufen Sie aus der Nachricht den Empfängerbezeichner (Meine ID) ab.
4.  Verwenden Sie den Empfängerbezeichner, um das Zertifikat abzurufen.
5.  Abrufen des privaten Schlüssels für das Zertifikat.
6.  Verwenden Sie den privaten Schlüssel, um den symmetrischen Schlüssel (Sitzungsschlüssel) zu entschlüsseln.
7.  Rufen Sie den Verschlüsselungsalgorithmus aus der Nachricht ab.
8.  Entschlüsseln Sie die Daten mithilfe des entschlüsselten Sitzungsschlüssels und des Verschlüsselungsalgorithmus.

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) führt alle Aufgaben zum Entschlüsseln einer Nachricht aus. Die Initialisierung von Strukturen und anderen Daten ist jedoch weiterhin erforderlich.

**So entschlüsseln Sie Daten mit CryptDecryptMessage**

1.  Abrufen eines Zeigers auf das verschlüsselte BLOB.
2.  Öffnen Sie einen Zertifikatspeicher.
3.  Erstellen Sie ein Zertifikatspeicherarray.
4.  Initialisieren Sie die [**CRYPT \_ DECRYPT MESSAGE \_ \_ PARA-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)
5.  Rufen Sie [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) auf, um die in der Nachricht enthaltenen Daten zu entschlüsseln.

[C-Beispielprogramm: Die Verwendung von CryptEncryptMessage und CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementiert die gerade vorgestellte Prozedur. Kommentare zeigen, welche Codeelemente die einzelnen Schritte in der Prozedur ausführen. Ausführliche Informationen zur Funktion finden Sie unter [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)und details zur Datenstruktur unter [**CRYPT \_ DECRYPT MESSAGE \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 



