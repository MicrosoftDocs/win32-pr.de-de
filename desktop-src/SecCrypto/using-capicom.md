---
description: Dieser Abschnitt enthält Szenarien mit CAPICOM-Prozeduren.
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: Verwenden von CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527623"
---
# <a name="using-capicom"></a><span data-ttu-id="21e3a-103">Verwenden von CAPICOM</span><span class="sxs-lookup"><span data-stu-id="21e3a-103">Using CAPICOM</span></span>

<span data-ttu-id="21e3a-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21e3a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="21e3a-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="21e3a-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="21e3a-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="21e3a-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="21e3a-107">Dieser Abschnitt enthält Szenarien mit CAPICOM-Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="21e3a-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="21e3a-108">Das Erstellen [*digitaler Signaturen*](../secgloss/d-gly.md) und das Aufheben der Zuordnung von Nachrichten mit CAPICOM erfolgt mithilfe der PKI-Kryptografie (Public Key-Infrastruktur) und kann nur durchgeführt werden, wenn der Signatur Geber oder Benutzer, der eine eingeschlossene Nachricht entschlüsselt, Zugriff auf ein Zertifikat mit einem verfügbaren, zugeordneten privaten Schlüssel hat.</span><span class="sxs-lookup"><span data-stu-id="21e3a-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="21e3a-109">Um eine eingeschlossene Nachricht zu entschlüsseln, muss sich ein Zertifikat mit Zugriff auf den privaten Schlüssel im My-Speicher befinden.</span><span class="sxs-lookup"><span data-stu-id="21e3a-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="21e3a-110">Aufgabenbasierte Szenarios und Beispiele wurden in die folgenden Abschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="21e3a-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="21e3a-111">Alternativen zur Verwendung von CAPICOM</span><span class="sxs-lookup"><span data-stu-id="21e3a-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="21e3a-112">Vorbereiten der Verwendung von CAPICOM</span><span class="sxs-lookup"><span data-stu-id="21e3a-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="21e3a-113">Verschlüsseln und Entschlüsseln von Daten</span><span class="sxs-lookup"><span data-stu-id="21e3a-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="21e3a-114">Signieren von Daten und Überprüfen digitaler Signaturen</span><span class="sxs-lookup"><span data-stu-id="21e3a-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="21e3a-115">Verwenden von Zertifikat speichern</span><span class="sxs-lookup"><span data-stu-id="21e3a-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="21e3a-116">Erstellen und empfangen von eingeschlossenen Daten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="21e3a-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
