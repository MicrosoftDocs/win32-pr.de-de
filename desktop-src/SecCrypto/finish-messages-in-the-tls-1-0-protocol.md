---
description: Eine Abschlussmeldung wird unmittelbar nach einer Änderungsverschlüsselungsspezifikation gesendet, um den Erfolg von Schlüsselaustausch- und Authentifizierungsprozessen zu überprüfen.
ms.assetid: 1ae92223-3729-48be-af42-146c9cbae6a5
title: Fertig stellen von Nachrichten im TLS 1.0-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e9af7502f0865661e2ed0f6a80059cb822395002ccaf035373dc3db322adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006978"
---
# <a name="finish-messages-in-the-tls-10-protocol"></a>Fertig stellen von Nachrichten im TLS 1.0-Protokoll

Eine Abschlussmeldung wird unmittelbar nach einer Änderungsverschlüsselungsspezifikation gesendet, um den Erfolg von Schlüsselaustausch- und Authentifizierungsprozessen zu überprüfen. Die Fertig stellenden Nachrichten im TLS 1.0-Protokoll werden mithilfe der [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) mit dem Hauptschlüssel, [](../secgloss/m-gly.md)einer Bezeichnung und einem Startwert als Eingabe berechnet. PRF erzeugt eine Ausgabe beliebiger Länge. Die folgende Methode wird verwendet, um die PRF-Ausgabe zu generieren, die in TLS 1.0-Abschlussnachrichten verwendet wird.

Ein PRF-Hashhandl wird mithilfe von [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) generiert, bei dem der Wert der [](../secgloss/h-gly.md) **\_ ALG-ID** auf CALG TLS1PRF und das Handle für den Hauptschlüssel festgelegt ist, der im \_ *hKey-Parameter übergeben* wird. Die Bezeichnungs- und Startwerte werden auf dem Hashhandling mithilfe der Werte HP TLS1PRF LABEL bzw. HP TLS1PRF SEED im dwParam-Parameter mit der \_ \_ \_ \_ [**CryptSetHashParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) festgelegt.  Schließlich ruft die Protokoll-Engine die [**Funktion CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) mit dem Wert HP HASHVAL im \_ *dwParam-Parameter* auf, um die PRF-Daten abzurufen, die in die Abschlussmeldung eingeschlossen werden sollen. Beim Aufruf von **CryptGetHashParam** muss die Protokoll-Engine angeben, wie viele Bytes von Daten PRF erzeugt werden. Dies erfolgt im *pdwDataLen-Parameter,* und die resultierenden Daten werden im Puffer platziert, auf den der *pbData-Parameter zeigt.*

Im Folgenden finden Sie den typischen Quellcode für diese Protokoll-Engine:


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



 

 
