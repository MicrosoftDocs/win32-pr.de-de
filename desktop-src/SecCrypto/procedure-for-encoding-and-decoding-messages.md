---
description: Beschreibt das Verfahren zum Codieren einer allgemeinen Nachricht.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Verfahren zum Codieren und Decodieren von Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a2fa98ace21513acdbdfb7241216b605b24b05c1890c776ee9c134668cb3ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977582"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Verfahren zum Codieren und Decodieren von Nachrichten

Das Verfahren zum Codieren einer allgemeinen Nachricht lautet wie folgt.

**So codieren Sie eine Nachricht**

1.  Initialisieren Sie die entsprechenden Datenstrukturen für den gewünschten Datentyp.
2.  Rufen Sie [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)auf, und übergeben Sie die erforderlichen Argumente. Wenn beim Aufrufen von **CryptMsgOpenToEncode** die Daten, die [**für CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) bereitgestellt werden sollen, bereits nachrichtencodiert wurden, übergeben Sie den entsprechenden Objektbezeichner in *pszInnerContentObjID* (z.B. "1.2.840.113549.1.7.2" für szOID \_ RSA \_ signedData). Wenn *pszInnerContentObjID* **NULL** ist, wird davon ausgegangen, dass der [*innere Inhaltstyp*](../secgloss/i-gly.md) nicht zuvor codiert wurde und entsprechend verarbeitet wird.
3.  Rufen Sie [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) so oft wie nötig auf, um die Nachricht abzuschließen. Legen Sie beim letzten Aufruf den *fFinal-Parameter* auf **TRUE** fest. (Weitere Informationen finden Sie unter **CryptMsgUpdate**.
4.  Rufen Sie [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um einen Zeiger auf die gewünschten Parameter wie den Inhalt abzurufen. Verwenden Sie für die Codierung einfacher, allgemeiner Daten CMSG \_ CONTENT \_ PARAM für *dwParamtype.*
5.  Schließen Sie die Nachricht, indem [**Sie CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)aufrufen.

Diese Prozedur führt zu einer codierten Nachricht eines in den Funktionsaufrufen angegebenen Typs.

Das Verfahren zum Decodieren einer allgemeinen Nachricht lautet wie folgt.

**So decodieren Sie eine Nachricht**

1.  Bestimmen Sie mithilfe von [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)die Erforderliche Länge für den Puffer zum Speichern der codierten Daten.
2.  Rufen Sie [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)auf, und übergeben Sie die erforderlichen Argumente. Um die Kompatibilität mit Internet Explorer Version 3.0 aufrechtzuerhalten, wird der *dwMsgType-Parameter* bereitgestellt. Signierte Daten, die in Internet Explorer 3.0 erstellt wurden, enthalten keine Headerinformationen. Wenn eine solche Nachricht aus Dateisignaturen extrahiert wird, muss der Nachrichtentyp daher an die Funktion übergeben werden. Wenn 0 (null) an den *parameter dwMsgType* übergeben wird, liest die Funktion den Nachrichtentyp aus dem Header der Nachricht. Wenn der Header fehlt, schlägt der Funktionsaufruf fehl. Bei Erfolg wird ein Handle für die geöffnete Nachricht zurückgegeben.
3.  Rufen Sie [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal auf. Dies bewirkt, dass je nach Nachrichtentyp die entsprechenden Aktionen für die Nachricht ausgeführt werden.
4.  Rufen Sie [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)auf, und übergeben Sie die gewünschte Aktion in *dwCtrlType,* um die Nachricht zusätzlich zu verarbeiten, z. B. eine zusätzliche Entschlüsselung oder Signaturüberprüfung.
5.  Rufen Sie [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) auf, um einen Zeiger auf die gewünschten Parameter wie den Inhalt abzurufen. Verwenden Sie CMSG \_ CONTENT \_ PARAM für den *dwParamtype-Parameter,* um einfache allgemeine Daten zu decodieren.
6.  Rufen Sie [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) auf, um die Nachricht zu schließen.

Ein Beispiel, in dem diese Schritte implementiert werden, finden Sie unter [C-Beispielprogramm: Codieren und Decodieren von Daten.](example-c-program-encoding-and-decoding-data.md) Prozeduren und ein Beispiel, das den Prozess der Codierung, Decodierung und Überprüfung der Signatur einer signierten Nachricht veranschaulicht, finden Sie unter [C-Beispielprogramm: Signieren, Codieren, Decodieren und Überprüfen einer Nachricht.](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)

 

 
