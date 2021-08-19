---
description: Stellt die Aufgaben dar, die zum Codieren einer Hashnachricht erforderlich sind.
ms.assetid: c1a65452-c634-4cc6-9afe-d6bf11d999d1
title: Codieren und Decodieren einer Hashnachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bed6ffae240d9139de471f16dcaaf2ed3e29d5bc92c8d7507b981c2af67541c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766741"
---
# <a name="encoding-and-decoding-a-hashed-message"></a>Codieren und Decodieren einer Hashnachricht

Hashdaten bestehen aus Inhalten eines beliebigen Typs und einem [*Hash*](../secgloss/h-gly.md) des Inhalts. Sie kann verwendet werden, wenn nur bestätigt werden muss, dass der Nachrichteninhalt seit der Erstellung des Hashs nicht geändert wurde.

Beim Erstellen einer Hashnachricht können mehrere Hashalgorithmen und mehrere Hashwerte vorhanden sein. Die folgende Abbildung zeigt die Aufgaben, die zum Codieren einer Hashnachricht erforderlich sind. Die Prozedur wird in dem Text beschrieben, der auf die Abbildung folgt.

![Erstellen einer Hashnachricht](images/hashmsg.png)

**So erstellen Sie eine Hashnachricht**

1.  Abrufen eines Zeigers auf die Daten, für die ein Hashwert verwendet werden soll.
2.  Wählen Sie den zu verwendenden Hashalgorithmus aus.
3.  Legen Sie die Daten mithilfe des Hashalgorithmus über eine Hashfunktion ab.
4.  Fügen Sie die ursprünglichen Zu hashenden Daten, die Hashalgorithmen und die Hashes in die codierte Nachricht ein.

Verwenden Sie das folgende Verfahren, um Nachrichtenfunktionen auf niedriger Ebene zu verwenden, um die soeben beschriebenen Aufgaben auszuführen.

**So hashen und codieren Sie eine Nachricht mithilfe von Nachrichtenfunktionen auf niedriger Ebene**

1.  Erstellen Sie den Inhalt, für den ein Hash erstellt werden soll, oder rufen Sie diesen ab.
2.  Abrufen eines Kryptografieanbieters.
3.  Initialisieren Sie die [**CMSG \_ HASHED \_ ENCODE \_ INFO-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info)
4.  Rufen Sie [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength) auf, um die Größe des codierten Nachrichten-BLOB abzurufen. Belegen Sie Dafür Arbeitsspeicher.
5.  Rufen Sie [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)auf, und übergeben Sie CMSG \_ HASHED für den *dwMsgType-Parameter* und einen Zeiger auf [**CMSG \_ HASHED \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_hashed_encode_info) für den *parameter pvMsgEncodeInfo.* Als Ergebnis dieses Aufrufs erhalten Sie ein Handle für die geöffnete Nachricht.
6.  Rufen Sie [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)auf, und übergeben Sie das in Schritt 5 abgerufene Handle und einen Zeiger auf die Daten, die gehasht und codiert werden sollen. Diese Funktion kann so oft wie nötig aufgerufen werden, um den Codierungsprozess abzuschließen.
7.  Rufen Sie [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie das in Schritt 5 abgerufene Handle und die entsprechenden Parametertypen für den Zugriff auf die gewünschten, codierten Daten. Übergeben Sie beispielsweise CMSG \_ CONTENT \_ PARAM, um einen Zeiger auf die gesamte [*PKCS \# 7-Nachricht*](../secgloss/p-gly.md) abzurufen.

    Wenn das Ergebnis dieser Codierung als [*innere Daten*](../secgloss/i-gly.md) für eine andere codierte Nachricht verwendet werden soll, z. B. eine umschlagbare Nachricht, muss CMSG \_ BARE CONTENT \_ \_ PARAM übergeben werden. Ein Beispiel, das dies zeigt, finden Sie unter [Alternativer Code für die Codierung einer umschlageten Nachricht.](alternate-code-for-encoding-an-enveloped-message.md)

8.  Schließen Sie die Nachricht, indem [**Sie CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)aufrufen.

Das Ergebnis dieser Prozedur ist eine codierte Nachricht, die die ursprünglichen Daten, die Hashalgorithmen und den [*Hash*](../secgloss/h-gly.md) dieser Daten enthält. In Schritt 7 wird ein Zeiger auf das codierte [*Nachrichten-BLOB*](../secgloss/b-gly.md) abgerufen.

Die folgenden beiden Verfahren decodieren und überprüfen dann Hashdaten.

**So decodieren Sie Hashdaten**

1.  Abrufen eines Zeigers auf das codierte BLOB.
2.  Rufen Sie [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)auf, und übergeben Sie die erforderlichen Argumente.
3.  Rufen Sie [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal auf, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die zu decodierenden Daten. Dies bewirkt, dass je nach Nachrichtentyp die entsprechenden Aktionen für die Nachricht ausgeführt werden.
4.  Rufen Sie [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, übergeben Sie das in Schritt 2 abgerufene Handle und die entsprechenden Parametertypen, um auf die gewünschten decodierten Daten zuzugreifen. Übergeben Sie beispielsweise CMSG \_ CONTENT \_ PARAM, um einen Zeiger auf den decodierten Inhalt abzurufen.

**So überprüfen Sie den Hash**

1.  Rufen Sie [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)auf, und übergeben Sie CMSG \_ STRG \_ VERIFY \_ HASH, um die Hashes zu überprüfen.
2.  Rufen Sie [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) auf, um die Nachricht zu schließen.

Ein Beispielprogramm finden Sie unter [C-Beispielprogramm: Codieren und Decodieren einer Hashnachricht.](example-c-program-encoding-and-decoding-a-hashed-message.md)

 

 
