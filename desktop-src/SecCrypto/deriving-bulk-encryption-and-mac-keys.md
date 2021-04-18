---
description: Massen Verschlüsselung und Mac-Schlüssel werden von einem Hauptschlüssel abgeleitet, können aber auch andere Quellen enthalten, je nach verwendetem Protokoll und Chiffre Sammlung.
ms.assetid: f78acb54-c32a-46a8-b465-855251069a57
title: Ableiten von Massen Verschlüsselung und Mac-Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cbf216fd850c7b98c638d4fdc10a84087d91ac
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354927"
---
# <a name="deriving-bulk-encryption-and-mac-keys"></a><span data-ttu-id="9f9fc-103">Ableiten von Massen Verschlüsselung und Mac-Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="9f9fc-103">Deriving Bulk Encryption and MAC Keys</span></span>

<span data-ttu-id="9f9fc-104">[*Massen Verschlüsselung*](../secgloss/b-gly.md) und [*Mac-Schlüssel*](../secgloss/m-gly.md) werden von einem [*Hauptschlüssel*](../secgloss/m-gly.md) abgeleitet, können aber auch andere Quellen enthalten, je nach verwendetem Protokoll und Chiffre Sammlung.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-104">[*Bulk encryption*](../secgloss/b-gly.md) and [*MAC keys*](../secgloss/m-gly.md) are derived from a [*master key*](../secgloss/m-gly.md) but can include other sources depending on the protocol and cipher suite used.</span></span>

<span data-ttu-id="9f9fc-105">Der Prozess der Ableitung von Massen Verschlüsselung und Mac-Schlüsseln ist für Client und Server identisch:</span><span class="sxs-lookup"><span data-stu-id="9f9fc-105">The process of deriving bulk encryption and MAC keys is the same for both client and server:</span></span>

1.  <span data-ttu-id="9f9fc-106">Die Protokoll-Engine ruft " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " einmal oder mehrmals für den Hauptschlüssel auf, um dem CSP die zum Erstellen der Schlüssel erforderlichen Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-106">The protocol engine calls [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) on the master key one or more times to provide the CSP with the information needed to build the keys.</span></span>
2.  <span data-ttu-id="9f9fc-107">Da [*kryptoapi*](../secgloss/c-gly.md) -Schlüssel nicht direkt von anderen Schlüsseln abgeleitet werden können, wird mithilfe von [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)ein Hash Objekt aus dem Hauptschlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-107">Because [*CryptoAPI*](../secgloss/c-gly.md) keys cannot be derived directly from other keys, a hash object is created from the master key using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="9f9fc-108">Dieser [*Hash*](../secgloss/h-gly.md) wird verwendet, um die neuen Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-108">This [*hash*](../secgloss/h-gly.md) is used to create the new keys.</span></span>
3.  <span data-ttu-id="9f9fc-109">Die beiden Massen Verschlüsselungsschlüssel und die beiden Mac-Schlüssel werden aus dem "Master Hash"-Objekt mithilfe von vier Aufrufen von " [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-109">The two bulk encryption keys and the two MAC keys are created from the "master hash" object using four calls to [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey).</span></span>

> [!Note]
> <span data-ttu-id="9f9fc-110">Beim Durchführen der SSL-erneuten Verbindungs Herstellung kann eine Protokoll-Engine das oben beschriebene Verfahren mehrmals mit demselben Hauptschlüssel ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-110">When performing SSL reconnects, a protocol engine can perform the above procedure several times using the same master key.</span></span> <span data-ttu-id="9f9fc-111">Dies ermöglicht es dem Client und dem Server, mehrere, häufig gleichzeitige Verbindungen zu verwenden, die jeweils unterschiedliche [*Massen Verschlüsselung*](../secgloss/b-gly.md) und Mac-Schlüssel ohne zusätzliche RSA-oder Diffie-Hellman Vorgänge verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-111">This enables the client and server to have multiple, often simultaneous connections, each using different [*Bulk encryption*](../secgloss/b-gly.md) and MAC keys without additional RSA or Diffie-Hellman operations.</span></span>
> 
> <span data-ttu-id="9f9fc-112">Alle CSPs müssen gute Thread sichere Verfahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-112">All CSPs must use good thread-safe practices.</span></span> <span data-ttu-id="9f9fc-113">Die Thread Anzahl von mehreren Dutzend ist nicht ungewöhnlich.</span><span class="sxs-lookup"><span data-stu-id="9f9fc-113">Thread counts of several dozen are not unusual.</span></span>

 

