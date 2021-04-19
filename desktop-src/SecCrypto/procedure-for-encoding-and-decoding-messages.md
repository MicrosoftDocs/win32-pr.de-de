---
description: Erläutert das Verfahren zum Codieren einer allgemeinen Nachricht.
ms.assetid: 554cab0d-cfa2-46a7-80d9-f41430eb4b47
title: Verfahren zum Codieren und Decodieren von Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49da09c2318fffd3d1c92d6012055172709609a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351627"
---
# <a name="procedure-for-encoding-and-decoding-messages"></a>Verfahren zum Codieren und Decodieren von Nachrichten

Die Vorgehensweise zum Codieren einer allgemeinen Nachricht lautet wie folgt.

**So codieren Sie eine Nachricht**

1.  Initialisieren Sie die entsprechenden Datenstrukturen für den gewünschten Datentyp.
2.  Nennen Sie [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), und übergeben Sie die erforderlichen Argumente. Wenn beim Aufrufen von **cryptmsgopentoencode** die Daten, die für [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) bereitgestellt werden sollen, bereits Nachrichten codiert wurden, übergeben Sie den entsprechenden Objekt Bezeichner in *pszinnercontentobjid* (z. b. "1.2.840.113549.1.7.2" für szoid \_ RSA \_ SignedData). Wenn *pszinnercontentobjid* **null** ist, wird davon ausgegangen, dass der [*innere Inhaltstyp*](../secgloss/i-gly.md) zuvor nicht codiert wurde und entsprechend verarbeitet wird.
3.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) so oft wie erforderlich, um die Nachricht abzuschließen. Legen Sie den *ffinal* -Parameter beim letzten Aufrufen auf **true** fest. (Ausführliche Informationen finden Sie unter **cryptmsgupdate**).
4.  Bitten Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , einen Zeiger auf die gewünschten Parameter zu erhalten, z. b. den Inhalt. Verwenden Sie für die Codierung von einfachen allgemeinen Daten CMSG- \_ Inhalts Parameter \_ für den *dwParamType*.
5.  Schließen Sie die Nachricht, indem Sie [**cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)aufrufen.

Diese Prozedur führt zu einer codierten Nachricht eines Typs, der in den Funktionsaufrufen angegeben wird.

Die Prozedur für das Decodieren einer allgemeinen Nachricht lautet wie folgt.

**So decodieren Sie eine Nachricht**

1.  Bestimmen Sie die Länge, die der Puffer zum Speichern der codierten Daten mithilfe von [**cryptmsgcalculateencodlength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)benötigt.
2.  Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente. Um die Kompatibilität mit Internet Explorer Version 3,0 aufrechtzuerhalten, wird der *dwmsgtype* -Parameter bereitgestellt. Signierte Daten, die in Internet Explorer 3,0 erstellt wurden, enthalten keine Header Informationen. Wenn eine solche Nachricht aus Datei Signaturen extrahiert wird, muss der Nachrichtentyp daher an die Funktion übermittelt werden. Wenn 0 an den *dwmsgtype* -Parameter übergeben wird, liest die Funktion den Nachrichtentyp aus dem Header der Nachricht. Wenn der Header fehlt, schlägt der Funktionsaufrufe fehl. Wenn erfolgreich, wird ein Handle für die geöffnete Nachricht zurückgegeben.
3.  " [**Cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) " einmal aufrufen. Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.
4.  Zur weiteren Verarbeitung der Nachricht, z. b. zusätzliche Entschlüsselung oder Signatur Überprüfung, wird [**cryptmsgcontrol**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)aufgerufen und die gewünschte Aktion in *dwctrltype* übergeben.
5.  Bitten Sie [**cryptmsggetparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) , einen Zeiger auf die gewünschten Parameter zu erhalten, z. b. den Inhalt. Zum Decodieren einfacher allgemeiner Daten verwenden Sie CMSG \_ Content \_ param für den *dwParamType* -Parameter.
6.  " [**Cryptmsgclose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) " aufrufen, um die Nachricht zu schließen.

Ein Beispiel, das diese Schritte implementiert, finden Sie unter [Beispiel C-Programm: Codieren und Decodieren von Daten](example-c-program-encoding-and-decoding-data.md). Prozeduren und ein Beispiel, das den Prozess der Codierung, Decodierung und Überprüfung der Signatur einer signierten Nachricht veranschaulicht, finden Sie [unter Beispiel C-Programm: Signieren, codieren, decodieren und Überprüfen einer Nachricht](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 
