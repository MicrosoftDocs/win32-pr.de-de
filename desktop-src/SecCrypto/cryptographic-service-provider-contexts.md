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

Die erste [*CryptoAPI-Funktion,*](../secgloss/c-gly.md) die von einer Anwendung aufgerufen wird, die kryptografische APIs verwendet, ist die [**CryptAcquireContext-Funktion.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) Diese Funktion gibt ein Handle für einen bestimmten CSP zurück, der die Spezifikation eines bestimmten [*Schlüsselcontainers*](../secgloss/k-gly.md) innerhalb des CSP enthält. Dieser Schlüsselcontainer ist entweder ein speziell angeforderter Schlüsselcontainer oder der Standardschlüsselcontainer für den derzeit angemeldeten Benutzer.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) kann auch einen neuen Schlüsselcontainer erstellen. Weitere Informationen finden Sie unter [C-Beispielprogramm: Erstellen eines Schlüsselcontainers und Generieren von Schlüsseln](example-c-program-creating-a-key-container-and-generating-keys.md) und [C-Beispielprogramm: Verwenden von CryptAcquireContext.](example-c-program-using-cryptacquirecontext.md)

Ein [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) verfügt sowohl über einen Namen als auch über einen Typ. Beispielsweise lautet der Name eines der derzeit im Lieferumfang des Betriebssystems enthaltenen CSPs [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md). Es handelt sich um einen [PROV \_ RSA FULL-Typanbieter. \_ ](prov-rsa-full.md) Der Name jedes Anbieters ist eindeutig. der Anbietertyp nicht ist.

Wenn eine Anwendung [**CryptAcquireContext aufruft,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) um ein CSP-Handle abzurufen, gibt sie einen Anbietertyp und optional einen Anbieternamen an. Wenn sowohl ein Typ als auch ein Name angegeben werden, lädt die Funktion den CSP mit dem übereinstimmenden Anbietertyp und Anbieternamen. Die Funktion gibt das Handle des CSP zurück, das sowohl Zugriff auf den CSP als auch auf einen [*Schlüsselcontainer*](../secgloss/k-gly.md) innerhalb des CSP bietet.

Wenn eine Anwendung [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) aufruft und einen Anbietertyp, aber keinen Anbieternamen angibt, sucht die Funktion nach einem benannten Anbieter, überprüft zunächst eine Liste der benannten Standardanbieter, die dem angemeldeten Benutzer zugeordnet sind, und, falls dies fehlschlägt, aus einer Liste der dem Computer zugeordneten benannten Standardanbieter. Nachdem der Anbietername bestimmt wurde, sucht die **CryptAcquireContext-Funktion** nach dem CSP für diesen Anbieter, lädt ihn und gibt sein Handle zurück.

Wenn Sie mit der Verwendung eines CSP-Handles fertig sind, geben Sie es frei, indem Sie die [**CryptReleaseContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) aufrufen.

 

 
