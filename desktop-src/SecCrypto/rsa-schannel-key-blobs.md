---
description: Blobvorgänge werden mit dem RSA/SChannel-Anbieter verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) zu exportieren und Schlüssel in zu importieren.
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: RSA/SChannel-schlüsselblobzugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862831"
---
# <a name="rsaschannel-key-blobs"></a>RSA/SChannel-schlüsselblobzugriff

[*Blobvorgänge*](../secgloss/b-gly.md) werden mit dem [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) -Anbieter verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) zu exportieren und Schlüssel in zu importieren.

-   [Blobschlüssel für öffentliche Schlüssel](#public-key-blobs)
-   [Blobschlüssel für private Schlüssel](#private-key-blobs)
-   [Einfache Schlüsselblob](#simple-key-blobs)

## <a name="public-key-blobs"></a>Blobschlüssel für öffentliche Schlüssel

[*Öffentliche Schlüssel-BLOBs*](../secgloss/p-gly.md), geben Sie **PublicKeyBlob** ein, die zum Speichern [*öffentlicher Schlüssel*](../secgloss/p-gly.md)verwendet werden. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen öffentlichen Schlüsselkomponenten beschrieben. Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Eine **Byte** Sequenz. Die Daten des Datasets mit öffentlichem Schlüssel befinden sich direkt nach der **rsapubkey** -Struktur. Die Länge dieser Daten hängt von der Länge des öffentlichen Schlüssels ab. Die Anzahl der Bytes kann bestimmt werden, indem der Wert des **bitlen** -Members von **rsapubkey** um acht dividiert wird. |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                              |
| rsapubkey      | Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur. Der **Magic** -Member muss auf 0x31415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA1.                                                                                      |



 

> [!Note]  
> Blobblobschlüssel für öffentliche Schlüssel werden nicht verschlüsselt. Sie enthalten öffentliche Schlüssel als [*Klartext*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Blobschlüssel für private Schlüssel

[*Private Schlüsselblobs*](../secgloss/p-gly.md), Typ **privatekeyblob**, werden zum Speichern von [*Paaren aus öffentlichem und privatem Schlüssel*](../secgloss/p-gly.md)verwendet. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

Wenn das [*Schlüsselblob*](../secgloss/k-gly.md) verschlüsselt ist, wird alles, aber der [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert. Es liegt in der Verantwortung der Anwendung, diese Informationen zu verwalten.

 

In der folgenden Tabelle werden die einzelnen BLOB-Komponenten des privaten Schlüssels beschrieben.

> [!Note]  
> Diese Felder entsprechen den im Abschnitt 7,2 von [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) 1 beschriebenen Feldern \# mit geringfügigen Unterschieden.

 



| Feld           | BESCHREIBUNG                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Eine **Byte** Sequenz. Der erste Exponent. Dies hat den numerischen Wert d mod (p – 1).                                                                                                                           |
| exponent2       | Eine **Byte** Sequenz. Der zweite Exponent. Dies hat den numerischen Wert d mod (q – 1).                                                                                                                          |
| Fak     | Eine **Byte** Sequenz. Fak. Dies hat den numerischen Wert (inverse of q) mod p.                                                                                                                           |
| Modulus         | Eine **Byte** Sequenz. Der Modulus. Diese verfügt über eine Zeichenfolge, die *Prime1* \* *Prime2* enthält. Dies wird häufig als n bezeichnet.                                                                                               |
| prime1          | Eine **Byte** Sequenz. Primzahl 1, häufig auch als p bezeichnet.                                                                                                                                                        |
| prime2          | Eine **Byte** Sequenz. Primzahl 2, häufig auch als q bezeichnet.                                                                                                                                                        |
| publickeystruc  | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                         |
| privateexponent | Eine **Byte** Sequenz. Der private Exponent, der häufig als "d" bezeichnet wird.                                                                                                                                                  |
| rsapubkey       | Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur. Der **Magic** -Member muss auf 0x32415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA2. |



 

> [!Note]  
> Blobblobschlüssel für private Schlüssel werden nicht verschlüsselt. Sie enthalten private Schlüssel in Klartext.

 

Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der **privatekeyblob** wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert. Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden. Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

 

> [!Caution]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.

 

## <a name="simple-key-blobs"></a>Einfache Schlüsselblob

[*Einfache Schlüsselblobs*](../secgloss/s-gly.md), geben Sie **simpleblob** ein, die zum Speichern und transportieren von Sitzungs Schlüsseln verwendet werden. Diese werden immer mit einem [*öffentlichen Schlüsselaustausch Schlüssel*](../secgloss/k-gly.md)verschlüsselt. Diese Schlüssel werden als Bytefolge im folgenden Format exportiert und importiert.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

In der folgenden Tabelle wird jede einfache BLOB-Komponente beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Eine [**ALG- \_ ID**](alg-id.md) -Struktur. Dies gibt in der Regel den calg \_ RSA \_ Keyx-Algorithmus an, der angibt, dass die Sitzungsschlüssel Daten mit einem öffentlichen Schlüsselaustausch Schlüssel mithilfe des [*RSA-Algorithmus für öffentliche Schlüssel*](../secgloss/r-gly.md)verschlüsselt wurden. |
| EncryptedKey   | Eine **Byte** Sequenz. Die verschlüsselten Sitzungsschlüssel Daten haben das Format PKCS \# 1, Typ 2-Verschlüsselungs Block. Weitere Informationen zu diesem Datenformat finden Sie unter Public Key Cryptography Standards (PKCS), veröffentlicht von RSA Data Security, Inc.                                                                                     |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                                                         |



 

Diese Daten haben immer die gleiche Größe wie der Modulo des öffentlichen Schlüssels. Öffentliche Schlüssel, die vom Microsoft-Basis Kryptografieanbieter generiert werden, sind z. b. immer 512 Bits (64 Bytes), sodass die verschlüsselten Sitzungsschlüssel Daten immer 64 Bytes sind.

 

 
