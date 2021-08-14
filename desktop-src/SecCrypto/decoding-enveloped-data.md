---
description: Allgemeine Aufgaben, die zum Decodieren einer umschlageten Nachricht erforderlich sind.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodieren umschlageierter Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99df9df80b2a4bc1e3c9d6894bc83624908468edb63f7d0283ee3dca1b50a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767809"
---
# <a name="decoding-enveloped-data"></a>Decodieren umschlageierter Daten

Die allgemeinen Aufgaben, die zum Decodieren einer umschlageten Nachricht erforderlich sind, sind in der folgenden Abbildung dargestellt und in der darauf folgenden Liste beschrieben.

![Decodieren umschlageierter Daten](images/decemsg.png)

Die Abfolge der Ereignisse zum Decodieren umschlageter Daten mithilfe der Schlüsseltransportschlüsselverwaltung, wie in der vorherigen Abbildung dargestellt, sieht wie folgt aus:

-   Ein Zeiger auf die [*digital umschlagete*](../secgloss/d-gly.md) Nachricht wird abgerufen.
-   Ein [*Zertifikatspeicher*](../secgloss/c-gly.md) wird geöffnet.
-   Aus der Nachricht wird die Empfänger-ID (Meine ID) abgerufen.
-   Die Empfänger-ID wird zum Abrufen des Zertifikats verwendet.
-   Der diesem Zertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird abgerufen.
-   Der private Schlüssel wird verwendet, um den [*symmetrischen*](../secgloss/s-gly.md) Schlüssel [*(Sitzungsschlüssel)*](../secgloss/s-gly.md)zu entschlüsseln.
-   Der Verschlüsselungsalgorithmus wird aus der Nachricht abgerufen.
-   Mit dem privaten Schlüssel und dem Verschlüsselungsalgorithmus werden die Daten entschlüsselt.

Im folgenden Verfahren werden Nachrichtenfunktionen auf niedriger Ebene verwendet, um die soeben aufgeführten Aufgaben auszuführen.

**So decodieren Sie eine umschlagete Nachricht**

1.  Abrufen eines Zeigers auf das codierte BLOB.
2.  Rufen Sie [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)auf, und übergeben Sie die erforderlichen Argumente.
3.  Rufen Sie [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal auf, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die zu decodierenden Daten. Dies bewirkt, dass je nach Nachrichtentyp die entsprechenden Aktionen für die Nachricht ausgeführt werden.
4.  Rufen Sie [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie das in Schritt 2 abgerufene Handle und CMSG \_ TYPE \_ PARAM, um zu überprüfen, ob die Nachricht vom umschlagten Datentyp ist.
5.  Rufen Sie erneut [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie CMSG \_ INNER CONTENT TYPE \_ \_ \_ PARAM, um den Datentyp des [*inneren Inhalts*](../secgloss/i-gly.md)abzurufen.
6.  Wenn der innere Inhaltsdatentyp **Daten** ist, fahren Sie mit dem Entschlüsseln und Decodieren des Inhalts fort. Führen Sie andernfalls eine decodierungsprozedur aus, die für den Inhaltsdatentyp geeignet ist.
7.  Vorausgesetzt, der innere Inhaltstyp ist "data", initialisieren Sie die [**CMSG \_ STRG \_ DECRYPT PARA-Datenstruktur, \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) und rufen [**Sie CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)auf, indem Sie CMSG \_ STRG DECRYPT und die Adresse der Struktur \_ übergeben. Der Inhalt wird entschlüsselt.
8.  Rufen Sie [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)auf, und übergeben Sie CMSG \_ CONTENT \_ PARAM, um einen Zeiger auf das decodierte Inhaltsdaten-BLOB **(BYTE-Zeichenfolge)** abzurufen.
9.  Rufen Sie [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) auf, um die Nachricht zu schließen.

Das Ergebnis dieser Prozedur ist, dass die Nachricht decodiert und entschlüsselt und ein Zeiger auf das Inhaltsdaten-BLOB abgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[C-Beispielprogramm: Codieren einer umschlageten, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
