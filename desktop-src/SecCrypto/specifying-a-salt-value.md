---
description: Sowohl der Basisanbieter als auch der erweiterte Anbieter können den Wert und die Länge des zu verwendenden Salt-Werts angeben. Der Basisanbieter legt mithilfe des KP SALT-Parameterwerts \_ einen Salt-Wert fest. Der Basisanbieter legt immer elf Bytes des Salt-Werts fest.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Angeben eines Salt-Werts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d80ca64bc69cbcf0ed98d72b5b061616fc3cf641f3970d1533b094ef5687f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897945"
---
# <a name="specifying-a-salt-value"></a>Angeben eines Salt-Werts

Sowohl der Basisanbieter als auch der erweiterte Anbieter können den Wert und die Länge des zu verwendenden [*Salt-Werts*](../secgloss/s-gly.md) angeben. Der Basisanbieter legt mithilfe des KP SALT-Parameterwerts \_ einen Salt-Wert fest. Der Basisanbieter legt immer elf Bytes des Salt-Werts fest.

Der erweiterte Anbieter legt den Salt-Wert fest, indem [**er CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mit dem angegebenen KP SALT EX-Parameterwert und dem pbData-Parameter aufruft, der auf eine \_ \_ [**CRYPT \_ \_ INTEGER-BLOB-Struktur**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))  mit dem Salt-Wert zeigen.

> [!Note]  
> Die Gesamtlänge eines symmetrischen Schlüssels des erweiterten [*Anbieters*](../secgloss/s-gly.md) und dessen Salt-Wert darf nicht größer als 128 Bits sein.

 

KP \_ SALT wird weiterhin aus Gründen der Abwärtskompatibilität mit dem Basisanbieter bereitgestellt. Neuere Anwendungen sollten den KP \_ SALT \_ EX-Parameterwert verwenden.

Im folgenden Beispiel wird ein Salt-Wert definiert.


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



 

 
