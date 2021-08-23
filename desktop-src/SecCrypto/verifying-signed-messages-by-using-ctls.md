---
description: Einer der Vorteile der Verwendung von Zertifikatvertrauenslisten (Certificate Trust Lists, CTLs) besteht darin, dass Anwendungen entworfen werden können, die signierte Nachrichten automatisch anhand vertrauenswürdiger Zertifikate überprüfen können, ohne den Benutzer mit Dialogfeldern zu stören.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Überprüfen von signierten Nachrichten mithilfe von CTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624a132ed976800d1c8a8ab0dcd878f533f0d0b947879e87e3e8dc21ccff51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896231"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Überprüfen von signierten Nachrichten mithilfe von CTLs

Einer der Vorteile der Verwendung von [*Zertifikatvertrauenslisten (Certificate Trust Lists,*](../secgloss/c-gly.md) CTLs) besteht darin, dass Anwendungen entworfen werden können, die signierte Nachrichten automatisch anhand vertrauenswürdiger Zertifikate überprüfen können, ohne den Benutzer mit Dialogfeldern zu stören. Außerdem erhalten Netzwerkadministrator-Steuerungsquellen, die als vertrauenswürdig eingestuft werden können.

Das folgende Verfahren kann verwendet werden, um die Signatur einer signierten Nachricht mithilfe einer CTL zu überprüfen.

**So überprüfen Sie eine signierte Nachricht mithilfe einer CTL**

1.  Decodieren Sie die Nachricht wie folgt:

    1.  Abrufen eines Zeigers auf die empfangene Nachricht (das codierte [*BLOB).*](../secgloss/b-gly.md)
    2.  Rufen Sie [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)auf, und übergeben Sie die erforderlichen Argumente.
    3.  Rufen Sie [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) einmal auf, und übergeben Sie das in Schritt b abgerufene Handle und einen Zeiger auf die zu decodierenden Daten. Dies bewirkt, dass je nach Nachrichtentyp die entsprechenden Aktionen für die Nachricht ausgeführt werden.

2.  Überprüfen Sie die Signatur der decodierten, signierten Nachricht, und erhalten Sie einen Zeiger auf den [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)des Signaturgebers.

    Dazu können Sie [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)aufrufen und das in Schritt 1c abgerufene Nachrichtenhandle als *hCryptMsg-Parameter* übergeben. Wenn der Funktionsaufruf **TRUE** zurückgibt, wurde die Signatur überprüft, und ein Zeiger auf den [**PCCERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) des Signaturgebers wird im *ppSigner-Parameter* zurückgegeben.

3.  Vergewissern Sie sich wie folgt, dass der Signierer eine vertrauenswürdige Quelle ist:

    1.  Öffnen Sie den Zertifikatspeicher, der die entsprechende CTL enthält.
    2.  Rufen Sie einen Zeiger auf den [**CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) ab, indem [**Sie CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)aufrufen.
    3.  Um zu bestätigen, dass der Signierer eine vertrauenswürdige Quelle ist, rufen Sie [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)auf, und übergeben Sie den Im vorherigen Schritt im *pCtlContext-Parameter* abgerufenen Zeiger, CTL \_ CERT \_ SUBJECT TYPE im \_ *dwSubjectType-Parameter* und den Zeiger auf den in Schritt 2 abgerufenen [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) im *pvSubject-Parameter.* Wenn der Funktionsaufruf **TRUE** zurückgibt, ist der an die Funktion übergebene **CERT \_ CONTEXT** eine vertrauenswürdige Quelle in der CTL.

 

 
