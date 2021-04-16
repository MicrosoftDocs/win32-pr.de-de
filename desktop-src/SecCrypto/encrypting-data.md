---
description: Beschreibt die Schritte, die zum Verschlüsseln einer Nachricht mit den grundlegenden Kryptografiefunktionen erforderlich sind.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Verschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566527"
---
# <a name="encrypting-data"></a>Verschlüsseln von Daten

Im folgenden Verfahren werden die Schritte beschrieben, die zum Verschlüsseln einer Nachricht mit den grundlegenden Kryptografiefunktionen erforderlich sind. Informationen zum Verschlüsseln von Nachrichten mit PKCS \# 7-Standards finden Sie unter [Nachrichten Funktionen auf niedriger Ebene](cryptography-functions.md) und [vereinfachte Nachrichten Funktionen](cryptography-functions.md).

**So verschlüsseln Sie eine Nachricht**

1.  Generieren Sie einen Sitzungsschlüssel mithilfe der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion.

    Durch diesen Befehl wird ein zufälliger Schlüssel generiert und ein Handle zurückgegeben, damit der Schlüssel zum Verschlüsseln und Entschlüsseln von Daten verwendet werden kann. Der zu verwendende Verschlüsselungsalgorithmus wird an dieser Stelle ebenfalls angegeben. Da CryptoAPI nicht zulässt, dass Anwendungen öffentliche Schlüssel Algorithmen zum Verschlüsseln von Massendaten verwenden, geben Sie einen symmetrischen Algorithmus wie RC2 oder RC4 mit dem [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Aufruf an.

2.  Verwenden Sie alternativ die [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) -Funktion, um ein Kennwort in einen Schlüssel umzuwandeln, der für die Verschlüsselung geeignet ist.

    Wenn eine Anwendung die Nachricht verschlüsseln muss, damit alle Benutzer mit einem bestimmten Kennwort die Daten entschlüsseln können, verwenden Sie [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) , um das Kennwort in einen Schlüssel zu transformieren, der für die Verschlüsselung geeignet ist.

    > [!Note]  
    > In diesem Fall wird diese Funktion anstelle der [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) -Funktion aufgerufen, und die nachfolgenden [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Aufrufe werden nicht benötigt.

     

3.  Legen Sie bei Bedarf zusätzliche kryptografieeigenschaften des Schlüssels mithilfe der [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) -Funktion fest.

    Nachdem der Schlüssel generiert wurde, können zusätzliche kryptografieeigenschaften des Schlüssels mit der [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)-Funktion festgelegt werden. Diese Funktion ermöglicht, dass verschiedene Abschnitte der Datei mit anderen Schlüssel Salzen verschlüsselt werden und eine Möglichkeit zum Ändern des Verschlüsselungs Modus oder Initialisierungs Vektors des Schlüssels bietet. Diese Parameter können verwendet werden, um die Verschlüsselung einem bestimmten Daten Verschlüsselungsstandard zu entsprechen.

4.  Verschlüsseln Sie die Daten in der Datei mit der [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) -Funktion.

    Die [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) -Funktion nimmt den im vorherigen Schritt generierten Sitzungsschlüssel an und verschlüsselt einen Datenpuffer.

    > [!Note]  
    > Wenn die Daten verschlüsselt werden, werden die Daten möglicherweise durch den Verschlüsselungsalgorithmus leicht erweitert. Die Anwendung ist dafür verantwortlich, die Länge der verschlüsselten Daten zu merken, damit die richtige Länge später für die [**cryptentschlpt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) -Funktion angegeben werden kann.

     

5.  Verwenden Sie optional die [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion, um dem aktuellen Benutzer zu gestatten, die Daten in der Zukunft zu entschlüsseln.

    Damit der aktuelle Benutzer die Daten zukünftig entschlüsseln kann, wird die [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Funktion verwendet, um den Entschlüsselungsschlüssel in verschlüsselter Form (einem Schlüsselblob) zu speichern, die nur mit dem privaten Schlüssel des Benutzers entschlüsselt werden kann. Diese Funktion erfordert zu diesem Zweck den öffentlichen Schlüsselaustausch Schlüssel des Benutzers, der über die Funktion " [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) " abgerufen werden kann. Die **CryptExportKey** -Funktion gibt ein Schlüssel-BLOB zurück, das von der Anwendung für die Verwendung beim Entschlüsseln der Datei gespeichert werden muss.

> [!Note]  
> Wenn die Anwendung Zertifikate (oder öffentliche Schlüssel) für andere Benutzer aufweist, können andere Benutzer die Datei entschlüsseln, indem Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) -Aufrufe für jeden Benutzer ausführen, der Zugriff erhalten soll. Die zurückgegebenen schlüsselblobspeicher müssen von der Anwendung gespeichert werden, wie in Schritt 5.

 

## <a name="creating-an-encrypted-message"></a>Erstellen einer verschlüsselten Nachricht

Die vereinfachten Nachrichten Funktionen erleichtern das Verschlüsseln und Entschlüsseln von Daten. Die folgende Abbildung zeigt die einzelnen Aufgaben, die zum Verschlüsseln einer Nachricht durchgeführt werden müssen. Die Schritte werden in der folgenden Liste beschrieben.

![Verschlüsseln einer Nachricht](images/encmsg.png)

**So verschlüsseln Sie eine Nachricht**

1.  Einen Zeiger auf die Klartext-Nachricht erhalten.
2.  Generieren Sie einen symmetrischen (Sitzungs-) Schlüssel.
3.  Verschlüsseln Sie die Nachrichten Daten mithilfe des symmetrischen Schlüssels und des angegebenen Verschlüsselungsalgorithmus.
4.  Öffnen Sie einen Zertifikat Speicher.
5.  Das Zertifikat des Empfängers erhalten.
6.  Den öffentlichen Schlüssel aus dem Zertifikat des Empfängers erhalten.
7.  Verschlüsseln Sie den symmetrischen Schlüssel mithilfe des öffentlichen Schlüssels des Empfängers.
8.  Den Bezeichner des Empfängers aus dem Zertifikat des Empfängers erhalten.
9.  Fügen Sie Folgendes in die Digital eingeschlossene Nachricht ein: den Daten Verschlüsselungsalgorithmus, die verschlüsselten Daten, den verschlüsselten symmetrischen Schlüssel und den Empfänger Bezeichner.

 

 



