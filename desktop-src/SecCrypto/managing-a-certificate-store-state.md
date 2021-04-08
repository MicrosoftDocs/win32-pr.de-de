---
description: Mehrere Funktionen stellen Dienste zum Verwalten eines Zertifikat Speicher Zustands bereit.
ms.assetid: bae3d693-31b3-4c1d-9a8f-0dafa8bb6897
title: Verwalten eines Zertifikat Speicher Zustands
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d66e40817f0f92f48e8841455998eff4dbffd6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961240"
---
# <a name="managing-a-certificate-store-state"></a>Verwalten eines Zertifikat Speicher Zustands

Mehrere Funktionen stellen Dienste zum Verwalten eines [*Zertifikat Speicher*](../secgloss/c-gly.md) [*Zustands*](../secgloss/s-gly.md)bereit.

Um Zugriff auf Zertifikate zu erhalten, muss der Zertifikat Speicher, in dem Sie gespeichert werden, durch einen Rückruf von " [**certopatstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) " oder " [**certopssystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)" geöffnet werden.

In der Regel wird ein Zertifikat Speicher im zwischengespeicherten Speicher geöffnet. Dabei kann es sich um einen neuen Speicher handeln, oder der Inhalt kann aus der lokalen Registrierung, der Registrierung auf einem Remote Computer, einer Datenträger Datei, einer PKCS \# 7-Nachricht oder einer anderen Quelle geladen werden.

Kryptoapi-Zertifikat Speicherfunktionen ermöglichen einem Speicher auch das Verwalten von Zertifikaten außerhalb des zwischengespeicherten Speichers in, z. b. eine externe Datenbank von Zertifikaten, z. b. die von der Microsoft Certificate Server-Datenbank bereitgestellte.

Einer der Parameter der [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) -Funktion, *lpszstoreprovider,* bestimmt den Typ des geöffneten Stores und den Anbieter, mit dem dieser Speicher geöffnet wird. Beispiele zum Öffnen von Zertifikat speichern mithilfe verschiedener Anbieter finden Sie unter [Beispiel C-Code zum Öffnen von Zertifikat speichern](example-c-code-for-opening-certificate-stores.md).

[**Certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) schließt einen Zertifikat Speicher. Wenn ein Zertifikat Speicher geschlossen wird, wird für jeden der Zertifikat Kontexte in diesem Speicher der [*Verweis Zähler*](../secgloss/r-gly.md) um 1 reduziert. Der Arbeitsspeicher wird für Zertifikate freigegeben, deren Verweis Zähler Null ist.

Wenn Sie \_ das Flag "CERT close \_ Store \_ Force" mit " \_ [**certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) " festlegen, wird der Zertifikat Speicher geschlossen, und es wird unabhängig von der Verweis Anzahl Speicher für alle Zertifikat Kontexte freigegeben In einigen Fällen, wie z. b. in Multithreadprogrammen, ist dies nicht wünschenswert. Wenn \_ \_ \_ das Häkchen \_ des Zertifikats zum Schließen des Speichers festgelegt ist, wird der Speicher geschlossen, aber von der Funktion wird ein Warnungs Wert zurückgegeben, wenn noch Speicher für Zertifikate zugewiesen ist, deren Verweis Zähler nicht auf 0 (null) reduziert wurden. Wenn der Verweis Zähler eines Zertifikats größer als 0 (null) ist, wurde kein Duplikat dieses Zertifikat Kontexts freigegeben. Verwenden Sie [**certfreecertifiingecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext), [**certfreecrlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)und [**certfreectlcontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext) , um alle Zertifikate freizugeben, die offen bleiben.

> [!Note]
> Bei einem [*Zertifikat Kontext*](../secgloss/c-gly.md) handelt es sich um eine Struktur vom Typ [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) , bei der es sich unter anderem um einen Zeiger auf das codierte [*zertifikatblob*](../secgloss/c-gly.md) und einen Zeiger auf eine [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Struktur handelt. Die **CERT \_ Info** -Struktur enthält die wichtigsten Zertifikat Daten. Weitere Informationen zu [*Zertifikaten*](../secgloss/c-gly.md), Zertifikats Sperr [*Listen*](../secgloss/c-gly.md) (CRL) und CTL-Kontext Strukturen ( [*Certificate Trust List*](../secgloss/c-gly.md) ) finden Sie unter [Codieren und Decodieren eines Zertifikat Kontexts](encoding-and-decoding-a-certificate-context.md).
> 
> Jeder Zertifikat Kontext enthält auch einen [*Verweis Zähler*](../secgloss/r-gly.md) , der die Anzahl der Kopien der zugewiesenen Kontext Adresse angibt. Jedes Mal, wenn ein Zertifikat Kontext in irgendeiner Weise dupliziert wird, wird der zugehörige Verweis Zähler um eins erhöht. Jedes Mal, wenn ein Zeiger auf einen Zertifikat kontextfrei gegeben wird, wird der Verweis Zähler im Zertifikat Kontext um 1 dekrementiert. Wenn der Verweis Zähler in einem Zertifikat Kontext 0 (null) erreicht, wird der Arbeitsspeicher, der den Kontext enthält, nicht mehr zugeordnet. Der für einen Zertifikat Kontext zugewiesene Arbeitsspeicher wird ebenfalls aufgehoben, wenn sich dieser Kontext in einem Speicher befindet und der Speicher mit dem Zertifikat " \_ Close Store Force" geschlossen wird \_ \_ \_ . Wenn die Zuordnung des Arbeitsspeichers für einen Kontext aufgehoben wird und Zeiger auf diesen Kontext weiterhin verwendet werden, sind diese Zeiger nicht mehr gültig.

 

[**Certduplikatestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore) erhöht den [*Verweis Zähler*](../secgloss/r-gly.md) für den Speicher.

[**Certsavestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore) speichert den Inhalt eines Speichers in einer Datenträger Datei oder einem Speicherort.

[**Certcontrolstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) verwaltet einen Speicher, während er geöffnet ist. Eine Anwendung mit einem geöffneten Speicher kann benachrichtigt werden, wenn der beibehaltene Zustand dieses Stores von einem anderen Prozess geändert wurde. Dies kann der Fall sein, wenn neue Zertifikate von einem Domänen Steuerungscomputer in den lokalen Computerspeicher kopiert wurden.

Wenn Änderungen erkannt werden, kann der zwischengespeicherte Speicher seinen zwischengespeicherten Speicher neu synchronisieren, sodass er dem beibehaltenen Zustand des Speicher entspricht. [**Certcontrolstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) unterstützt auch einen Prozess, bei dem zwischengespeicherte Speicher Änderungen in einen permanenten Speicher kopiert werden, wenn diese Änderungen im zwischengespeicherten Speicher nicht automatisch gespeichert werden.

Zertifikat Speicher ähnliche Zertifikat Kontexte können erweiterte Eigenschaften haben. [**Certsetstoreproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty) fügt einem Zertifikat Speicher erweiterte Eigenschaften hinzu. [**Certgetstoreproperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty) Ruft alle Eigenschaften ab, die in einem Zertifikat Speicher festgelegt sind. Derzeit ist die einzige vordefinierte Zertifikat Speicher Eigenschaft ein lokalisierter Name eines Stores.

 

 
