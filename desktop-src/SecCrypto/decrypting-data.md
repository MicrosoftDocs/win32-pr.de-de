---
description: Zeigt die Schritte zum Entschlüsseln einer verschlüsselten Nachricht an.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Entschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350158"
---
# <a name="decrypting-data"></a>Entschlüsseln von Daten

Dieser Abschnitt enthält die Schritte zum Entschlüsseln einer verschlüsselten Nachricht.

**So entschlüsseln Sie eine verschlüsselte Nachricht**

1.  Einen Zeiger auf die Digital eingeschlossene Nachricht erhalten.
2.  Öffnen Sie einen Zertifikat Speicher.
3.  Rufen Sie in der Meldung den Empfänger Bezeichner (meine ID) ab.
4.  Verwenden Sie den Empfänger Bezeichner, um das Zertifikat abzurufen.
5.  Den privaten Schlüssel für das Zertifikat erhalten.
6.  Verwenden Sie den privaten Schlüssel, um den symmetrischen (Sitzungs-) Schlüssel zu entschlüsseln.
7.  Rufen Sie den Verschlüsselungsalgorithmus aus der Nachricht ab.
8.  Entschlüsseln Sie die Daten mithilfe des entschlüsselten Sitzungsschlüssels und des Verschlüsselungsalgorithmus.

[**Cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) übernimmt alle Aufgaben zum Entschlüsseln einer Nachricht. die Initialisierung von Strukturen und anderen Daten ist jedoch weiterhin erforderlich.

**So entschlüsseln Sie Daten mithilfe von "cryptdecryptmessage"**

1.  Einen Zeiger auf das verschlüsselte Blob erhalten.
2.  Öffnen Sie einen Zertifikat Speicher.
3.  Erstellen Sie ein Zertifikat Speicher Array.
4.  Initialisieren Sie [**die \_ Meldung "Crypt entschlüsselungsfehlermeldung \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) ".
5.  Nennen Sie [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) , um die in der Nachricht enthaltenen Daten zu entschlüsseln.

[Beispiel für ein C-Programm: die Verwendung von cryptencryptmessage und cryptdecryptmessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementiert die soeben vorgestellte Prozedur. Kommentare zeigen an, welche Code Elemente die einzelnen Schritte in der Prozedur ausführen. Weitere Informationen zur-Funktion finden Sie unter [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage). Weitere Informationen zur Datenstruktur finden Sie unter [**crypt \_ Entschlüsseln der \_ Nachricht \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 



