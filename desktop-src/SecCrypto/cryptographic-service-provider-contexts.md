---
description: Die erste CryptoAPI-Funktion, die von einer Anwendung aufgerufen wird, die kryptografische APIs verwendet, ist die CryptAcquireContext-Funktion.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Kryptografiedienstanbieterkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ad2e77178ade8cc286dae1ff7334c89d33e46a63af227503f8e163f7d81cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768632"
---
# <a name="cryptographic-service-provider-contexts"></a>Kryptografiedienstanbieterkontexte

Die erste [*CryptoAPI-Funktion,*](../secgloss/c-gly.md) die von einer Anwendung aufgerufen wird, die kryptografische APIs verwendet, ist die [**CryptAcquireContext-Funktion.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) Diese Funktion gibt ein Handle an einen bestimmten CSP zurück, das die Spezifikation eines bestimmten [*Schlüsselcontainers innerhalb*](../secgloss/k-gly.md) des CSP enthält. Dieser Schlüsselcontainer ist entweder ein speziell angeforderter Schlüsselcontainer oder der Standardschlüsselcontainer für den derzeit angemeldeten Benutzer.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) kann auch einen neuen Schlüsselcontainer erstellen. Weitere Informationen finden Sie unter [Beispiel C-Programm: Erstellen](example-c-program-creating-a-key-container-and-generating-keys.md) eines Schlüsselcontainers und Generieren von Schlüsseln und Beispiel [C-Programm: Verwenden von CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Ein [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (Cryptographic Service Provider, CSP) hat sowohl einen Namen als auch einen Typ. Der Name eines der CSPs, die derzeit im Lieferumfang des Betriebssystems enthalten sind, ist [beispielsweise Microsoft Base Cryptographic Provider.](microsoft-base-cryptographic-provider.md) Es handelt sich um einen [PROV \_ RSA \_ FULL-Typanbieter.](prov-rsa-full.md) Der Name jedes Anbieters ist eindeutig. Der Anbietertyp ist nicht.

Wenn eine Anwendung [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) aufruft, um ein CSP-Handle zu erhalten, gibt sie einen Anbietertyp und optional einen Anbieternamen an. Wenn sowohl ein Typ als auch ein Name angegeben werden, lädt die Funktion den CSP mit dem übereinstimmenden Anbietertyp und Anbieternamen. Die Funktion gibt das Handle des CSP zurück, das sowohl Zugriff auf den CSP als auch auf einen Schlüsselcontainer [*innerhalb*](../secgloss/k-gly.md) des CSP bietet.

Wenn eine Anwendung [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) aufruft und einen Anbietertyp, aber keinen Anbieternamen angibt, sucht die Funktion nach einem benannten Anbieter und überprüft zunächst eine Liste der benannten Standardanbieter, die dem angemeldeten Benutzer zugeordnet sind, und, falls dies fehlschlägt, aus einer Liste der benannten Standardanbieter, die dem Computer zugeordnet sind. Nachdem der Anbietername bestimmt wurde, sucht die **CryptAcquireContext-Funktion** nach dem CSP für diesen Anbieter, lädt ihn und gibt sein Handle zurück.

Wenn Sie die Verwendung eines CSP-Handles abgeschlossen haben, geben Sie es frei, indem Sie die [**CryptReleaseContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) aufrufen.

 

 
