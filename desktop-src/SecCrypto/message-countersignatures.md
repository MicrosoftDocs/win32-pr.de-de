---
description: Manchmal erfordert eine signierte Nachricht eine gegen Signatur.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Nachrichten gegen Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752128"
---
# <a name="message-countersignatures"></a><span data-ttu-id="2cfab-103">Nachrichten gegen Signaturen</span><span class="sxs-lookup"><span data-stu-id="2cfab-103">Message Countersignatures</span></span>

<span data-ttu-id="2cfab-104">Manchmal erfordert eine signierte Nachricht eine [*gegen Signatur*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2cfab-104">Sometimes a signed message requires a [*countersignature*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2cfab-105">Beispielsweise kann Benutzer a eine signierte Daten Nachricht an Benutzer B senden, wobei B erwartet, dass die Vereinbarung mit den im Dokument enthaltenen Begriffen bestätigt wird.</span><span class="sxs-lookup"><span data-stu-id="2cfab-105">For example, user A may send a signed-data message to user B, expecting B to confirm agreement with the terms contained in the document.</span></span> <span data-ttu-id="2cfab-106">Benutzer B decodiert die Nachricht, liest die Begriffe und signiert die Nachricht, wenn Sie in der Vereinbarung steht.</span><span class="sxs-lookup"><span data-stu-id="2cfab-106">User B decodes the message, reads the terms and, if in agreement, countersigns the message.</span></span> <span data-ttu-id="2cfab-107">Die gegen signierte Nachricht wird dann an Benutzer a zurückgesendet. Benutzer a weiß nun, dass der Benutzer B den Bedingungen zugestimmt hat.</span><span class="sxs-lookup"><span data-stu-id="2cfab-107">The countersigned message is then sent back to user A. User A now knows, and can prove, that user B agreed to the terms.</span></span>

<span data-ttu-id="2cfab-108">In der folgenden Tabelle sind Abschnitte aufgelistet, die Prozedur Beschreibungen oder C-Programmbeispiele für die Nachrichten gegen Signierung enthalten.</span><span class="sxs-lookup"><span data-stu-id="2cfab-108">The following table lists sections that contain procedure descriptions or C program examples of message countersigning.</span></span>



| <span data-ttu-id="2cfab-109">`Section`</span><span class="sxs-lookup"><span data-stu-id="2cfab-109">Section</span></span>                                                                                                                                 | <span data-ttu-id="2cfab-110">Contents</span><span class="sxs-lookup"><span data-stu-id="2cfab-110">Contents</span></span>                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="2cfab-111">Nachrichtenfunktionen</span><span class="sxs-lookup"><span data-stu-id="2cfab-111">Message Functions</span></span>](cryptography-functions.md)                                                                       | <span data-ttu-id="2cfab-112">Listet die gegen Signatur Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="2cfab-112">Lists the counter signature functions.</span></span>                             |
| [<span data-ttu-id="2cfab-113">Gegen Signieren einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="2cfab-113">Countersigning a Message</span></span>](countersigning-a-message.md)                                                                                | <span data-ttu-id="2cfab-114">Erläutert den Prozess der gegen Signierung einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2cfab-114">Details the process of counter signing a message.</span></span>                  |
| [<span data-ttu-id="2cfab-115">Überprüfen einer gegen Signatur</span><span class="sxs-lookup"><span data-stu-id="2cfab-115">Verifying a Countersignature</span></span>](verifying-a-countersignature.md)                                                                        | <span data-ttu-id="2cfab-116">Erläutert das Verfahren zum Überprüfen einer gegen Signatur.</span><span class="sxs-lookup"><span data-stu-id="2cfab-116">Details the procedure for verifying a counter signature.</span></span>           |
| [<span data-ttu-id="2cfab-117">Überprüfen einer signierten Nachricht</span><span class="sxs-lookup"><span data-stu-id="2cfab-117">Verifying a Signed Message</span></span>](verifying-a-signed-message.md)                                                                            | <span data-ttu-id="2cfab-118">Erläutert einen Prozess zum Überprüfen der Signatur in einer signierten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2cfab-118">Details a process for verifying the signature on a signed message.</span></span> |
| [<span data-ttu-id="2cfab-119">Beispiel-C-Programm: Codieren und Decodieren einer gegen signierten Nachricht</span><span class="sxs-lookup"><span data-stu-id="2cfab-119">Example C Program: Encoding and Decoding a CounterSigned Message</span></span>](example-c-program-encoding-and-decoding-a-countersigned-message.md) | <span data-ttu-id="2cfab-120">Beispiel-C-Programm, das eine gegen signierte Nachricht codiert und decodiert.</span><span class="sxs-lookup"><span data-stu-id="2cfab-120">Sample C program that encodes and decodes a countersigned message.</span></span> |



 

 

 
