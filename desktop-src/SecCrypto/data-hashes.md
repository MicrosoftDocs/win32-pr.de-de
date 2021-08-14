---
description: Ein Hash eines Texts oder einer anderen Bytezeichenfolge ist ein zugeordneter, statistisch eindeutiger Wert fester Länge.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Datenhashes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a998c2172f6bd3b48bb3cdc94f1ed2207384606950dd9d6e8b6f3152149eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767768"
---
# <a name="data-hashes"></a>Datenhashes

Ein [*Hash*](../secgloss/h-gly.md) eines Texts oder einer anderen Bytezeichenfolge ist ein zugeordneter, statistisch eindeutiger Wert fester Länge. In einigen Dokumenten wird ein *Hash* eines Texts auch als Digest bezeichnet. In dieser Dokumentation wird jedoch immer der Begriff Hash verwendet. CryptoAPI-Funktionen bieten eine Möglichkeit, einen Hash für beliebigen Text oder eine andere Bytezeichenfolge zu erstellen. Dieser Hash kann dann als eindeutiger Bezeichner der zugeordneten Daten verwendet werden.

Um die [*Integrität*](../secgloss/i-gly.md) eines Texts sicherzustellen, kann ein [*Hash*](../secgloss/h-gly.md) eines Texts gesendet werden, um den Text zu begleitet. Der Empfänger kann dann einen Hash für die empfangenen Daten berechnen und den berechneten Hash mit dem empfangenen Hash vergleichen. Wenn die beiden übereinstimmen, müssen die empfangenen Daten mit den Daten übereinstimmen, aus denen der empfangene Hash erstellt wurde.

Um einen Hashwert abzurufen, erstellen Sie mit [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)ein Hashobjekt. Dieses Objekt sammelt die zu überprüfenden Daten. Die Daten werden dann dem Hashobjekt mit der [**CryptHashData-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) hinzugefügt.

Nachdem der letzte Datenblock dem Hash hinzugefügt wurde, wird die [**CryptGetHashParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) verwendet, um den Hashwert der Daten abzurufen.

Die Sicherheit wird verbessert, indem das Hashobjekt mit [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) zerstört wird, sobald der Hashwert abgerufen wurde.

 

 
