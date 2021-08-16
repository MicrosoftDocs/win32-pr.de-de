---
description: Massenverschlüsselung und MAC-Schlüssel werden von einem Hauptschlüssel abgeleitet, können aber abhängig vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung auch andere Quellen enthalten.
ms.assetid: f78acb54-c32a-46a8-b465-855251069a57
title: Ableiten von Massenverschlüsselung und MAC-Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602419be7cdddea27c190806f0d03e087b8aac63eeeee2d80e96e2b3bcfae561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767704"
---
# <a name="deriving-bulk-encryption-and-mac-keys"></a>Ableiten von Massenverschlüsselung und MAC-Schlüsseln

[*Massenverschlüsselung und*](../secgloss/b-gly.md) [*MAC-Schlüssel*](../secgloss/m-gly.md) werden von einem [*Hauptschlüssel abgeleitet,*](../secgloss/m-gly.md) können aber abhängig vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung auch andere Quellen enthalten.

Der Prozess der Ableitung von Massenverschlüsselung und MAC-Schlüsseln ist für Client und Server identisch:

1.  Die Protokoll-Engine ruft [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) mindestens einmal auf dem Hauptschlüssel auf, um dem CSP die Informationen zur Verfügung zu stellen, die zum Erstellen der Schlüssel erforderlich sind.
2.  Da [*CryptoAPI-Schlüssel*](../secgloss/c-gly.md) nicht direkt von anderen Schlüsseln abgeleitet werden können, wird mithilfe von [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)ein Hashobjekt aus dem Hauptschlüssel erstellt. Dieser [*Hash*](../secgloss/h-gly.md) wird verwendet, um die neuen Schlüssel zu erstellen.
3.  Die beiden Massenverschlüsselungsschlüssel und die beiden MAC-Schlüssel werden aus dem Masterhashobjekt mit vier Aufrufen von [**CryptDeriveKey erstellt.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)

> [!Note]
> Bei erneuten SSL-Verbindungen kann eine Protokoll-Engine das oben beschriebene Verfahren mehrmals mit demselben Hauptschlüssel ausführen. Dadurch können Client und Server über mehrere, häufig gleichzeitige Verbindungen verfügen, die jeweils unterschiedliche Massenverschlüsselungs- und MAC-Schlüssel ohne zusätzliche RSA- oder Diffie-Hellman verwenden. [](../secgloss/b-gly.md)
> 
> Alle CSPs müssen gute threadsichere Methoden verwenden. Die Threadanzahl von mehreren Dutzenden ist nicht ungewöhnlich.

 

Im Folgenden finden Sie einen typischen Quellcode für die Protokoll-Engine:


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



 

 
