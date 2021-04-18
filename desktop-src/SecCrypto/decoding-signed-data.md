---
description: Prozess zum Decodieren signierter Daten.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decodieren signierter Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340180"
---
# <a name="decoding-signed-data"></a>Decodieren signierter Daten

Der folgende allgemeine Prozess decodiert einen [*signierten Datentyp*](../secgloss/s-gly.md) .

**Decodieren einer signierten Nachricht**

1.  Einen Zeiger auf das codierte BLOB erhalten.
2.  Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente.
3.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal, und übergeben Sie dabei das in Schritt 2 abgerufene Handle und einen Zeiger auf die Daten, die decodiert werden sollen. Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.
4.  Aufrufen von [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), übergeben des in Schritt 2 abgerufenen Handles und der entsprechenden Parametertypen für den Zugriff auf die decodierten Daten. Übergeben Sie z. b. CMSG \_ Content \_ param, um einen Zeiger auf den decodierten Inhalt zu erhalten.

Im folgenden allgemeinen Prozess wird die Signatur einer decodierten, signierten Nachricht überprüft.

**So überprüfen Sie die Signatur einer decodierten, signierten Nachricht**

1.  Nennen Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), und übergeben Sie das Nachrichten Handle und CMSG \_ Signer \_ CERT \_ Info \_ param, um die [**Zertifikat \_ Informationen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) des Signatur Gebers aus der Nachricht abzurufen.
2.  Zum Öffnen eines temporären Informationsspeicher, der mit den Zertifikaten aus der Nachricht initialisiert wird, wird " [**certopdstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) " aufgerufen.
3.  Nennen Sie [**certgetsubjetcertificallefromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) , um die [**Zertifikat \_ Informationen**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) des Signatur Gebers aus den in der Nachricht enthaltenen Zertifikaten abzurufen.
4.  Nennen Sie [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), und übergeben \_ \_ \_ Sie die Signatur von CMSG STRG Verify, um die Signaturen zu überprüfen.
5.  " [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) " aufrufen, um die Nachricht zu schließen.

Das Ergebnis dieser Prozeduren ist, dass die Signatur überprüft und ein Zeiger auf den decodierten Nachrichten Inhalt abgerufen wird, der in Schritt 4 der Prozedur zum Decodieren einer signierten Nachricht abgerufen wurde.

Weitere Informationen zur C-Codierung finden Sie [unter Beispiel c-Programm: Signieren, codieren, decodieren und Überprüfen einer Nachricht](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
