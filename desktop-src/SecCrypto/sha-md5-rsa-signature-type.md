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
# <a name="shamd5-rsa-signature-type"></a><span data-ttu-id="a915c-103">RSA-Signaturtyp SHA/MD5</span><span class="sxs-lookup"><span data-stu-id="a915c-103">SHA/MD5 RSA Signature Type</span></span>

<span data-ttu-id="a915c-104">CSPs für Prov \_ RSA \_ SChannel muss den calg \_ SSL3 \_ SHAMD5- [*Hash*](../secgloss/h-gly.md) unterstützen, der mit dem Microsoft-Basis Kryptografieanbieter kompatibel ist, der in SSL 3,0 und TLS 1,0-Client Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a915c-104">CSPs for PROV\_RSA\_SCHANNEL must support the CALG\_SSL3\_SHAMD5 [*hash*](../secgloss/h-gly.md) that is compatible with the Microsoft Base Cryptographic Provider used in SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="a915c-105">Dieser Hash besteht aus einer Verkettung eines [*MD5*](../secgloss/m-gly.md) -Hashs und einem SHA-Hash, der mit einem RSA-oder Diffie-Hellman privaten Schlüssel signiert ist.</span><span class="sxs-lookup"><span data-stu-id="a915c-105">This hash consists of a concatenation of an [*MD5*](../secgloss/m-gly.md) hash and a SHA hash signed with an RSA or Diffie-Hellman private key.</span></span> <span data-ttu-id="a915c-106">Ein Handle für einen Hashwert dieses Typs wird mithilfe der [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) -Funktion oder der [**cpkreatehash**](https://www.bing.com/search?q=**CPCreateHash**) -Funktion mit calg \_ SSL3 \_ SHAMD5 als *algid* -Parameter erstellt.</span><span class="sxs-lookup"><span data-stu-id="a915c-106">A handle to a hash value of this type is created by using the [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) or [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) function with CALG\_SSL3\_SHAMD5 as the *Algid* parameter.</span></span> <span data-ttu-id="a915c-107">Beispiele für die Verwendung von Hash Funktionen finden Sie im [Beispiel c-Programm: Erstellen und Hashing eines Sitzungsschlüssels](example-c-program-creating-and-hashing-a-session-key.md) und [Beispiel-c-Programm: Signieren eines Hashs und Überprüfen der Hash Signatur](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span><span class="sxs-lookup"><span data-stu-id="a915c-107">Examples of using hash functions can be seen in [Example C Program: Creating and Hashing a Session Key](example-c-program-creating-and-hashing-a-session-key.md) and [Example C Program: Signing a Hash and Verifying the Hash Signature](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span></span>

 

 
