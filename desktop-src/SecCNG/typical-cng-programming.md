---
description: Die CNG-API implementiert ein erweiterbares Anbieter Modell, mit dem Sie einen Anbieter laden können, indem Sie anstelle eines bestimmten Anbieters den erforderlichen Kryptografiealgorithmus angeben.
ms.assetid: a88a089b-4afe-4201-96f7-97f19bce18a1
title: Typische CNG-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1119da63ca1ea0613444b150914c06664f36c121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751657"
---
# <a name="typical-cng-programming"></a>Typische CNG-Programmierung

Die CNG-API implementiert ein erweiterbares Anbieter Modell, mit dem Sie einen Anbieter laden können, indem Sie anstelle eines bestimmten Anbieters den erforderlichen Kryptografiealgorithmus angeben. Der Vorteil besteht darin, dass ein Algorithmusanbieter ersetzt oder aktualisiert werden kann, und Sie müssen den Code nicht in irgendeiner Weise ändern, um den neuen Anbieter zu verwenden. Wenn ein Algorithmus in Zukunft als unsicher eingestuft wird, kann auch eine sicherere Version dieses Algorithmus installiert werden, ohne dass sich dies auf den Code auswirkt. Die meisten CNG-APIs erfordern einen Anbieter oder ein Objekt, das von einem Anbieter erstellt wurde.

Die üblichen Schritte bei der Verwendung der CNG-API für kryptografische primitive Vorgänge sind wie folgt:

1.  Öffnen des Algorithmusanbieters
2.  Festlegen oder Festlegen von algorithmuseigenschaften
3.  Erstellen oder Importieren eines Schlüssels
4.  Ausführen kryptografischer Vorgänge
5.  Schließen des Algorithmusanbieters

Weitere Informationen finden Sie unter Programmieren von Beispielen.

## <a name="opening-the-algorithm-provider"></a>Öffnen des Algorithmusanbieters

Die Funktion " [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) " bietet ein algorithmusanbieterhandle, das in nachfolgenden CNG-APIs verwendet wird, z. [**b. bcryptkreatehash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) oder [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair).

## <a name="getting-or-setting-algorithm-properties"></a>Festlegen oder Festlegen von algorithmuseigenschaften

Sie können das algorithmusanbieterhandle verwenden, um Implementierungsdetails für den Algorithmus zu erhalten, z. b. die Schlüsselgröße oder den aktuellen Betriebsmodus. Sie verwenden die Funktion " [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) ", um bestimmte Eigenschaften abzurufen.

Sie können auch die Eigenschaften des Algorithmus ändern. Wenn Sie z. b. die ECB-Block Verschlüsselungs Verkettung mit AES verwenden möchten, legen Sie die Eigenschaft **bcrypt- \_ Verkettungs \_ Modus** eines AES-Algorithmus auf **bcrypt \_ Chain \_ Mode \_ ECB** fest. die Eigenschaft wird allen mit diesem algorithmushandle erstellten AES-Schlüsseln zugewiesen, ohne dass jeder AES-Schlüssel konfiguriert werden muss. Sie verwenden die Funktion " [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) ", um diese Eigenschaften zu ändern.

## <a name="creating-or-importing-a-key"></a>Erstellen oder Importieren eines Schlüssels

Abhängig vom verwendeten Algorithmustyp müssen Sie möglicherweise einen Schlüssel erstellen oder laden. Die Funktion [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) nimmt z. b. ein Schlüssel Handle für den ersten Parameter an. Wenn diese Funktion Daten mit einem symmetrischen Verschlüsselungsalgorithmus wie z. b. AES verschlüsseln soll, müssen Sie zuerst einen Schlüssel abrufen. Wie Sie den Schlüssel abrufen, hängt vom verwendeten Algorithmustyp und der Quelle des Schlüssels ab.

Sie können kurzlebige Schlüssel mit den Funktionen [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) und [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) erstellen. Sie können auch kurzlebige Schlüssel aus einem speicherblob mit den Funktionen " [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) " und " [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) " importieren.

Bei persistenten Schlüsseln verwenden Sie die Schlüsselspeicher Funktionen, um einen Schlüsselspeicher Anbieter zu laden und dann die Schlüssel zu erstellen oder zu laden. Sie können diese Funktionen auch zum Erstellen oder Laden von kurzlebigen Schlüsseln verwenden, indem Sie **null** für alle Container Namen übergeben. Weitere Informationen zu den wichtigsten Speicherfunktionen finden Sie unter [CNG-Schlüsselspeicher Funktionen](cng-key-storage-functions.md).

## <a name="performing-cryptographic-operations"></a>Ausführen kryptografischer Vorgänge

Sie sind nun bereit, den kryptografischen Vorgang auszuführen, z. b. das Verschlüsseln oder Entschlüsseln von Daten mit den Funktionen [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) bzw. [**bcryptentschlpt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .

## <a name="closing-the-algorithm-provider"></a>Schließen des Algorithmusanbieters

Wenn der Anbieter nicht mehr benötigt wird, müssen Sie das Handle an die Funktion " [**bcryptclosealgorithmprovider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) " übergeben, um den Anbieter zu schließen. Dies bewirkt, dass der Anbieter alle Ressourcen freigibt, die für die Instanz des Algorithmusanbieters reserviert wurden. Nachdem ein Anbieter Handle geschlossen wurde, kann es nicht wieder verwendet werden.

Das Laden eines Anbieters kann ein relativ Zeit intensiver Prozess sein. Daher sollten Sie alle Anbieter Handles Zwischenspeichern, die während der Lebensdauer der Anwendung mehrmals referenziert werden.

## <a name="programming-examples"></a>Programmierbeispiele

In den folgenden Beispielen wird beschrieben, wie bestimmte Kryptografievorgänge mithilfe von CNG durchgeführt werden.

-   [Erstellen eines Hash mit CNG](creating-a-hash-with-cng.md)
-   [Signieren von Daten mit CNG](signing-data-with-cng.md)
-   [Verschlüsseln von Daten mit CNG](encrypting-data-with-cng.md)

 

 



