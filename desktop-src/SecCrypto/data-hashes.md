---
description: Ein Hash eines Texts oder einer anderen Byte Zeichenfolge ist ein zugeordneter, statistisch eindeutiger Wert mit fester Länge.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Datenhashes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868427"
---
# <a name="data-hashes"></a>Datenhashes

Ein [*Hash*](../secgloss/h-gly.md) eines Texts oder einer anderen Byte Zeichenfolge ist ein zugeordneter, statistisch eindeutiger Wert mit fester Länge. In einigen Dokumenten wird ein *Hashwert* eines Texts auch als Digest bezeichnet. in dieser Dokumentation wird jedoch immer der Begriff Hash verwendet. CryptoAPI-Funktionen bieten die Möglichkeit, einen Hashwert für beliebige Text oder andere Zeichen folgen zu erstellen. Dieser Hash kann dann als eindeutiger Bezeichner der zugehörigen Daten verwendet werden.

Um die [*Integrität*](../secgloss/i-gly.md) eines Texts sicherzustellen, kann ein [*Hash*](../secgloss/h-gly.md) eines Texts an den Text gesendet werden. Der Empfänger kann dann einen Hashwert für die empfangenen Daten berechnen und den mit dem empfangenen Hash berechneten Hash vergleichen. Wenn die beiden Übereinstimmungen vorliegen, müssen die empfangenen Daten mit den Daten übereinstimmen, aus denen der empfangene Hash erstellt wurde.

Um einen Hashwert zu erhalten, erstellen Sie mithilfe von " [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)" ein Hash Objekt. Mit diesem Objekt werden die zu überprüfenden Daten gesammelt. Die Daten werden dann mit der [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) -Funktion dem Hash Objekt hinzugefügt.

Nachdem der letzte Datenblock dem Hash hinzugefügt wurde, wird die [**cryptgethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) -Funktion verwendet, um den Hashwert der Daten abzurufen.

Eine bessere Sicherheit wird gewährleistet, indem das Hash Objekt mit [**cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) zerstört wird, sobald der Hashwert abgerufen wurde.

 

 
