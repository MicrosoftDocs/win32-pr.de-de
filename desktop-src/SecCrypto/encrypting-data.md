---
description: Beschreibt die Schritte zum Verschlüsseln einer Nachricht mit den Basiskryptografiefunktionen.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Verschlüsseln von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7d2a7fde500397959f0a2352b3f8ddb4fa662209afb251ddceaa8774048f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874454"
---
# <a name="encrypting-data"></a>Verschlüsseln von Daten

Das folgende Verfahren beschreibt die Schritte zum Verschlüsseln einer Nachricht mit den Basiskryptografiefunktionen. Informationen zum Verschlüsseln von Nachrichten mit PKCS \# 7-Standards finden Sie unter [Low-level Message Functions (Nachrichtenfunktionen](cryptography-functions.md) auf niedriger Ebene) und [Simplified Message Functions (Vereinfachte Nachrichtenfunktionen).](cryptography-functions.md)

**So verschlüsseln Sie eine Nachricht**

1.  Generieren Sie einen Sitzungsschlüssel mithilfe der [**CryptGenKey-Funktion.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)

    Durch diesen Aufruf wird ein zufälliger Schlüssel generiert und ein Handle zurückgegeben, damit der Schlüssel zum Verschlüsseln und Entschlüsseln von Daten verwendet werden kann. Der zu verwendende Verschlüsselungsalgorithmus wird an diesem Punkt ebenfalls angegeben. Da CryptoAPI es Anwendungen nicht erlaubt, Algorithmen mit öffentlichem Schlüssel zum Verschlüsseln von Massendaten zu verwenden, geben Sie mit dem [**CryptGenKey-Aufruf**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) einen symmetrischen Algorithmus wie RC2 oder RC4 an.

2.  Alternativ können Sie die [**CryptDeriveKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) verwenden, um ein Kennwort in einen Schlüssel zu transformieren, der für die Verschlüsselung geeignet ist.

    Wenn eine Anwendung die Nachricht verschlüsseln muss, damit alle Benutzer mit einem angegebenen Kennwort die Daten entschlüsseln können, verwenden Sie [**CryptDeriveKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) um das Kennwort in einen Schlüssel zu transformieren, der für die Verschlüsselung geeignet ist.

    > [!Note]  
    > In diesem Fall wird diese Funktion anstelle der [**CryptGenKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) aufgerufen, und die nachfolgenden [**CryptExportKey-Aufrufe**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) sind nicht erforderlich.

     

3.  Legen Sie bei Bedarf zusätzliche kryptografische Eigenschaften des Schlüssels mithilfe der [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) fest.

    Nachdem der Schlüssel generiert wurde, können zusätzliche kryptografische Eigenschaften des Schlüssels mit der [**CryptSetKeyParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)festgelegt werden. Diese Funktion ermöglicht die Verschlüsselung verschiedener Abschnitte der Datei mit unterschiedlichen Schlüssel salts und bietet eine Möglichkeit, den Verschlüsselungsmodus oder Initialisierungsvektor des Schlüssels zu ändern. Diese Parameter können verwendet werden, um die Verschlüsselung einem bestimmten Datenverschlüsselungsstandard zu entsprechen.

4.  Verschlüsseln Sie die Daten in der Datei mit der [**CryptEncrypt-Funktion.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt)

    Die [**CryptEncrypt-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) übernimmt den Sitzungsschlüssel, der im vorherigen Schritt generiert wurde, und verschlüsselt einen Datenpuffer.

    > [!Note]  
    > Wenn die Daten verschlüsselt werden, können die Daten durch den Verschlüsselungsalgorithmus leicht erweitert werden. Die Anwendung ist dafür verantwortlich, die Länge der verschlüsselten Daten zu speichern, damit später die richtige Länge für die [**CryptDecrypt-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) angegeben werden kann.

     

5.  Verwenden Sie optional die [**CryptExportKey-Funktion,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) damit der aktuelle Benutzer die Daten in Zukunft entschlüsseln kann.

    Damit der aktuelle Benutzer die Daten in Zukunft entschlüsseln kann, wird die [**CryptExportKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) verwendet, um den Entschlüsselungsschlüssel in verschlüsselter Form (einem Schlüssel-BLOB) zu speichern, der nur mit dem privaten Schlüssel des Benutzers entschlüsselt werden kann. Diese Funktion erfordert den öffentlichen Schlüsselaustauschschlüssel des Benutzers für diesen Zweck, der mithilfe der [**CryptGetUserKey-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) abgerufen werden kann. Die **CryptExportKey-Funktion** gibt ein Schlüsselblob zurück, das von der Anwendung gespeichert werden muss, damit die Datei entschlüsselt werden kann.

> [!Note]  
> Wenn die Anwendung über Zertifikate (oder öffentliche Schlüssel) für andere Benutzer verfügt, kann sie anderen Benutzern erlauben, die Datei zu entschlüsseln, indem [**sie CryptExportKey-Aufrufe**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) für jeden Benutzer ausführt, der Zugriff erhalten soll. Die zurückgegebenen Schlüssel-BLOBs müssen wie in Schritt 5 von der Anwendung gespeichert werden.

 

## <a name="creating-an-encrypted-message"></a>Erstellen einer verschlüsselten Nachricht

Die vereinfachten Nachrichtenfunktionen erleichtern das Verschlüsseln und Entschlüsseln von Daten. Die folgende Abbildung zeigt die einzelnen Aufgaben, die zum Verschlüsseln einer Nachricht ausgeführt werden müssen. Die Schritte werden in der folgenden Liste beschrieben.

![Verschlüsseln einer Nachricht](images/encmsg.png)

**So verschlüsseln Sie eine Nachricht**

1.  Abrufen eines Zeigers auf die Klartextnachricht.
2.  Generieren Sie einen symmetrischen Schlüssel (Sitzungsschlüssel).
3.  Verschlüsseln Sie die Nachrichtendaten mithilfe des symmetrischen Schlüssels und des angegebenen Verschlüsselungsalgorithmus.
4.  Öffnen Sie einen Zertifikatspeicher.
5.  Abrufen des Zertifikats des Empfängers.
6.  Abrufen des öffentlichen Schlüssels aus dem Zertifikat des Empfängers.
7.  Verschlüsseln Sie den symmetrischen Schlüssel mithilfe des öffentlichen Schlüssels des Empfängers.
8.  Abrufen des Empfängerbezeichners aus dem Zertifikat des Empfängers.
9.  Fügen Sie Folgendes in die DigitalUmschlagnachricht ein: den Datenverschlüsselungsalgorithmus, die verschlüsselten Daten, den verschlüsselten symmetrischen Schlüssel und den Empfängerbezeichner.

 

 



