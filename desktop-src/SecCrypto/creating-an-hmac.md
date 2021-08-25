---
description: Erläutert, wie ein HMAC erstellt wird.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Erstellen eines HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb600b00c0bfa3ac8af24cd297b1e2dd67933e2990216dafe84713ee5e831c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876666"
---
# <a name="creating-an-hmac"></a>Erstellen eines HMAC

**So berechnen Sie einen HMAC**

1.  Rufen Sie durch Aufrufen von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)einen Zeiger auf den Microsoft [*Cryptographic Service Provider*](../secgloss/c-gly.md) (CSP) ab.
2.  Erstellen Sie ein Handle für ein [*HMAC-Hashobjekt,*](../secgloss/h-gly.md) indem Sie [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)aufrufen. [](../secgloss/h-gly.md) Übergeben Sie CALG \_ HMAC im *Algid-Parameter.* Übergeben Sie das Handle eines [*symmetrischen Schlüssels*](../secgloss/s-gly.md) im *hKey-Parameter.* Dieser symmetrische Schlüssel ist der Schlüssel, der zum Berechnen des HMAC verwendet wird.
3.  Geben Sie den Typ des Zu verwendenden Hashs an, indem [**Sie CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) aufrufen, wobei der *dwParam-Parameter* auf den Wert HP HMAC INFO festgelegt \_ \_ ist. Der *pbData-Parameter* muss auf eine initialisierte [**HMAC \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) verweisen.
4.  Rufen Sie [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) auf, um mit dem Berechnen des HMAC der Daten zu beginnen. Der erste Aufruf von **CryptHashData** bewirkt, dass der Schlüsselwert mithilfe des XOR-Operators mit der inneren Zeichenfolge und den Daten kombiniert wird. Das Ergebnis des XOR-Vorgangs wird mit einem Hashwert versehen, und dann werden die Zieldaten für den HMAC (auf den der *pbData-Parameter* verweist, der im Aufruf von **CryptHashData** übergeben wird) mit einem Hashwert versehen. Bei Bedarf können nachfolgende Aufrufe von **CryptHashData** durchgeführt werden, um das Hashing der Zieldaten abzuschließen.
5.  Rufen Sie [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) auf, wobei der *dwParam-Parameter* auf HP HASHVAL festgelegt \_ ist. Dieser Aufruf bewirkt, dass der innere Hash abgeschlossen und die äußere Zeichenfolge mithilfe von XOR mit dem Schlüssel kombiniert wird. Das Ergebnis des XOR-Vorgangs wird mit einem Hashwert versehen, und das Ergebnis des inneren Hashs (abgeschlossen im vorherigen Schritt) wird mit einem Hashwert versehen. Der äußere Hash wird dann fertig gestellt und im *pbData-Parameter* und der Länge im *dwDataLen-Parameter* zurückgegeben.

> [!Note]  
> Verwenden Sie nicht den gleichen [*symmetrischen*](../secgloss/s-gly.md) Schlüssel [*(Sitzungsschlüssel)*](../secgloss/s-gly.md)sowohl für die Nachrichtenverschlüsselung als auch [*für Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (MAC). Die Verwendung desselben Schlüssels für beide erhöht erheblich das Risiko, dass Nachrichten von Angreifern decodiert werden.

 

 

 
