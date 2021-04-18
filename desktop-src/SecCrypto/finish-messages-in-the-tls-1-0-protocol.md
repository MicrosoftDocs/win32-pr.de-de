---
description: Unmittelbar nach einer Nachricht zum Ändern der Verschlüsselungs Spezifikation wird eine Abschluss Meldung gesendet, um den Erfolg von Schlüsselaustausch-und Authentifizierungs Prozessen zu überprüfen.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Fertigstellen von Nachrichten im TLS 1,0-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a0f0f3e85916e66d434cb3e69b083348e40143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352461"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Fertigstellen von Nachrichten im TLS 1,0-Protokoll

Unmittelbar nach einer Nachricht zum Ändern der Verschlüsselungs Spezifikation wird eine Abschluss Meldung gesendet, um den Erfolg von Schlüsselaustausch-und Authentifizierungs Prozessen zu überprüfen. Die Abschluss Meldungen im TLS 1,0-Protokoll werden mithilfe der [*Pseudo Zufallsfunktion (Pseudo Random Function*](../secgloss/p-gly.md) , PRF) mit dem [*Hauptschlüssel*](../secgloss/m-gly.md), einer Bezeichnung und einem Ausgangswert als Eingabe berechnet. PRF erzeugt eine Ausgabe beliebiger Länge. Die folgende Methode wird verwendet, um die PRF-Ausgabe zu generieren, die in TLS 1,0-Abschluss Meldungen verwendet wird.

Ein PRF- [*Hashhandle*](../secgloss/h-gly.md) wird mithilfe von [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) generiert, wobei der **ALG- \_ ID** -Wert auf calg \_ TLS1PRF und das Handle für den Hauptschlüssel im *HKEY* -Parameter übergeben wird. Die Bezeichnungs-und Seed-Werte werden für das Hashhandle mit den Werten HP \_ TLS1PRF \_ Label \_ \_ bzw. HP TLS1PRF Seed im *dwparam* -Parameter mit der [**cryptsethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) -Funktion festgelegt. Schließlich ruft die Protokoll-Engine die Funktion " [**cryptgethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) " mit dem Wert "HP \_ hashval" im Parameter " *dwparam* " auf, um die PRF-Daten abzurufen, die in die Abschluss Meldung eingeschlossen werden sollen. Beim Aufrufen von **cryptgethashparam** muss die Protokoll-Engine angeben, wie viele Bytes von Daten PRF erstellt werden. Dies erfolgt im *pdwdatalen* -Parameter, und die resultierenden Daten werden in den Puffer eingefügt, auf den der *pbData* -Parameter zeigt.

Im folgenden ist der typische Quellcode für diese Protokoll-Engine aufgeführt:


```C++
CRYPT_DATA_BLOB Data;
HCRYPTHASH hFinishHash;
BYTE rgbFinishPRF[12];
BYTE rgbCliHashOfHandshakes[36];

//------------------------------------------------------------
// get client finish message

CryptCreateHash(
         hProv, 
         CALG_TLS1PRF, 
         hMasterKey, 
         0, 
         &hFinishHash);

Data.pbData = (BYTE*)"client finished";
Data.cbData = 15;
CryptSetHashParam(
         hFinishHash, 
         HP_TLS1PRF_LABEL, 
         (BYTE*)&Data, 
         0);

Data.pbData = rgbCliHashOfHandshakes;
Data.cbData = sizeof(rgbCliHashOfHandshakes);
CryptSetHashParam(
          hFinishHash, 
          HP_TLS1PRF_SEED, 
          (BYTE*)&Data, 
          0);

cbFinishPRF = sizeof(rgbFinishPRF);
CryptGetHashParam(
          hFinishHash, 
          HP_HASHVAL, 
          rgbFinishPRF, 
          &cbFinishPRF, 
          0);

CryptDestroyHash(hFinishHash);
```



 

 
