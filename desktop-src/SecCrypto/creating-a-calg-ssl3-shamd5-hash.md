---
description: Erläutert, wie ein calg \_ SSL3 SHAMD5-Hash erstellt wird \_ .
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Erstellen eines CALG_SSL3_SHAMD5 Hash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358559"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>Erstellen eines calg- \_ SSL3 \_ SHAMD5 Hash

**So erstellen Sie einen calg- \_ SSL3 \_ SHAMD5-Hash**

1.  Erstellen Sie mithilfe der standardmäßigen kryptoapi-Methodik sowohl einen MD5-als auch einen [*SHA*](../secgloss/s-gly.md) - [*Hash*](../secgloss/h-gly.md) der Zieldaten.
2.  Verketten Sie die beiden Hashwerte mit dem MD5-Wert ganz links und dem SHA-Wert ganz rechts. Dies führt zu einem Wert von 36 Byte (16 Bytes + 20 Bytes).
3.  Rufen Sie ein Handle für ein [*Hash Objekt*](../secgloss/h-gly.md) durch Aufrufen von " [**cryptcreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with calg SSL3 SHAMD5" ab, \_ \_ das im *algid* -Parameter übergeben wird.
4.  Legen Sie den Hashwert mit einem Rückruf von [**cryptsethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam)fest. Die verketteten Hashwerte werden als **Byte** \* im *pbData* -Parameter übergeben, und der HP \_ hashval-Wert muss im *dwparam* -Parameter übergeben werden. Das Aufrufen von [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mithilfe des Handles, das von [**cryptcreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in Schritt 3 zurückgegeben wird, schlägt fehl.
5.  Rufen Sie [**cryptsignhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) auf, um die Signatur zu generieren.
6.  Nennen Sie [**cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) , um das Hash Objekt zu zerstören.

 

 