<span data-ttu-id="9f9fc-114">Der folgende Code ist der typische Quellcode für die Protokoll-Engine:</span><span class="sxs-lookup"><span data-stu-id="9f9fc-114">The following is typical source code for the protocol engine:</span></span>


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

BOOL fClient = <TRUE if this is code for the client?>;
CRYPT_DATA_BLOB Data;
HCRYPTHASH hMasterHash;

//--------------------------------------------------------------------
// Finish creating the master_secret.

switch(<protocol being used>)
{
    case <PCT 1.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_CLEAR_KEY, 
                   (PBYTE)&Data, 
                   0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CLIENT_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_SERVER_RANDOM, 
                    (PBYTE)&Data, 
                    0);

//------------------------------------------------------------
// Specify the SH_CERTIFICATE_DATA.
        Data.pbData = pbServerCertificate;
        Data.cbData = cbServerCertificate;
        CryptSetKeyParam(
                    hMasterKey, 
                    KP_CERTIFICATE, 
                    (PBYTE)&Data, 
                    0);
        break;

    case <SSL 2.0>:

//------------------------------------------------------------
// Specify clear key value.

        Data.pbData = pClearKey;
        Data.cbData = cbClearKey;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLEAR_KEY, 
                 (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify the CH_CHALLENGE_DATA.

        Data.pbData = pChallenge;
        Data.cbData = cbChallenge;
        CryptSetKeyParam(
                 hMasterKey, 
                 KP_CLIENT_RANDOM,
                 (BYTE*)&Data, 
                 0);

//------------------------------------------------------------
// Specify the SH_CONNECTION_ID_DATA.

        Data.pbData = pConnectionID;
        Data.cbData = cbConnectionID;
        CryptSetKeyParam(
                   hMasterKey, 
                   KP_SERVER_RANDOM,
                   (BYTE*)&Data, 
                   0);
        break;

case <SSL 3.0>:
case <TLS 1.0>:


//------------------------------------------------------------
// Specify client_random.

        Data.pbData = pClientRandom;
        Data.cbData = cbClientRandom;
        CryptSetKeyParam(
                hMasterKey, 
                KP_CLIENT_RANDOM, 
                (PBYTE)&Data, 
                 0);

//------------------------------------------------------------
// Specify server_random.

        Data.pbData = pServerRandom;
        Data.cbData = cbServerRandom;
        CryptSetKeyParam(
                  hMasterKey, 
                  KP_SERVER_RANDOM, 
                  (PBYTE)&Data, 
                  0);
}

//------------------------------------------------------------
// Create the master hash object from the master key.

CryptCreateHash(
            hProv, 
            CALG_SCHANNEL_MASTER_HASH,
            hMasterKey, 
            0, 
            &hMasterHash);

//------------------------------------------------------------
// Derive read key from the master hash object.

CryptDeriveKey(hProv, 
               CALG_SCHANNEL_ENC_KEY, 
               hMasterHash,
               fClient ? CRYPT_SERVER : 0,
               &hReadKey);

//------------------------------------------------------------
// Derive write key from the master hash object.

CryptDeriveKey(
           hProv,
           CALG_SCHANNEL_ENC_KEY,
           hMasterHash,
           fClient ? 0 : CRYPT_SERVER,
           &hWriteKey);

if(<protocol being used> != <SSL 2.0>)   // for SSL 2.0, the master 
                                         // key is also the MAC.
{
//------------------------------------------------------------
// Derive read MAC from the master hash object.

    CryptDeriveKey(
              hProv,
              CALG_SCHANNEL_MAC_KEY,
              hMasterHash,
              fClient ? CRYPT_SERVER : 0,
              &hReadMAC);

//------------------------------------------------------------
// Derive write MAC from the master hash object.

    CryptDeriveKey(
             hProv,
             CALG_SCHANNEL_MAC_KEY,
             hMasterHash,
             fClient ? 0 : CRYPT_SERVER,
             &hWriteMAC);
}

CryptDestroyHash(hMasterHash);
```



 

 
