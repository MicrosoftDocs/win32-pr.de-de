---
description: Die eingeschlossene Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger. Die generierte Nachricht weist das PKCS \# 7/CMS-Format auf.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Erstellen und empfangen von eingeschlossenen Daten Nachrichten in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343149"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="16bf0-104">Erstellen und empfangen von eingeschlossenen Daten Nachrichten in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="16bf0-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="16bf0-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16bf0-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="16bf0-106">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="16bf0-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="16bf0-107">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="16bf0-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="16bf0-108">Eine eingeschlossene Nachricht ist eine Nachricht, die für eine Gruppe von Empfängern verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="16bf0-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="16bf0-109">Im Umschlag Prozess wird ein Sitzungs Verschlüsselungsschlüssel generiert, und die Nachricht wird mit diesem Schlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="16bf0-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="16bf0-110">Der Verschlüsselungsschlüssel selbst wird dann separat für jeden Empfänger verschlüsselt, wobei die öffentlichen Schlüssel aus dem Zertifikat des gewünschten Empfängers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16bf0-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="16bf0-111">Die eingeschlossene Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="16bf0-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="16bf0-112">Die generierte Nachricht weist das PKCS \# 7/CMS-Format auf.</span><span class="sxs-lookup"><span data-stu-id="16bf0-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="16bf0-113">In den folgenden Abschnitten werden Prozeduren und Beispiele für eingeschlossene Nachrichten Aufgaben beschrieben:</span><span class="sxs-lookup"><span data-stu-id="16bf0-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="16bf0-114">Senden einer eingeschlossenen Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="16bf0-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="16bf0-115">Empfangen einer eingeschlossenen Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="16bf0-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



