---
description: Eine eingeschlossene Nachricht ist eine Nachricht, die für einen Empfänger oder eine Gruppe von Empfängern verschlüsselt ist.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Erstellen und empfangen von eingeschlossenen Daten Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354455"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="aeede-103">Erstellen und empfangen von eingeschlossenen Daten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="aeede-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="aeede-104">Eine eingeschlossene Nachricht ist eine Nachricht, die für eine Gruppe von Empfängern verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="aeede-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="aeede-105">Im Umschlag Prozess wird ein Sitzungs Verschlüsselungsschlüssel generiert, und die Nachricht wird mit diesem Schlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="aeede-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="aeede-106">Der Verschlüsselungsschlüssel selbst wird dann separat für jeden Empfänger verschlüsselt, wobei die öffentlichen Schlüssel aus dem Zertifikat des gewünschten Empfängers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aeede-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="aeede-107">Die eingeschlossene Nachricht besteht aus der verschlüsselten Nachricht, den Zertifikaten der vorgesehenen Empfänger und dem Satz verschlüsselter Schlüssel, einer für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="aeede-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="aeede-108">Die generierte Nachricht weist das [*PKCS \# 7*](../secgloss/p-gly.md)/CMS-Format auf.</span><span class="sxs-lookup"><span data-stu-id="aeede-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="aeede-109">In den folgenden Abschnitten werden Prozeduren und Beispiele für eingeschlossene Nachrichten Aufgaben beschrieben:</span><span class="sxs-lookup"><span data-stu-id="aeede-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="aeede-110">Codieren von eingeschlossenen Daten</span><span class="sxs-lookup"><span data-stu-id="aeede-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="aeede-111">Decodieren von eingeschlossenen Daten</span><span class="sxs-lookup"><span data-stu-id="aeede-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="aeede-112">Alternativer Code zum Codieren einer eingeschlossenen Nachricht</span><span class="sxs-lookup"><span data-stu-id="aeede-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="aeede-113">Beispiel-C-Programm: Codieren einer eingeschlossenen, signierten Nachricht</span><span class="sxs-lookup"><span data-stu-id="aeede-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
