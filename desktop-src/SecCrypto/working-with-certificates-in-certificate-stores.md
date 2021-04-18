---
description: Mehrere Funktionen fügen einen Zertifikat Kontext oder einen Link zu einem Kontext zu einem Store \[ Platform Software Development Kit (SDK) hinzu \] .
ms.assetid: 0355b254-be52-4af4-9567-ee2df092075f
title: Arbeiten mit Zertifikaten in Zertifikat speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba1ce89c9b9352ef787ed65230b709967125532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347659"
---
# <a name="working-with-certificates-in-certificate-stores"></a>Arbeiten mit Zertifikaten in Zertifikat speichern

Mehrere Funktionen fügen einen Zertifikat Kontext oder einen Link zu einem Speicher zu einem Speicher hinzu.

Für Zertifikate, die bereits im Zertifikat Kontext Formular vorhanden sind:

-   [**Certaddcertificatcher econtextto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
-   [**Certaddcrlcontextflistore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)
-   [**Certaddctlcontextto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)
-   [**Certaddcertifialisielinktostore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)
-   [**Certaddcrllinkto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)
-   [**Certaddctllinkto Store**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)

Für Zertifikate, die codierte Formulare, aber keine vollständigen Zertifikat Kontexte sind:

-   [**Bei CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)
-   [**Certaddencodedcrldestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)
-   [**Certaddencodedctldestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)

Mit den folgenden Funktionen wird ein Zertifikat, eine Zertifikat Sperr Liste oder eine CTL aus einem Speicher gelöscht, indem der Verweis Zähler um 1 dekrementiert wird. Wenn dies bewirkt, dass der Verweis Zähler Null wird, wird der zum Speichern des Zertifikats, der CRL oder der CTL verwendete Arbeitsspeicher freigegeben.

-   [**Certdeletecertifipeefromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)
-   [**Certdeletecrlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)
-   [**Certdeletectlfromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)

 

 



