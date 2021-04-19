---
description: Stellt die Aufgaben dar, die zum Codieren einer Hash Nachricht erforderlich sind.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codieren und Decodieren einer Hash Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91d165634c1ae00a59f2c77b1fc5a36b53dbd96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360733"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codieren und Decodieren einer Hash Nachricht

Hash Daten bestehen aus Inhalten eines beliebigen Typs und einem [*Hash*](../secgloss/h-gly.md) des Inhalts. Sie kann verwendet werden, wenn nur sichergestellt werden muss, dass der Nachrichten Inhalt seit der Hash Erstellung nicht geändert wurde.

Beim Erstellen einer Hash Nachricht können mehrere Hash Algorithmen und mehrere Hashes vorhanden sein. Die folgende Abbildung zeigt die Aufgaben, die zum Codieren einer Hash Nachricht erforderlich sind. Die Prozedur wird in dem Text beschrieben, der der Abbildung folgt.

![Erstellen einer Hash Nachricht](images/hashmsg.png)

**So erstellen Sie eine Hash Nachricht**

1.  Einen Zeiger auf die Daten, für die ein Hashwert erstellt werden soll.
2.  Wählen Sie den zu verwendenden Hash Algorithmus aus.
3.  Fügen Sie die Daten mithilfe des Hash Algorithmus über eine Hash Funktion ein.
4.  Fügen Sie die ursprünglichen Daten ein, die in den Hash Hash eingefügt werden sollen, die Hash Algorithmen und die Hashes in der codierten Nachricht.

Verwenden Sie das folgende Verfahren, wenn Sie Nachrichten Funktionen auf niedriger Ebene verwenden möchten, um die gerade beschriebenen Aufgaben auszuführen.

**So können Sie eine Nachricht mithilfe von Nachrichten Funktionen auf niedriger Ebene mit Hash-und Codieren**

1.  Hiermit wird der zu hashende Inhalt erstellt oder abgerufen.
2.  Verschaffen Sie sich einen Kryptografieanbieter.
3.  Initialisieren Sie die CMSG-Hash Struktur zum [**\_ \_ Codieren von \_ Informationen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) .
4.  Sie können [**cryptmsgcalculateencodedlength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) aufrufen, um die Größe des codierten nachrichtenblobs zu erhalten. Arbeitsspeicher zuweisen.
5.  Nennen Sie " [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)", und übergeben Sie für den Parameter " \_ *dwmsgtype* " den Parameter "CMSG Hashed" und einen Zeiger auf " [**CMSG \_ Hashed \_ encode \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) " für den Parameter " *pvmsgencodeinfo* ". Als Ergebnis dieses Aufrufes wird ein Handle für die geöffnete Nachricht angezeigt.
6.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate), und übergeben Sie das in Schritt 5 abgerufene Handle und einen Zeiger auf die Daten, für die ein Hashwert erstellt und codiert werden soll. Diese Funktion kann so oft wie nötig aufgerufen werden, um den Codierungsprozess abzuschließen.
7.  Aufrufen von [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), übergeben des in Schritt 5 abgerufenen Handles und der entsprechenden Parametertypen für den Zugriff auf die gewünschten, codierten Daten. Übergeben Sie z. b. CMSG \_ Content \_ param, um einen Zeiger auf die gesamte [*PKCS \# 7*](../secgloss/p-gly.md) -Nachricht zu erhalten.

    Wenn das Ergebnis dieser Codierung als [*innere Daten*](../secgloss/i-gly.md) für eine andere codierte Nachricht verwendet werden soll, z. b. eine eingeschlossene Nachricht, muss CMSG-Bare-Content-Parameter \_ \_ \_ übergeben werden. Ein Beispiel, das dies veranschaulicht, finden Sie unter [alternativer Code zum Codieren einer](alternate-code-for-encoding-an-enveloped-message.md)eingeschlossenen Nachricht.

8.  Schließen Sie die Nachricht, indem Sie [**cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)aufrufen.

Das Ergebnis dieser Prozedur ist eine codierte Nachricht, die die ursprünglichen Daten, die Hash Algorithmen und den [*Hash*](../secgloss/h-gly.md) der Daten enthält. Ein Zeiger auf das codierte [*nachrichtenblob*](../secgloss/b-gly.md) wird in Schritt 7 abgerufen.

Die folgenden zwei Prozeduren decodieren und überprüfen dann Hashdaten.

**So decodieren Sie Daten mit Hash**

1.  Einen Zeiger auf das codierte BLOB erhalten.
2.  Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente.
3.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die Daten, die decodiert werden sollen. Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.
4.  Aufrufen von [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), übergeben des in Schritt 2 abgerufenen Handles und der entsprechenden Parametertypen für den Zugriff auf die gewünschten, decodierten Daten. Übergeben Sie z. b. CMSG \_ Content \_ param, um einen Zeiger auf den decodierten Inhalt zu erhalten.

**So überprüfen Sie den Hash**

1.  Nennen Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), und übergeben \_ Sie den Hash der CMSG STRG-Taste, \_ \_ um die Hashwerte zu überprüfen.
2.  " [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) " aufrufen, um die Nachricht zu schließen.

Ein Beispielprogramm finden Sie unter [Beispiel C-Programm: Codieren und Decodieren einer Hash Nachricht](example-c-program-encoding-and-decoding-a-hashed-message.md).

 

 
