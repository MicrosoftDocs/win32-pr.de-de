---
description: CSPs für Prov \_ RSA \_ SChannel muss den calg \_ SSL3 \_ SHAMD5-Hash unterstützen, der mit dem Microsoft-Basis Kryptografieanbieter kompatibel ist, der in SSL 3,0 und TLS 1,0-Client Authentifizierung verwendet wird.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: RSA-Signaturtyp SHA/MD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344025"
---
# <a name="shamd5-rsa-signature-type"></a>RSA-Signaturtyp SHA/MD5

CSPs für Prov \_ RSA \_ SChannel muss den calg \_ SSL3 \_ SHAMD5- [*Hash*](../secgloss/h-gly.md) unterstützen, der mit dem Microsoft-Basis Kryptografieanbieter kompatibel ist, der in SSL 3,0 und TLS 1,0-Client Authentifizierung verwendet wird. Dieser Hash besteht aus einer Verkettung eines [*MD5*](../secgloss/m-gly.md) -Hashs und einem SHA-Hash, der mit einem RSA-oder Diffie-Hellman privaten Schlüssel signiert ist. Ein Handle für einen Hashwert dieses Typs wird mithilfe der [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) -Funktion oder der [**cpkreatehash**](https://www.bing.com/search?q=**CPCreateHash**) -Funktion mit calg \_ SSL3 \_ SHAMD5 als *algid* -Parameter erstellt. Beispiele für die Verwendung von Hash Funktionen finden Sie im [Beispiel c-Programm: Erstellen und Hashing eines Sitzungsschlüssels](example-c-program-creating-and-hashing-a-session-key.md) und [Beispiel-c-Programm: Signieren eines Hashs und Überprüfen der Hash Signatur](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
