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
# <a name="specifying-a-salt-value"></a><span data-ttu-id="c5640-105">Angeben eines Salt-Werts</span><span class="sxs-lookup"><span data-stu-id="c5640-105">Specifying a Salt Value</span></span>

<span data-ttu-id="c5640-106">Sowohl der Basis Anbieter als auch der erweiterte Anbieter können den Wert und die Länge des zu verwendenden [*Salt-Werts*](../secgloss/s-gly.md) angeben.</span><span class="sxs-lookup"><span data-stu-id="c5640-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="c5640-107">Der Basis Anbieter legt einen Salt-Wert mit dem Wert des KP- \_ Salt-Parameters fest.</span><span class="sxs-lookup"><span data-stu-id="c5640-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="c5640-108">Der Basis Anbieter legt immer elf Bytes an Salt-Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c5640-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="c5640-109">Der erweiterte Anbieter legt den Salt-Wert fest, indem er [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mit dem Parameterwert "KP Salt Ex" aufruft, \_ \_ und mit dem *pbData* -Parameter, der auf eine [**crypt- \_ \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) -Struktur mit dem Salt-Wert verweist.</span><span class="sxs-lookup"><span data-stu-id="c5640-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="c5640-110">Die Gesamtlänge eines [*symmetrischen*](../secgloss/s-gly.md) Anbieters des erweiterten Anbieters und des Salt-Werts dürfen nicht größer als 128 Bits sein.</span><span class="sxs-lookup"><span data-stu-id="c5640-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="c5640-111">Der KP- \_ Salt wird weiterhin aus Gründen der Abwärtskompatibilität mit dem Basis Anbieter bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c5640-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="c5640-112">Neuere Anwendungen sollten den Wert des \_ Parameters "KP Salt Ex" verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="c5640-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="c5640-113">Im folgenden Beispiel wird ein Salt-Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5640-113">The following example sets a salt value.</span></span>


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



 

 
