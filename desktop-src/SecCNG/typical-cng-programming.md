---
description: Die CNG-API implementiert ein erweiterbares Anbietermodell, mit dem Sie einen Anbieter laden können, indem Sie den erforderlichen kryptografischen Algorithmus anstelle eines bestimmten Anbieters angeben.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Typische CNG-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1cd45c68d7c34c3815008690b49cabfefff437222b29512abbf858cf3b370f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905521"
---
# <a name="typical-cng-programming"></a>Typische CNG-Programmierung

Die CNG-API implementiert ein erweiterbares Anbietermodell, mit dem Sie einen Anbieter laden können, indem Sie den erforderlichen kryptografischen Algorithmus anstelle eines bestimmten Anbieters angeben. Der Vorteil ist, dass ein Algorithmusanbieter ersetzt oder aktualisiert werden kann und Sie Ihren Code nicht ändern müssen, um den neuen Anbieter zu verwenden. Wenn ein Algorithmus in Zukunft als unsicher eingestuft wird, kann auch eine sicherere Version dieses Algorithmus installiert werden, ohne den Code zu beeinträchtigen. Die meisten CNG-APIs erfordern einen Anbieter oder ein von einem Anbieter erstelltes Objekt.

Die typischen Schritte für die Verwendung der CNG-API für kryptografische primitive Vorgänge sind die folgenden:

1.  Öffnen des Algorithmusanbieters
2.  Abrufen oder Festlegen von Algorithmuseigenschaften
3.  Erstellen oder Importieren eines Schlüssels
4.  Ausführen kryptografischer Vorgänge
5.  Schließen des Algorithmusanbieters

Weitere Informationen finden Sie unter Programmierbeispiele.

## <a name="opening-the-algorithm-provider"></a>Öffnen des Algorithmusanbieters

Die [**BCryptOpenAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) bietet Ihnen ein Algorithmusanbieterhandl, das in nachfolgenden CNG-APIs wie [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) oder [**BCryptGenerateKeyPair verwendet wird.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair)

## <a name="getting-or-setting-algorithm-properties"></a>Abrufen oder Festlegen von Algorithmuseigenschaften

Sie können das Handle des Algorithmusanbieters verwenden, um Implementierungsdetails für den Algorithmus zu erhalten, z. B. die Schlüsselgröße oder den aktuellen Betriebsmodus. Sie verwenden die [**BCryptGetProperty-Funktion,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) um bestimmte Eigenschaften zu erhalten.

Sie können auch die Eigenschaften des Algorithmus ändern. Wenn Sie z. B. DIE BLOCKCHIFFR-Verschlüsselung mit AES verwenden möchten, legen Sie die **BCRYPT \_ CHAINING \_ MODE-Eigenschaft** eines AES-Algorithmus auf **BCRYPT \_ CHAIN MODE \_ \_ 2016 FEST.** Die Eigenschaft wird allen AES-Schlüsseln zugewiesen, die mit diesem Algorithmushand handle erstellt wurden, ohne dass jeder AES-Schlüssel konfiguriert werden muss. Sie verwenden die [**BCryptSetProperty-Funktion,**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) um diese Eigenschaften zu ändern.

## <a name="creating-or-importing-a-key"></a>Erstellen oder Importieren eines Schlüssels

Je nach Typ des verwendeten Algorithmus müssen Sie möglicherweise einen Schlüssel erstellen oder laden. Beispielsweise verwendet die [**BCryptEncrypt-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) ein Schlüsselhand handle für den ersten Parameter. Wenn diese Funktion Daten mit einem symmetrischen Verschlüsselungsalgorithmus wie AES verschlüsseln soll, müssen Sie zunächst einen Schlüssel abrufen. Wie Sie den Schlüssel abrufen, hängt vom Verwendeten Algorithmustyp und der Quelle des Schlüssels ab.

Sie können kurzlebige Schlüssel mit den [**Funktionen BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) und [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) erstellen. Sie können auch kurzlebige Schlüssel aus einem Speicherblob mit den [**Funktionen BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) und [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) importieren.

Für persistente Schlüssel verwenden Sie die Schlüsselspeicherfunktionen, um einen Schlüsselspeicheranbieter zu laden und die Schlüssel anschließend zu erstellen oder zu laden. Sie können diese Funktionen auch verwenden, um kurzlebigen Schlüssel zu erstellen oder zu laden, indem Sie **NULL** für alle Containernamen übergeben. Weitere Informationen zu den schlüsseln Speicherfunktionen finden Sie unter [CNG Key Storage Functions](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Ausführen kryptografischer Vorgänge

Sie können nun den kryptografischen Vorgang ausführen, z. B. das Verschlüsseln oder Entschlüsseln von Daten mithilfe der [**Funktionen BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) bzw. [**BCryptDecrypt.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt)

## <a name="closing-the-algorithm-provider"></a>Schließen des Algorithmusanbieters

Wenn der Anbieter nicht mehr benötigt wird, müssen Sie das Handle an die [**BCryptCloseAlgorithmProvider-Funktion**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) übergeben, um den Anbieter zu schließen. Dies bewirkt, dass der Anbieter alle Ressourcen frei gibt, die dieser Algorithmusanbieterinstanz zugeordnet wurden. Nachdem ein Anbieterhand handle geschlossen wurde, kann es nicht mehr wiederverwendet werden.

Das Laden eines Anbieters kann ein relativ zeitintensiver Prozess sein. Daher sollten Sie alle Anbieterhandles zwischenspeichern, auf die Sie während der Lebensdauer Ihrer Anwendung mehrmals verweisen.

## <a name="programming-examples"></a>Programmierbeispiele

In den folgenden Beispielen wird beschrieben, wie sie bestimmte kryptografische Vorgänge mit CNG ausführen.

-   [Erstellen eines Hashs mit CNG](creating-a-hash-with-cng.md)
-   [Signieren von Daten mit CNG](signing-data-with-cng.md)
-   [Verschlüsseln von Daten mit CNG](encrypting-data-with-cng.md)

 

 



