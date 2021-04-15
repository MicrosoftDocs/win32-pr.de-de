---
description: Nicht transparente BLOB-(auch als "opaquekeyblob" bezeichnet) werden zum Speichern von Sitzungs Schlüsseln in einem herstellerspezifischen Format verwendet, z. b. Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Nicht transparenter BLOB-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393769"
---
# <a name="opaque-blob-type"></a>Nicht transparenter BLOB-Typ

Nicht transparente [*BLOB*](../secgloss/o-gly.md)-(auch als "opaquekeyblob" bezeichnet) werden zum Speichern von [*Sitzungs Schlüsseln*](../secgloss/s-gly.md) in einem herstellerspezifischen Format verwendet, z. b. [*SChannel*](../secgloss/s-gly.md). Sie enthalten das Basis Schlüsselmaterial und alle aktuellen [*Zustands*](../secgloss/s-gly.md) Informationen. Dies schließt Informationen wie den [*Salt-Wert*](../secgloss/s-gly.md), den [*Initialisierungs Vektor*](../secgloss/i-gly.md)und die Schlüssel Tabelle ein. Das Format von nicht transparenten blobbden ist nicht veröffentlicht. Jeder CSP-Anbieter bestimmt sein eigenes BLOB-Format.

Da ein Schlüssel in ein nicht transparentes BLOB im CSP-spezifischen Format exportiert wird, kann er nur in den CSP importiert werden, von dem er ursprünglich exportiert wurde.

Wenn zwei Prozesse beteiligt sind, ruft [](../secgloss/p-gly.md) jeder Prozess [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) unabhängig auf. Jeder Prozess erhält ein Handle für einen Schlüssel Container. Beide Prozesse können über Handles für denselben Schlüssel Container verfügen. Ein Prozess erstellt die Schlüssel und exportiert Sie in nicht transparente blobwerte und übergibt dann die blobwerte an den zweiten Prozess. Der zweite Prozess importiert die Schlüssel aus dem BLOB in den [*Schlüssel Container*](../secgloss/k-gly.md).

Wenn ein Hardware-CSP den Export von Schlüsseln nicht unterstützt, enthält das BLOB möglicherweise nur den Index eines Schlüssel Registers oder etwas ähnliches. In diesem Fall wird der restliche Vorgang ignoriert.

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
