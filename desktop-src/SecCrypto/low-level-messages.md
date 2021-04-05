---
description: Die Nachrichten Funktionen auf niedriger Ebene codieren Daten für die Übertragung und Decodierung von Daten, die empfangen wurden. Auf Low-Level-Nachrichten Funktionen werden auch die Signaturen empfangener Nachrichten entschlüsselt und überprüft.
ms.assetid: 42c19920-c7f7-4a4d-9de3-3de9a34fbe0c
title: Nachrichten Funktionen auf niedriger Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22654f19dfe5178dfb98006c17c2d0536f78cd46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752129"
---
# <a name="low-level-message-functions"></a><span data-ttu-id="20190-104">Nachrichten Funktionen auf niedriger Ebene</span><span class="sxs-lookup"><span data-stu-id="20190-104">Low-level Message Functions</span></span>

<span data-ttu-id="20190-105">Die [*Nachrichten Funktionen auf niedriger Ebene*](../secgloss/l-gly.md) codieren Daten für die Übertragung und Decodierung von Daten, die empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="20190-105">The [*low-level message functions*](../secgloss/l-gly.md) encode data for transmission and decode data that has been received.</span></span> <span data-ttu-id="20190-106">Auf Low-Level-Nachrichten Funktionen werden auch die Signaturen empfangener Nachrichten entschlüsselt und überprüft.</span><span class="sxs-lookup"><span data-stu-id="20190-106">Low-level message functions also decrypt and verify the signatures of received messages.</span></span>

<span data-ttu-id="20190-107">Wenn eine Nachricht mithilfe einer Funktion zum Öffnen von Nachrichten auf niedriger Ebene geöffnet wird, bleibt sie offen und verfügbar (behält ihren [*Zustand*](../secgloss/s-gly.md)bei), bis Sie geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="20190-107">When a message is opened using a low-level message open function, it remains open and available (maintains its [*state*](../secgloss/s-gly.md)) until it is closed.</span></span> <span data-ttu-id="20190-108">Dadurch kann eine Nachricht schrittweise mithilfe mehrerer Aufrufe der [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) -Funktion erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="20190-108">This allows a message to be constructed piecemeal using multiple calls to the [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) function.</span></span>

<span data-ttu-id="20190-109">Die Verwendung von Nachrichten Funktionen auf niedriger Ebene erfordert mehr Funktionsaufrufe als die Verwendung von vereinfachten Nachrichten Funktionen (siehe [vereinfachte Meldungen](simplified-messages.md)).</span><span class="sxs-lookup"><span data-stu-id="20190-109">Using low-level message functions requires more function calls than using simplified message functions (see [Simplified Messages](simplified-messages.md)).</span></span> <span data-ttu-id="20190-110">Wenn die vereinfachten Nachrichten Funktionen verwendet werden, wird mehr Arbeit innerhalb der Funktionen der API ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20190-110">If the simplified message functions are used, more of the work is done inside the functions of the API.</span></span>

<span data-ttu-id="20190-111">Die Verwendung von Nachrichten Funktionen auf niedriger Ebene umfasst die zusätzliche Arbeit bei Aufrufen von anderen Zertifikaten oder Kryptografiefunktionen.</span><span class="sxs-lookup"><span data-stu-id="20190-111">Using low-level message functions involves the additional work of making calls to other certificate or cryptographic functions.</span></span> <span data-ttu-id="20190-112">Beispielsweise können Daten aus Aufrufen von Zertifikat Funktionen zum Initialisieren von Strukturen benötigt werden, die von diesen Low-Level-Nachrichten Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20190-112">For example, data from calls to certificate functions may be needed to initialize structures used by these low-level message functions.</span></span> <span data-ttu-id="20190-113">Vereinfachte Nachrichten Funktionen initialisieren viele dieser Strukturen intern.</span><span class="sxs-lookup"><span data-stu-id="20190-113">Simplified message functions initialize many of these structures internally.</span></span>

<span data-ttu-id="20190-114">In der folgenden Tabelle sind Abschnitte mit Prozedur Beschreibungen und C-Codebeispiele für die Verwendung der Funktionen auf niedriger Ebene aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="20190-114">The following table lists sections with procedure descriptions and C code examples of using the low-level message functions.</span></span>



| <span data-ttu-id="20190-115">`Section`</span><span class="sxs-lookup"><span data-stu-id="20190-115">Section</span></span>                                                                               | <span data-ttu-id="20190-116">Contents</span><span class="sxs-lookup"><span data-stu-id="20190-116">Contents</span></span>                                           |
|---------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="20190-117">Nachrichten Funktionen auf niedriger Ebene</span><span class="sxs-lookup"><span data-stu-id="20190-117">Low-level Message Functions</span></span>](cryptography-functions.md) | <span data-ttu-id="20190-118">Listet die Nachrichten Funktionen auf niedriger Ebene auf.</span><span class="sxs-lookup"><span data-stu-id="20190-118">Lists the low-level message functions.</span></span>             |
| [<span data-ttu-id="20190-119">Signieren von Daten</span><span class="sxs-lookup"><span data-stu-id="20190-119">Signing Data</span></span>](signing-data.md)                                                      | <span data-ttu-id="20190-120">Erläutert die zum Signieren von Daten erforderlichen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="20190-120">Details the tasks needed to sign data.</span></span>             |
| [<span data-ttu-id="20190-121">Codieren von eingeschlossenen Daten</span><span class="sxs-lookup"><span data-stu-id="20190-121">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)                                | <span data-ttu-id="20190-122">Erläutert die Aufgaben, die zum Codieren von eingeschlossenen Daten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="20190-122">Details the tasks needed to encode enveloped data.</span></span> |
| [<span data-ttu-id="20190-123">Decodieren von eingeschlossenen Daten</span><span class="sxs-lookup"><span data-stu-id="20190-123">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)                                | <span data-ttu-id="20190-124">Erläutert die Aufgaben, die zum Decodieren von eingeschlossenen Daten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="20190-124">Details the tasks needed to decode enveloped data.</span></span> |



 

 

 
