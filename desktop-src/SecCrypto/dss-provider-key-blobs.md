---
description: Wird mit dem DSS-Anbieter (Digital Signature Standard) zum Exportieren von Schlüsseln aus und Importieren von Schlüsseln in den Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) verwendet.
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Schlüssel-blobschlüssel des DSS-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958838"
---
# <a name="dss-provider-key-blobs"></a>Schlüssel-blobschlüssel des DSS-Anbieters

[*Blobvorgänge*](../secgloss/b-gly.md) werden mit dem DSS-Anbieter ( [*Digital Signature Standard*](../secgloss/d-gly.md) ) zum Exportieren von Schlüsseln und Importieren von Schlüsseln in den [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) verwendet.

-   [Blobschlüssel für öffentliche Schlüssel](#public-key-blobs)
-   [Blobschlüssel für private Schlüssel](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobschlüssel für öffentliche Schlüssel

Ein öffentlicher DSS- [*Schlüssel*](../secgloss/p-gly.md) wird exportiert und als BLOB importiert, eine Folge von Bytes, die wie folgt strukturiert ist.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

In der folgenden Tabelle werden diese Komponenten beschrieben. Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Eine [**dsspubkey**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) -Struktur. Der **magische** Member muss den Wert 0x31535344 aufweisen. Diese hexadezimal Zahl ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DSS1. |
| g              | Eine **Byte** Sequenz. Der Generator, g. Muss dieselbe Länge wie p aufweisen. Wenn Sie nicht die gleiche Länge wie p hat, muss Sie mit 0x00 Bytes aufgefüllt werden.                                                                      |
| p              | Eine **Byte** Sequenz. Der primmodulus (p). Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.                                                                                                 |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                                |
| q              | Eine **Byte** Sequenz. Die Länge von Primzahlen, q, 20 Bytes. Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.                                                                                     |
| seedstruct     | Eine [**dssseed**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) -Struktur. Seed-und Counter-Werte zum Überprüfen von primes.                                                                                                                                |
| Y              | Eine **Byte** Sequenz. Der öffentliche Schlüssel y. Muss dieselbe Länge wie p aufweisen. Wenn Sie nicht die gleiche Länge wie p hat, muss Sie mit 0x00 Bytes aufgefüllt werden.                                                                         |



 

> [!Note]  
> [*Blobblobschlüssel für öffentliche Schlüssel*](../secgloss/p-gly.md) werden nicht verschlüsselt. Sie enthalten öffentliche Schlüssel als [*Klartext*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Blobschlüssel für private Schlüssel

Ein privater DSS- [*Schlüssel*](../secgloss/p-gly.md) wird exportiert und als Sequenz von Bytes importiert, die wie folgt strukturiert ist.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

In der folgenden Tabelle werden die einzelnen Komponenten beschrieben. Alle Werte liegen im [*Little-Endian-*](../secgloss/l-gly.md) Format vor.



| Feld          | BESCHREIBUNG                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Eine [**dsspubkey**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) -Struktur. Der **Magic** -Member muss auf 0x32535344 festgelegt werden. Diese hexadezimal Zahl ist die [*ASCII*](../secgloss/a-gly.md) -Codierung von DSS2. |
| g              | Eine **Byte** Sequenz. Der Generator, g. Muss dieselbe Länge wie p aufweisen. Wenn Sie nicht die gleiche Länge wie p hat, muss Sie mit 0x00 Bytes aufgefüllt werden.                                                                |
| publickeystruc | Eine [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Struktur.                                                                                                                                                          |
| p              | Eine **Byte** Sequenz. Der primmodulus (p). Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.                                                                                           |
| q              | Eine **Byte** Sequenz. Die Primzahl, f. q ist eine Länge von 20 Bytes. Das signifikanteste Bit des signifikantesten muss auf 1 festgelegt werden.                                                                          |
| seedstruct     | Eine [**dssseed**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) -Struktur. Seed-und Counter-Werte zum Überprüfen von primes.                                                                                                                          |
| x              | Eine **Byte** Sequenz. Der geheime Exponent, x. Muss immer 20 Byte lang sein. Wenn x kleiner als 20 Bytes ist, muss es mit 0x00 aufgefüllt werden.                                                     |



 

Wenn Sie [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)aufrufen, kann der Entwickler auswählen, ob der Schlüssel verschlüsselt werden soll. Der **privatekeyblob** wird verschlüsselt, wenn der *hexpkey* -Parameter ein gültiges Handle für einen Sitzungsschlüssel enthält. Alles außer dem [**publickeystruc**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) -Teil des BLOBs wird verschlüsselt.

> [!Note]  
> Der Verschlüsselungsalgorithmus und die Verschlüsselungsschlüssel Parameter werden nicht zusammen mit dem BLOB für den privaten Schlüssel gespeichert. Diese Informationen müssen von der Anwendung verwaltet und gespeichert werden. Wenn 0 (null) für *hexpkey* übermittelt wird, wird der private Schlüssel ohne Verschlüsselung exportiert.

 

> [!Caution]  
> Es ist gefährlich, private Schlüssel ohne Verschlüsselung zu exportieren, da Sie dann anfällig für das Abfangen und die Verwendung durch nicht autorisierte Entitäten sind.

 

 

 
