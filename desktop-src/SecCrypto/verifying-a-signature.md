---
description: Um eine Signatur zu überprüfen, erstellen Sie ein Hashobjekt mit CryptCreateHash. Dieses Hashobjekt sammelt die zu überprüfenden Daten. Die Daten werden dann dem Hashobjekt mit der CryptHashData-Funktion hinzugefügt.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Überprüfen einer Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b3ea56533a9e04a53d847c80b1172ff155e847b8c9d5cf9b0f2ab3e24c8ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896245"
---
# <a name="verifying-a-signature"></a>Überprüfen einer Signatur

Um eine Signatur zu überprüfen, erstellen Sie mit [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)ein [*Hashobjekt.*](../secgloss/h-gly.md) Dieses Hashobjekt sammelt die zu überprüfenden Daten. Die Daten werden dann dem Hashobjekt mit der [**CryptHashData-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) hinzugefügt.

Nachdem der letzte Datenblock dem Hash hinzugefügt wurde, verwenden Sie [**CryptVerifySignature,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) um die Signatur zu überprüfen. Die Adresse der Signaturdaten, ein Handle für das Hashobjekt und das Handle der öffentlichen Schlüssel werden an **CryptVerifySignature** übergeben.

Nachdem die Signatur überprüft wurde (oder die Überprüfung fehlgeschlagen ist), zerstören Sie das Hashobjekt mithilfe der [**CryptDestroyHash-Funktion.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash)

 

 
