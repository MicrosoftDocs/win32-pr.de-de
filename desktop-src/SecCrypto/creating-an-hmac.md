---
description: Erläutert, wie ein HMAC erstellt wird.
ms.assetid: b1747b7e-a505-4b23-93bc-cef4e77bf825
title: Erstellen eines HMAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364314081bd1d84d6d9bfff889c234470cc6775c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368022"
---
# <a name="creating-an-hmac"></a>Erstellen eines HMAC

**So berechnen Sie einen HMAC**

1.  Rufen Sie einen Zeiger auf den Microsoft [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) ab, indem Sie [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)aufrufen.
2.  Erstellen Sie ein Handle für ein [*HMAC*](../secgloss/h-gly.md)-[*Hash Objekt*](../secgloss/h-gly.md) , indem Sie [**cryptcreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)aufrufen. Übergeben Sie den calg- \_ HMAC im *algid* -Parameter. Übergeben Sie das Handle eines [*symmetrischen Schlüssels*](../secgloss/s-gly.md) im *HKEY* -Parameter. Dieser symmetrische Schlüssel ist der Schlüssel, der verwendet wird, um den HMAC zu berechnen.
3.  Geben Sie den zu verwendenden Hashtyp an, indem Sie [**cryptsethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) mit dem Parameter *dwparam* auf den Wert HP \_ HMAC \_ Info festlegen. Der *pbData* -Parameter muss auf eine initialisierte [**HMAC- \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-hmac_info) Struktur zeigen.
4.  Wenden Sie [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) an, um mit dem Berechnen des HMACs der Daten zu beginnen. Der erste Rückruf von **CryptHashData** bewirkt, dass der Schlüsselwert mit dem XOR-Operator mit der inneren Zeichenfolge und den Daten kombiniert wird. Das Ergebnis der XOR-Operation wird als Hash verwendet, und dann werden die Zieldaten für den HMAC (auf den der *pbData* -Parameter verweist, der im Rückruf von **CryptHashData** übergeben wird) mit Hash versehen. Ggf. können nachfolgende Aufrufe von **CryptHashData** erfolgen, um das hashup der Zieldaten abzuschließen.
5.  Nennen Sie [**cryptgethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) mit dem Parameter *dwparam* , der auf HP hashval festgelegt ist \_ . Dieser Befehl bewirkt, dass der innere Hash abgeschlossen ist und die äußere Zeichenfolge mithilfe von XOR mit dem Schlüssel kombiniert wird. Das Ergebnis der XOR-Operation wird als Hash verwendet, und anschließend wird das Ergebnis des inneren Hashs (im vorherigen Schritt abgeschlossen) als Hash verwendet. Der äußere Hash wird dann beendet und im *pbData* -Parameter und der Länge im *dwdatalen* -Parameter zurückgegeben.

> [!Note]  
> Verwenden Sie nicht denselben [*symmetrischen*](../secgloss/s-gly.md) ([*Sitzungs*](../secgloss/s-gly.md)-) Schlüssel sowohl für die Nachrichten Verschlüsselung als auch für die [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (Mac)-Generierung. Wenn Sie den gleichen Schlüssel für beides verwenden, erhöht sich das Risiko, dass Nachrichten von Angreifern decodiert werden.

 

 

 
