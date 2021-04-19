---
description: Sowohl der Basis Anbieter als auch der erweiterte Anbieter können den Wert und die Länge des zu verwendenden Salt-Werts angeben. Der Basis Anbieter legt einen Salt-Wert mit dem Wert des KP- \_ Salt-Parameters fest. Der Basis Anbieter legt immer elf Bytes an Salt-Wert fest.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Angeben eines Salt-Werts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369881"
---
# <a name="specifying-a-salt-value"></a>Angeben eines Salt-Werts

Sowohl der Basis Anbieter als auch der erweiterte Anbieter können den Wert und die Länge des zu verwendenden [*Salt-Werts*](../secgloss/s-gly.md) angeben. Der Basis Anbieter legt einen Salt-Wert mit dem Wert des KP- \_ Salt-Parameters fest. Der Basis Anbieter legt immer elf Bytes an Salt-Wert fest.

Der erweiterte Anbieter legt den Salt-Wert fest, indem er [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mit dem Parameterwert "KP Salt Ex" aufruft, \_ \_ und mit dem *pbData* -Parameter, der auf eine [**crypt- \_ \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) -Struktur mit dem Salt-Wert verweist.

> [!Note]  
> Die Gesamtlänge eines [*symmetrischen*](../secgloss/s-gly.md) Anbieters des erweiterten Anbieters und des Salt-Werts dürfen nicht größer als 128 Bits sein.

 

Der KP- \_ Salt wird weiterhin aus Gründen der Abwärtskompatibilität mit dem Basis Anbieter bereitgestellt. Neuere Anwendungen sollten den Wert des \_ Parameters "KP Salt Ex" verwenden \_ .

Im folgenden Beispiel wird ein Salt-Wert festgelegt.


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
