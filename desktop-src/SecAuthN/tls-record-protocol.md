---
description: Das TLS-Daten Satz Protokoll (Transport Layer Security) sichert Anwendungsdaten mit den Schlüsseln, die während des Handshakes erstellt werden.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: TLS-Daten Satz Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356957"
---
# <a name="tls-record-protocol"></a><span data-ttu-id="23593-103">TLS-Daten Satz Protokoll</span><span class="sxs-lookup"><span data-stu-id="23593-103">TLS Record Protocol</span></span>

<span data-ttu-id="23593-104">Das TLS-Daten Satz Protokoll ( [*Transport Layer Security*](../secgloss/t-gly.md) ) sichert Anwendungsdaten mit den Schlüsseln, die während des [Handshakes](tls-handshake-protocol.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23593-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="23593-105">Das Daten Satz Protokoll ist für das Sichern von Anwendungsdaten und das Überprüfen der [*Integrität*](../secgloss/i-gly.md) und des Ursprungs zuständig.</span><span class="sxs-lookup"><span data-stu-id="23593-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="23593-106">Folgendes wird verwaltet:</span><span class="sxs-lookup"><span data-stu-id="23593-106">It manages the following:</span></span>

-   <span data-ttu-id="23593-107">Aufteilen ausgehender Nachrichten in verwaltbare Blöcke und Wiederherstellen eingehender Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="23593-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="23593-108">Komprimieren von ausgehenden Blöcken und das Komprimieren eingehender Blöcke (optional).</span><span class="sxs-lookup"><span data-stu-id="23593-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="23593-109">Anwenden eines [*Nachrichtenauthentifizierungscode*](../secgloss/m-gly.md) (Mac) auf ausgehende Nachrichten und Überprüfen eingehender Nachrichten mit dem Mac.</span><span class="sxs-lookup"><span data-stu-id="23593-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="23593-110">Verschlüsseln von ausgehenden Nachrichten und entschlüsseln eingehender Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="23593-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="23593-111">Wenn das Datensatz-Protokoll fertiggestellt ist, werden die ausgehenden verschlüsselten Daten für den Transport an die TCP-Schicht (Transmission Control Protocol) weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="23593-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
