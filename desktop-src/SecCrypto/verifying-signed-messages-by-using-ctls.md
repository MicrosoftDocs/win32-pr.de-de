---
description: Einer der Vorteile der Verwendung von Zertifikat Vertrauens Listen (Certificate Trust Lists, CTLs) besteht darin, dass Anwendungen entworfen werden können, die signierte Nachrichten anhand vertrauenswürdiger Zertifikate automatisch verifizieren können, ohne den Benutzer mit Dialogfeldern zu stören.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Überprüfen von signierten Nachrichten mithilfe von CTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373069"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Überprüfen von signierten Nachrichten mithilfe von CTLs

Einer der Vorteile der Verwendung von [*Zertifikat Vertrauens Listen (Certificate Trust Lists*](../secgloss/c-gly.md) , CTLs) besteht darin, dass Anwendungen entworfen werden können, die signierte Nachrichten anhand vertrauenswürdiger Zertifikate automatisch verifizieren können, ohne den Benutzer mit Dialogfeldern zu stören. Außerdem werden einem Netzwerkadministrator Steuerungs Quellen als vertrauenswürdig eingestuft.

Das folgende Verfahren kann verwendet werden, um die Signatur einer signierten Nachricht mithilfe einer CTL zu überprüfen.

**So überprüfen Sie eine signierte Nachricht mithilfe einer CTL**

1.  Decodieren Sie die Nachricht wie folgt:

    1.  Einen Zeiger auf die empfangene Meldung (das codierte [*BLOB*](../secgloss/b-gly.md)) erhalten.
    2.  Nennen Sie [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), und übergeben Sie die erforderlichen Argumente.
    3.  Nennen Sie [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal, und übergeben Sie dabei das in Schritt b abgerufene Handle und einen Zeiger auf die Daten, die decodiert werden sollen. Dies bewirkt, dass die entsprechenden Aktionen für die Nachricht durchgeführt werden, abhängig vom Nachrichtentyp.

2.  Überprüfen Sie die Signatur der decodierten, signierten Nachricht, und erhalten Sie einen Zeiger auf den [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)des Signatur Gebers.

    Dies kann durch Aufrufen von [**cryptmsggetandverifysigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)erfolgen, indem das in Schritt 1C abgerufene Nachrichten Handle als *hcryptmsg* -Parameter übergeben wird. Wenn der Funktions Aufrufwert **true** zurückgibt, wurde die Signatur überprüft, und ein Zeiger auf den [**pccert- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) des Signatur Gebers wird im *ppsigner* -Parameter zurückgegeben.

3.  Vergewissern Sie sich, dass der Signatur Geber wie folgt eine vertrauenswürdige Quelle ist:

    1.  Öffnen Sie den Zertifikat Speicher, der die entsprechende CTL enthält.
    2.  Abrufen eines Zeigers auf den [**CTL- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) durch Aufrufen von " [**certfindctlinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)".
    3.  Um zu bestätigen, dass der Signatur Geber eine vertrauenswürdige Quelle ist, müssen Sie [**certfindsubjetinctl**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)aufrufen und dabei den im vorherigen Schritt abgerufenen Zeiger im *pctlcontext* -Parameter, CTL \_ CERT \_ Subject \_ Type im Parameter *dwsubjettype* und den Zeiger auf den in Schritt 2 im Parameter *pvsubject* abgerufenen [**Zertifikat \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) übergeben. Wenn der Funktions Rückruf **true** zurückgibt, ist der an die Funktion über gegebene **CERT- \_ Kontext** eine vertrauenswürdige Quelle in der CTL.

 

 
