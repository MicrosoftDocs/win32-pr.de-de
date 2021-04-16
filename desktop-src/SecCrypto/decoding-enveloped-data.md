---
description: Allgemeine Aufgaben, die zum Decodieren einer eingeschlossenen Nachricht erforderlich sind.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Decodieren von eingeschlossenen Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557336"
---
# <a name="decoding-enveloped-data"></a>Decodieren von eingeschlossenen Daten

Die allgemeinen Aufgaben, die zum Decodieren einer eingeschlossenen Nachricht erforderlich sind, werden in der folgenden Abbildung dargestellt und in der folgenden Liste beschrieben.

![Decodieren von eingeschlossenen Daten](images/decemsg.png)

Die Abfolge der Ereignisse für das Decodieren von eingeschlossenen Daten mithilfe der Schlüssel Transport Schlüsselverwaltung, wie in der vorherigen Abbildung dargestellt, lautet wie folgt:

-   Ein Zeiger auf die [*Digital eingehüllte*](../secgloss/d-gly.md) Nachricht wird abgerufen.
-   Ein [*Zertifikat Speicher*](../secgloss/c-gly.md) wird geöffnet.
-   In der Meldung wird die Empfänger-ID (meine ID) abgerufen.
-   Die Empfänger-ID wird zum Abrufen des Zertifikats verwendet.
-   Der diesem Zertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird abgerufen.
-   Der private Schlüssel wird verwendet, um den [*symmetrischen*](../secgloss/s-gly.md) ([*Sitzungs*](../secgloss/s-gly.md)-) Schlüssel zu entschlüsseln.
-   Der Verschlüsselungsalgorithmus wird aus der Nachricht abgerufen.
-   Mit dem privaten Schlüssel und dem Verschlüsselungsalgorithmus werden die Daten entschlüsselt.

Im folgenden Verfahren werden Low-Level-Nachrichten Funktionen verwendet, um die gerade aufgeführten Aufgaben auszuführen.

**So decodieren Sie eine eingeschlossene Nachricht**

1.  Einen Zeiger auf das codierte BLOB erhalten.
2.  Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente.
3.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die Daten, die decodiert werden sollen. Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.
4.  Nennen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie das in Schritt 2 und CMSG-Typparameter abgerufene handle, \_ \_ um zu überprüfen, ob die Nachricht vom eingeschlossenen Datentyp ist.
5.  Wiederholen Sie den Befehl [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie \_ \_ den internen Inhaltstyp CMSG, \_ \_ um den Datentyp des [*inneren Inhalts*](../secgloss/i-gly.md)abzurufen.
6.  Wenn der Datentyp der inneren Inhalte " **Daten**" ist, können Sie den Inhalt entschlüsseln und decodieren. Andernfalls führen Sie eine für den Inhalts Datentyp geeignete Decodierungs Prozedur aus.
7.  Angenommen, der innere Inhaltstyp ist "Data", initialisieren Sie die [**CMSG \_ STRG \_ entschlüsseln \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) -Datenstruktur, und nennen Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), und übergeben Sie CMSG \_ STRG \_ entschlüsseln und die Adresse der-Struktur. Der Inhalt wird entschlüsselt.
8.  Nennen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie CMSG \_ Content \_ param, um einen Zeiger auf das decodierte inhaltsdatenblob (**Byte** Zeichenfolge) zu erhalten.
9.  " [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) " aufrufen, um die Nachricht zu schließen.

Das Ergebnis dieser Prozedur ist, dass die Nachricht decodiert und entschlüsselt und ein Zeiger in das inhaltsdatenblob abgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel-C-Programm: Codieren einer eingeschlossenen, signierten Nachricht](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
