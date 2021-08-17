---
description: Mehrere Funktionen stellen Dienste zum Verwalten eines Zertifikatspeicherstatus zur Verfügung.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Verwalten eines Zertifikats Store Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cbbb41691b66abfa2d49d669b13ec7fd438bd4ae503bf944d9e4923f647f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425670"
---
# <a name="managing-a-certificate-store-state"></a>Verwalten eines Zertifikats Store Status

Mehrere Funktionen stellen Dienste zum Verwalten eines [*Zertifikatspeicherstatus*](../secgloss/c-gly.md) [*zur Verfügung.*](../secgloss/s-gly.md)

Um Zugriff auf Zertifikate zu erhalten, muss der Zertifikatspeicher, in dem sie gespeichert sind, durch einen Aufruf von [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) oder [**CertOpenSystemStore geöffnet werden.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)

In der Regel wird ein Zertifikatspeicher im zwischengespeicherten Arbeitsspeicher geöffnet. Es kann sich um einen neuen Speicher oder seinen Inhalt aus der lokalen Registrierung, der Registrierung auf einem Remotecomputer, einer Datenträgerdatei, einer PKCS 7-Nachricht oder einer anderen Quelle \# sein.

CryptoAPI-Zertifikatspeicherfunktionen ermöglichen es einem Speicher auch, Zertifikate außerhalb des zwischengespeicherten Arbeitsspeichers zu verwalten, z. B. in einer externen Datenbank mit Zertifikaten, z. B. der von der Microsoft-Zertifikatserver-Datenbank bereitgestellten Datenbank.

Einer der Parameter der [**CertOpenStore-Funktion,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) *lpszStoreProvider,* bestimmt den Typ des geöffneten Speichers und den Anbieter, der zum Öffnen dieses Speichers verwendet wird. Beispiele zum Öffnen von Zertifikatspeichern mithilfe verschiedener Anbieter finden Sie unter [C-Beispielcode zum Öffnen von Zertifikatspeichern.](example-c-code-for-opening-certificate-stores.md)

[**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) schließt einen Zertifikatspeicher. Wenn ein Zertifikatspeicher geschlossen wird, wird die Verweisanzahl jedes Zertifikatkontexts in diesem Speicher [*um*](../secgloss/r-gly.md) eins reduziert. Arbeitsspeicher wird für Zertifikate frei, deren Verweisanzahl auf 0 (null) gesetzt wird.

Wenn Sie CERT CLOSE STORE FORCE FLAG mit \_ \_ \_ \_ [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) festlegen, wird der Zertifikatspeicher geschlossen und Arbeitsspeicher für alle Zertifikatkontexte frei, unabhängig von der Verweisanzahl. In einigen Fällen, z. B. in Multithreadprogrammen, ist dies nicht wünschenswert. Wenn CERT CLOSE STORE CHECK FLAG festgelegt ist, wird der Speicher geschlossen, aber von der Funktion wird ein Warnungswert zurückgegeben, wenn für Zertifikate, deren Verweisanzahl nicht auf 0 reduziert wurde, weiterhin Arbeitsspeicher zugeordnet \_ \_ \_ \_ wird. Wenn die Verweisanzahl eines Zertifikats größer als 0 (null) ist, wurde kein Duplikat dieses Zertifikatkontexts frei. Verwenden [**Sie CertFreeCertificateContext,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)und [**CertFreeCTLContext,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) um alle geöffneten Zertifikate frei zu geben.

> [!Note]
> Ein [*Zertifikatkontext*](../secgloss/c-gly.md) ist eine Struktur vom Typ [**CERT \_ CONTEXT,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) die neben anderen Membern über einen Zeiger auf das codierte ZertifikatBLOB und einen Zeiger auf eine [**CERT \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) verfügt. [](../secgloss/c-gly.md) Die **CERT \_ INFO-Struktur** enthält die wichtigsten Zertifikatdaten. Weitere Informationen zu [*Zertifikaten,*](../secgloss/c-gly.md)Zertifikatsperrlisten (Certificate [*Revocation List,*](../secgloss/c-gly.md) CRL) und CTL-Kontextstrukturen [*(Certificate Trust List,*](../secgloss/c-gly.md) Zertifikatvertrauensliste) finden Sie unter Codieren und [Decodieren eines Zertifikatkontexts.](encoding-and-decoding-a-certificate-context.md)
> 
> Jeder Zertifikatkontext enthält auch einen [*Verweiszähler,*](../secgloss/r-gly.md) der die Anzahl der zugewiesenen Kopien der Kontextadresse angibt. Jedes Mal, wenn ein Zertifikatkontext in irgendeiner Weise dupliziert wird, wird seine Verweisanzahl um eins erhöht. Jedes Mal, wenn ein Zeiger auf einen Zertifikatkontext frei wird, wird die Verweisanzahl im Zertifikatkontext um eins dekrementiert. Wenn die Verweisanzahl für einen Zertifikatkontext 0 (null) erreicht, wird der Speicher, der den Kontext hält, nicht mehr zugeordnet. Der für einen Zertifikatkontext zugeordnete Arbeitsspeicher wird ebenfalls wieder zugeordnet, wenn sich dieser Kontext in einem Speicher befindet und der Speicher mithilfe des CERT \_ CLOSE \_ STORE \_ FORCE-FLAGs geschlossen \_ wird. Wenn der Speicher für einen Kontext nicht mehr zugeordnet wird und Zeiger auf diesen Kontext noch verwendet werden, sind diese Zeiger nicht mehr gültig.

 

[**CertDuplicateStore erhöht**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) die [*Verweisanzahl*](../secgloss/r-gly.md) im Speicher.

[**CertSaveStore speichert**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) den Inhalt eines Speichers in einer Datenträgerdatei oder einem Speicherort, und

[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) verwaltet einen Speicher, während er geöffnet ist. Eine Anwendung mit einem geöffneten Speicher kann benachrichtigt werden, wenn sich der persistente Zustand dieses Speichers durch einen anderen Prozess geändert hat. Dies kann passieren, wenn neue Zertifikate von einem Domänensteuerungscomputer in den lokalen Computerspeicher kopiert werden.

Wenn Änderungen gefunden werden, kann der zwischengespeicherte Speicher seinen zwischengespeicherten Speicher erneut synchronisieren, um dem persistenten Zustand des Speichers zu passen. [**CertControlStore unterstützt**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) auch einen Prozess, bei dem zwischengespeicherte Speicheränderungen in permanenten Speicher kopiert werden, wenn diese Änderungen im zwischengespeicherten Speicher nicht automatisch gespeichert werden.

Zertifikatspeicher-orientierte Zertifikatkontexte können erweiterte Eigenschaften aufweisen. [**CertSetStoreProperty fügt**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) einem Zertifikatspeicher erweiterte Eigenschaften hinzu. [**CertGetStoreProperty ruft**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) alle Eigenschaften ab, die für einen Zertifikatspeicher festgelegt sind. Derzeit ist die einzige vordefinierte Zertifikatspeichereigenschaft der lokalisierte Name eines Speichers.

 

 
