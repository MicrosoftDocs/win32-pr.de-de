---
description: Stellen Sie eine Verbindung mit einer bestimmten Smartcard her und kommunizieren Sie.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Smartcard-und Reader-Zugriffs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363299"
---
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="7b4ea-103">Smartcard-und Reader-Zugriffs Funktionen</span><span class="sxs-lookup"><span data-stu-id="7b4ea-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="7b4ea-104">Die folgenden Funktionen stellen eine Verbindung mit einer bestimmten [*Smartcard*](../secgloss/s-gly.md)her und kommunizieren mit Ihnen.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="7b4ea-105">E/a-Vorgänge für die Karte verwenden einen Puffer zum Senden oder empfangen von Daten sowie eine Struktur, die Protokoll Steuerungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="7b4ea-106">Die Struktur der Protokoll Steuerungsinformationen beginnt immer mit einer " [**SCard \_ IO \_ Request**](scard-io-request.md) "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="7b4ea-107">Thema</span><span class="sxs-lookup"><span data-stu-id="7b4ea-107">Topic</span></span>                                                  | <span data-ttu-id="7b4ea-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b4ea-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b4ea-109">**Scardconnect**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="7b4ea-110">Herstellen einer Verbindung mit einer Karte</span><span class="sxs-lookup"><span data-stu-id="7b4ea-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="7b4ea-111">**Scardreconnect**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="7b4ea-112">Stellen Sie eine Verbindung wieder her.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="7b4ea-113">**"Scarddisconnect"**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="7b4ea-114">Beenden Sie eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="7b4ea-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="7b4ea-116">Starten Sie eine [*Transaktion*](../secgloss/t-gly.md), und blockieren Sie den Zugriff auf eine Karte durch andere Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="7b4ea-117">**"SCardEndTransaction"**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="7b4ea-118">Beenden Sie eine Transaktion, sodass andere Anwendungen auf eine Karte zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="7b4ea-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="7b4ea-120">Geben Sie den aktuellen Status des Readers an.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="7b4ea-121">**Scardüberträgt**</span><span class="sxs-lookup"><span data-stu-id="7b4ea-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="7b4ea-122">Fordert den Dienst an und empfängt Daten mit [*t = 0*](../secgloss/t-gly.md), [*t = 1*](../secgloss/t-gly.md)und unformatierten Protokollen von einer Karte zurück.</span><span class="sxs-lookup"><span data-stu-id="7b4ea-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 
