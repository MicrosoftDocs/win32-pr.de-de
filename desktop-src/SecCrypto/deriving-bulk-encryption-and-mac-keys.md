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
# <a name="deriving-bulk-encryption-and-mac-keys"></a>Ableiten von Massen Verschlüsselung und Mac-Schlüsseln

[*Massen Verschlüsselung*](../secgloss/b-gly.md) und [*Mac-Schlüssel*](../secgloss/m-gly.md) werden von einem [*Hauptschlüssel*](../secgloss/m-gly.md) abgeleitet, können aber auch andere Quellen enthalten, je nach verwendetem Protokoll und Chiffre Sammlung.

Der Prozess der Ableitung von Massen Verschlüsselung und Mac-Schlüsseln ist für Client und Server identisch:

1.  Die Protokoll-Engine ruft " [**cryptsetkeyparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) " einmal oder mehrmals für den Hauptschlüssel auf, um dem CSP die zum Erstellen der Schlüssel erforderlichen Informationen bereitzustellen.
2.  Da [*kryptoapi*](../secgloss/c-gly.md) -Schlüssel nicht direkt von anderen Schlüsseln abgeleitet werden können, wird mithilfe von [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)ein Hash Objekt aus dem Hauptschlüssel erstellt. Dieser [*Hash*](../secgloss/h-gly.md) wird verwendet, um die neuen Schlüssel zu erstellen.
3.  Die beiden Massen Verschlüsselungsschlüssel und die beiden Mac-Schlüssel werden aus dem "Master Hash"-Objekt mithilfe von vier Aufrufen von " [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)" erstellt.

> [!Note]
> Beim Durchführen der SSL-erneuten Verbindungs Herstellung kann eine Protokoll-Engine das oben beschriebene Verfahren mehrmals mit demselben Hauptschlüssel ausführen. Dies ermöglicht es dem Client und dem Server, mehrere, häufig gleichzeitige Verbindungen zu verwenden, die jeweils unterschiedliche [*Massen Verschlüsselung*](../secgloss/b-gly.md) und Mac-Schlüssel ohne zusätzliche RSA-oder Diffie-Hellman Vorgänge verwenden.
> 
> Alle CSPs müssen gute Thread sichere Verfahren verwenden. Die Thread Anzahl von mehreren Dutzend ist nicht ungewöhnlich.

 

Der folgende Code ist der typische Quellcode für die Protokoll-Engine:


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



 

 
