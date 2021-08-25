---
description: Wird mit dem DSS-Anbieter (Digital Signature Standard) verwendet, um Schlüssel aus dem Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) zu exportieren und in diesen zu importieren.
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: DSS-Anbieterschlüssel-BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accbc2cbdc7f543fb2a46b77741d5be7f9e216efcf36b487f7d08912bf5d3991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875320"
---
# <a name="dss-provider-key-blobs"></a>DSS-Anbieterschlüssel-BLOBs

[*BLOBs*](../secgloss/b-gly.md) werden mit dem [*DSS-Anbieter (Digital Signature Standard)*](../secgloss/d-gly.md) verwendet, um Schlüssel aus dem [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) zu exportieren und in diesen zu importieren.

-   [BLOBs mit öffentlichem Schlüssel](#public-key-blobs)
-   [Private Schlüsselblobs](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOBs mit öffentlichem Schlüssel

Ein [*öffentlicher*](../secgloss/p-gly.md) DSS-Schlüssel wird als BLOB exportiert und importiert. Dies ist eine Folge von Bytes, die wie folgt strukturiert ist.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

In der folgenden Tabelle werden diese Komponenten beschrieben. Alle Werte liegen im [*Little-Endian-Format*](../secgloss/l-gly.md) vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Eine [**DSSPUBKEY-Struktur.**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) Der **magic-Member** muss den Wert 0x31535344 haben. Diese Hexadezimalzahl ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von DSS1. |
| g              | Eine **BYTE-Sequenz.** Der Generator, g. Muss die gleiche Länge wie p haben. Wenn sie nicht die gleiche Länge wie p auf hat, muss sie mit 0x00 Bytes aufgefüllt werden.                                                                      |
| p              | Eine **BYTE-Sequenz.** Der Primmodulus, p. Das wichtigste Bit des wichtigsten Byte muss auf eins festgelegt werden.                                                                                                 |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                |
| q              | Eine **BYTE-Sequenz.** Die Primzahl q, 20 Byte lang. Das wichtigste Bit des wichtigsten Byte muss auf eins festgelegt werden.                                                                                     |
| seedstruct     | Eine [**DSSSEED-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) Ausgangswert und Indikatorwerte zum Überprüfen von Primzahlen.                                                                                                                                |
| y              | Eine **BYTE-Sequenz.** Der öffentliche Schlüssel, y. Muss dieselbe Länge wie p haben. Wenn sie nicht die gleiche Länge wie p auf hat, muss sie mit 0x00 Bytes aufgefüllt werden.                                                                         |



 

> [!Note]  
> [*BLOBs mit öffentlichem Schlüssel*](../secgloss/p-gly.md) werden nicht verschlüsselt. Sie enthalten öffentliche Schlüssel in [*Klartextform.*](../secgloss/p-gly.md)

 

## <a name="private-key-blobs"></a>Private Key-BLOBs

Ein [*privater*](../secgloss/p-gly.md) DSS-Schlüssel wird exportiert und als Bytefolge importiert, die wie folgt strukturiert ist.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

In der folgenden Tabelle werden die einzelnen Komponenten beschrieben. Alle Werte liegen im [*Little-Endian-Format*](../secgloss/l-gly.md) vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Eine [**DSSPUBKEY-Struktur.**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) Der **magic-Member** muss auf 0x32535344 festgelegt werden. Diese Hexadezimalzahl ist die [*ASCII-Codierung*](../secgloss/a-gly.md) von DSS2. |
| g              | Eine **BYTE-Sequenz.** Der Generator, g. Muss die gleiche Länge wie p haben. Wenn sie nicht die gleiche Länge wie p auf hat, muss sie mit 0x00 Bytes aufgefüllt werden.                                                                |
| publickeystruc | Eine [**PUBLICKEYSTRUC-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                          |
| p              | Eine **BYTE-Sequenz.** Der Primmodulus, p. Das wichtigste Bit des wichtigsten Byte muss auf eins festgelegt werden.                                                                                           |
| q              | Eine **BYTE-Sequenz.** Die Primzahl q. q hat eine Länge von 20 Bytes. Das wichtigste Bit des wichtigsten Byte muss auf eins festgelegt werden.                                                                          |
| seedstruct     | Eine [**DSSSEED-Struktur.**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) Ausgangswert und Indikatorwerte zum Überprüfen von Primzahlen.                                                                                                                          |
| x              | Eine **BYTE-Sequenz.** Der geheime Exponent x. Muss immer 20 Bytes lang sein. Wenn x kleiner als 20 Bytes ist, muss es mit 0x00 aufgefüllt werden.                                                     |



 

Beim Aufrufen von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. **PRIVATEKEYBLOB** wird verschlüsselt, wenn der *hExpKey-Parameter* ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**PUBLICKEYSTRUC-Teil**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) des BLOB wird verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüsselparameter werden nicht zusammen mit dem BLOB des privaten Schlüssels gespeichert. Die Anwendung muss diese Informationen verwalten und speichern. Wenn 0 (null) für *hExpKey* übergeben wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

 

> [!Caution]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da sie dann anfällig für abfangende und nicht autorisierte Entitäten sind.

 

 

 
