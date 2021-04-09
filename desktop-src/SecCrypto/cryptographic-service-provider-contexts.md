---
description: Die erste kryptoapi-Funktion, die von einer Anwendung aufgerufen wird, die kryptografische APIs verwendet, ist die CryptAcquireContext-Funktion.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Kryptografiedienstanbieter-Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df20df528b0ba0c385c7ab690436351d918f1521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128800"
---
# <a name="cryptographic-service-provider-contexts"></a>Kryptografiedienstanbieter-Kontexte

Die erste [*kryptoapi*](../secgloss/c-gly.md) -Funktion, die von einer Anwendung aufgerufen wird, die kryptografische APIs verwendet, ist die [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion. Diese Funktion gibt ein Handle für einen bestimmten CSP zurück, der die Spezifikation eines bestimmten [*Schlüssel Containers*](../secgloss/k-gly.md) innerhalb des CSP einschließt. Dieser Schlüssel Container ist entweder ein speziell angeforderter Schlüssel Container oder der Standardschlüssel Container für den aktuell angemeldeten Benutzer.

[**Mit CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) kann auch ein neuer Schlüssel Container erstellt werden. Weitere Informationen finden Sie unter [Beispiel c-Programm: Erstellen eines Schlüssel Containers und Erstellen von Schlüsseln](example-c-program-creating-a-key-container-and-generating-keys.md) und [Beispiel-c-Programm: Verwenden von CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Ein [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) verfügt über einen Namen und einen Typ. Beispielsweise ist der Name eines der derzeit mit dem Betriebssystem gelieferten CSPs der Microsoft- [Basis Kryptografieanbieter](microsoft-base-cryptographic-provider.md). Dabei handelt es sich um einen [Prov \_ RSA \_ Full](prov-rsa-full.md) -Typanbieter. Der Name jedes Anbieters ist eindeutig. der Anbietertyp ist nicht.

Wenn eine Anwendung [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) zum Abrufen eines CSP-Handles aufruft, gibt Sie einen Anbietertyp und optional einen Anbieter Namen an. Wenn sowohl ein Typ als auch ein Name angegeben ist, lädt die Funktion den CSP mit dem entsprechenden Anbietertyp und Anbieter Namen. Die Funktion gibt das Handle des CSP zurück, das den Zugriff sowohl auf den CSP als auch auf einen [*Schlüssel Container*](../secgloss/k-gly.md) innerhalb des CSP ermöglicht.

Wenn eine Anwendung [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) aufruft und einen Anbietertyp, aber keinen Anbieter Namen angibt, sucht die Funktion nach einem benannten Anbieter und überprüft zunächst eine Liste mit den standardmäßigen benannten Anbietern, die dem angemeldeten Benutzer zugeordnet sind, und, falls dies nicht der Fall ist, aus einer Liste mit den standardmäßigen benannten Anbietern, die dem Computer zugeordnet sind. Nachdem der Anbieter Name ermittelt wurde, sucht die **CryptAcquireContext** -Funktion nach dem CSP-Anbieter, lädt ihn und gibt sein Handle zurück.

Wenn Sie die Verwendung eines CSP-Handles abgeschlossen haben, geben Sie es durch Aufrufen der [**cryptreleasecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) -Funktion frei.

 

 
