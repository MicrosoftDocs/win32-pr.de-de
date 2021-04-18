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
# <a name="finish-messages-in-the-tls-10-protocol"></a><span data-ttu-id="3f8d3-103">Fertigstellen von Nachrichten im TLS 1,0-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3f8d3-103">Finish Messages in the TLS 1.0 Protocol</span></span>

<span data-ttu-id="3f8d3-104">Unmittelbar nach einer Nachricht zum Ändern der Verschlüsselungs Spezifikation wird eine Abschluss Meldung gesendet, um den Erfolg von Schlüsselaustausch-und Authentifizierungs Prozessen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-104">A finish message is sent immediately after a change cipher spec message to verify the success of key exchange and authentication processes.</span></span> <span data-ttu-id="3f8d3-105">Die Abschluss Meldungen im TLS 1,0-Protokoll werden mithilfe der [*Pseudo Zufallsfunktion (Pseudo Random Function*](../secgloss/p-gly.md) , PRF) mit dem [*Hauptschlüssel*](../secgloss/m-gly.md), einer Bezeichnung und einem Ausgangswert als Eingabe berechnet.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-105">The finish messages in the TLS 1.0 protocol are calculated using [*Pseudo-Random Function*](../secgloss/p-gly.md) (PRF) with the [*master key*](../secgloss/m-gly.md), a label, and a seed as input.</span></span> <span data-ttu-id="3f8d3-106">PRF erzeugt eine Ausgabe beliebiger Länge.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-106">PRF produces an output of arbitrary length.</span></span> <span data-ttu-id="3f8d3-107">Die folgende Methode wird verwendet, um die PRF-Ausgabe zu generieren, die in TLS 1,0-Abschluss Meldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-107">The following method is used to generate the PRF output used in TLS 1.0 finish messages.</span></span>

<span data-ttu-id="3f8d3-108">Ein PRF- [*Hashhandle*](../secgloss/h-gly.md) wird mithilfe von [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) generiert, wobei der **ALG- \_ ID** -Wert auf calg \_ TLS1PRF und das Handle für den Hauptschlüssel im *HKEY* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-108">A PRF [*hash*](../secgloss/h-gly.md) handle is generated using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with the **ALG\_ID** value set to CALG\_TLS1PRF and the handle to the master key passed in the *hKey* parameter.</span></span> <span data-ttu-id="3f8d3-109">Die Bezeichnungs-und Seed-Werte werden für das Hashhandle mit den Werten HP \_ TLS1PRF \_ Label \_ \_ bzw. HP TLS1PRF Seed im *dwparam* -Parameter mit der [**cryptsethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) -Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-109">The label and seed values are set on the hash handle using the values HP\_TLS1PRF\_LABEL and HP\_TLS1PRF\_SEED, respectively, in the *dwParam* parameter with the [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam) function.</span></span> <span data-ttu-id="3f8d3-110">Schließlich ruft die Protokoll-Engine die Funktion " [**cryptgethashparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) " mit dem Wert "HP \_ hashval" im Parameter " *dwparam* " auf, um die PRF-Daten abzurufen, die in die Abschluss Meldung eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-110">Finally, the protocol engine calls the function [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) with the value HP\_HASHVAL in the *dwParam* parameter to retrieve the PRF data to be included in the finish message.</span></span> <span data-ttu-id="3f8d3-111">Beim Aufrufen von **cryptgethashparam** muss die Protokoll-Engine angeben, wie viele Bytes von Daten PRF erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-111">When making the call to **CryptGetHashParam**, the protocol engine must specify how many bytes of data PRF will produce.</span></span> <span data-ttu-id="3f8d3-112">Dies erfolgt im *pdwdatalen* -Parameter, und die resultierenden Daten werden in den Puffer eingefügt, auf den der *pbData* -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="3f8d3-112">This is done in the *pdwDataLen* parameter, and the resulting data is placed in the buffer pointed to by the *pbData* parameter.</span></span>

<span data-ttu-id="3f8d3-113">Im folgenden ist der typische Quellcode für diese Protokoll-Engine aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3f8d3-113">The following is typical source code for this protocol engine:</span></span>


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



 

 
