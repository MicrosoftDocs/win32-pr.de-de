---
description: Allgemeine Aufgaben, die zum Decodieren einer umschlagten Nachricht erforderlich sind.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodieren von umumschlagten Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df9df80b2a4bc1e3c9d6894bc83624908468edb63f7d0283ee3dca1b50a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767809"
---
# <a name="decoding-enveloped-data"></a>Decodieren von umumschlagten Daten

Die allgemeinen Aufgaben, die zum Decodieren einer umschlagten Nachricht erforderlich sind, sind in der folgenden Abbildung dargestellt und in der folgenden Liste beschrieben.

![Decodieren von umhumhierten Daten](images/decemsg.png)

Die Abfolge der Ereignisse zum Decodieren von umhumhierten Daten mithilfe der Schlüsseltransportschlüsselverwaltung, wie in der vorherigen Abbildung dargestellt, lautet wie folgt:

-   Ein Zeiger auf die [*digital umhumhierte Nachricht*](../secgloss/d-gly.md) wird abgerufen.
-   Ein [*Zertifikatspeicher*](../secgloss/c-gly.md) wird geöffnet.
-   Aus der Nachricht wird die Empfänger-ID (Meine ID) abgerufen.
-   Die Empfänger-ID wird zum Abrufen des Zertifikats verwendet.
-   Der [*private Schlüssel,*](../secgloss/p-gly.md) der diesem Zertifikat zugeordnet ist, wird abgerufen.
-   Der private Schlüssel wird verwendet, um den [*symmetrischen*](../secgloss/s-gly.md) Schlüssel [*(Sitzung)*](../secgloss/s-gly.md)zu entschlüsseln.
-   Der Verschlüsselungsalgorithmus wird aus der Nachricht abgerufen.
-   Mithilfe des privaten Schlüssels und des Verschlüsselungsalgorithmus werden die Daten entschlüsselt.

Im folgenden Verfahren werden Nachrichtenfunktionen auf niedriger Ebene verwendet, um die gerade aufgeführten Aufgaben auszuführen.

**So decodieren Sie eine umschlagte Nachricht**

1.  Hier erhalten Sie einen Zeiger auf das codierte BLOB.
2.  Rufen [**Sie CryptMsgOpenToDecode auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)und übergeben Sie die erforderlichen Argumente.
3.  Rufen [**Sie CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal auf, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die daten, die decodiert werden sollen. Dies führt dazu, dass je nach Nachrichtentyp die entsprechenden Aktionen für die Nachricht durchgeführt werden.
4.  Rufen [**Sie CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie das in Schritt 2 abgerufene Handle und CMSG TYPE PARAM, um zu überprüfen, ob die Nachricht den Umschlagdatentyp \_ auf \_ hat.
5.  Rufen Sie [**erneut CryptMsgGetParam auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)und übergeben Sie CMSG \_ INNER CONTENT TYPE \_ \_ PARAM, um den Datentyp \_ des inneren Inhalts zu [*erhalten.*](../secgloss/i-gly.md)
6.  Wenn der innere Inhaltsdatentyp Daten **ist,** fahren Sie mit dem Entschlüsseln und Decodieren des Inhalts fort. Führen Sie andernfalls eine decodierungsprozedur aus, die für den Inhaltsdatentyp geeignet ist.
7.  Unter der Annahme, dass der innere Inhaltstyp "data" ist, initialisieren Sie die [**CMSG-DATENstruktur STRG \_ \_ DECRYPT \_ PARA,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) und rufen [**Sie CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)auf, und übergeben Sie CMSG STRG DECRYPT und die Adresse der \_ \_ Struktur. Der Inhalt wird entschlüsselt.
8.  Rufen [**Sie CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie CMSG CONTENT PARAM, um einen Zeiger auf das \_ decodierte Inhaltsdaten-BLOB \_ **(BYTE-Zeichenfolge)** zu erhalten.
9.  Rufen [**Sie CryptMsgClose auf,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) um die Nachricht zu schließen.

Das Ergebnis dieser Prozedur ist, dass die Nachricht decodiert und entschlüsselt wird und ein Zeiger auf das Inhaltsdaten-BLOB abgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel C-Programm: Codieren einer umschlagenden, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
