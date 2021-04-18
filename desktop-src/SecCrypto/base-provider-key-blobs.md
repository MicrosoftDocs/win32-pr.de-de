---
description: Der Basis Anbieter und der erweiterte Anbieter verwenden dieselben Schlüsselblob.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: Schlüssel-BLOB des Basis Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c763f97fe6e7868246e0bce30ee2a741e8bd212f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345751"
---
# <a name="base-provider-key-blobs"></a>Schlüssel-BLOB des Basis Anbieters

Der Basis Anbieter und der erweiterte Anbieter verwenden dieselben [*Schlüsselblob*](../secgloss/k-gly.md).

-   [Blobschlüssel für öffentliche Schlüssel](#public-key-blobs)
-   [Blobschlüssel für private Schlüssel](#private-key-blobs)
-   [Einfache Schlüsselblob](#simple-key-blobs)

## <a name="public-key-blobs"></a>Blobschlüssel für öffentliche Schlüssel

[*Öffentliche Schlüssel-BLOBs*](../secgloss/p-gly.md), geben Sie **PublicKeyBlob** ein, die verwendet werden, um [*öffentliche Schlüssel*](../secgloss/p-gly.md) außerhalb eines [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) zu speichern. BLOB für öffentliche Schlüssel des Basis Anbieters haben das folgende Format:

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen öffentlichen Schlüsselkomponenten beschrieben. Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulus        | Die Daten des Datasets mit öffentlichem Schlüssel befinden sich direkt nach der [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur. Die Größe dieser Daten hängt von der Größe des öffentlichen Schlüssels ab. Die Anzahl der Bytes kann bestimmt werden, indem der Wert des Felds **rsapubkey bitlen** durch acht dividiert wird. |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                 |
| rsapubkey      | Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur. Der **Magic** -Member muss auf 0x31415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA1.                                                                         |



 

> [!Note]  
> Blobblobschlüssel für öffentliche Schlüssel werden nicht verschlüsselt. Sie enthalten öffentliche Schlüssel als [*Klartext*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Blobschlüssel für private Schlüssel

[*Private Schlüsselblobs*](../secgloss/p-gly.md), Typ **privatekeyblob**, werden zum Speichern [*privater Schlüssel*](../secgloss/p-gly.md) außerhalb eines CSP verwendet. Die BLOB des privaten Schlüssels des Basis Anbieters haben das folgende Format.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

In der folgenden Tabelle wird die BLOB-Komponente des privaten Schlüssels beschrieben.

> [!Note]  
> Diese Felder entsprechen den im Abschnitt 7,2 von [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) 1 beschriebenen Feldern \# mit geringfügigen Unterschieden.

 



| Feld           | BESCHREIBUNG                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fak     | Fak. Dies hat den numerischen Wert (inverse of q) mod p.                                                                                                                                                |
| exponent1       | Exponent 1. Dies hat den numerischen Wert d mod (p – 1).                                                                                                                                                        |
| exponent2       | Exponent 2. Dies hat den numerischen Wert d mod (q – 1).                                                                                                                                                        |
| Modulus         | Der Modulus. Dies hat den Wert *Prime1*×*Prime2* und wird häufig als n bezeichnet.                                                                                                                                   |
| prime1          | Primzahl 1, häufig auch als p bezeichnet.                                                                                                                                                                             |
| prime2          | Primzahl 2, häufig auch als q bezeichnet.                                                                                                                                                                             |
| privateexponent | Privater Exponent, der häufig als "d" bezeichnet wird.                                                                                                                                                                           |
| publickeystruc  | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                         |
| rsapubkey       | Eine [**rsapubkey**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) -Struktur. Der **Magic** -Member muss auf 0x32415352 festgelegt werden. Dieser Hexadezimalwert ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von RSA2. |



 

> [!Note]  
> Blobblobschlüssel für private Schlüssel werden nicht verschlüsselt. Sie enthalten private Schlüssel in Klartext.

 

Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der **privatekeyblob** wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert. Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden. Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

 

> [!Caution]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.

 

## <a name="simple-key-blobs"></a>Einfache Schlüsselblob

[*Einfache Schlüsselblobs*](../secgloss/s-gly.md), geben Sie **simpleblob** ein, die zum Speichern und transportieren von Sitzungs Schlüsseln außerhalb eines CSP verwendet werden. Einfache Schlüssel-BLOB des Basis Anbieters werden immer mit einem [*öffentlichen Schlüsselaustausch*](../secgloss/k-gly.md)Schlüssel verschlüsselt. Der **pbData** -Member von **simpleblob** ist eine Folge von Bytes im folgenden Format.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

In der folgenden Tabelle werden die einzelnen Komponenten des **pbData** -Members von **simpleblob** beschrieben.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Eine [**ALG- \_ ID**](alg-id.md) -Struktur, die den Verschlüsselungsalgorithmus angibt, mit dem die Sitzungsschlüssel Daten verschlüsselt werden. Dabei handelt es sich in der Regel um den Wert calg \_ RSA \_ Keyx, der angibt, dass die Sitzungsschlüssel Daten mit einem öffentlichen Schlüsselaustausch Schlüssel mithilfe des [*RSA-Algorithmus für öffentliche Schlüssel*](../secgloss/r-gly.md)verschlüsselt wurden.                                                                                                                           |
| EncryptedKey   | Eine **Byte** Sequenz, die die verschlüsselten Sitzungsschlüssel Daten in Form eines PKCS 1- \# , Typ-2-Verschlüsselungs Blocks darstellt. Weitere Informationen zu diesem Datenformat finden Sie unter Public Key Cryptography Standards (PKCS) \# 1, veröffentlicht von RSA Data Security, Inc. Diese Daten haben immer die gleiche Größe wie der Modulo des öffentlichen Schlüssels. Beispielsweise können öffentliche Schlüssel, die vom Microsoft RSA-Basis Anbieter generiert werden, 512 Bits (64 Bytes) sein, sodass die verschlüsselten Sitzungsschlüssel Daten auch immer 512 Bits (64 Bytes) sind.<br/> |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
