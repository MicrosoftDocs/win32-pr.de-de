---
description: SChannel unterstützt die Versionen 1,0, 1,1 und 1,2 des Transport Layer Security (TLS)-Protokolls.
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: TLS-Protokoll (Transport Layer Security)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364113"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="8f44e-103">TLS-Protokoll (Transport Layer Security)</span><span class="sxs-lookup"><span data-stu-id="8f44e-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="8f44e-104">SChannel unterstützt die Versionen 1,0, 1,1 und 1,2 des [*Transport Layer Security (TLS)-Protokolls*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8f44e-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="8f44e-105">Dieses Protokoll ist ein Industriestandard, der den Schutz der über das Internet kommunizierten Informationen schützt.</span><span class="sxs-lookup"><span data-stu-id="8f44e-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="8f44e-106">TLS geht davon aus, dass ein Verbindungs orientierter Transport (in der Regel TCP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f44e-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="8f44e-107">Das TLS-Protokoll ermöglicht es Client/Server-Anwendungen, die folgenden Sicherheitsrisiken zu erkennen:</span><span class="sxs-lookup"><span data-stu-id="8f44e-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="8f44e-108">Manipulation von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="8f44e-108">Message tampering</span></span>
-   <span data-ttu-id="8f44e-109">Abfangen der Nachricht</span><span class="sxs-lookup"><span data-stu-id="8f44e-109">Message interception</span></span>
-   <span data-ttu-id="8f44e-110">Nachrichten Fälschung</span><span class="sxs-lookup"><span data-stu-id="8f44e-110">Message forgery</span></span>

<span data-ttu-id="8f44e-111">Die vollständige Spezifikation des TLS-Protokolls ist auf der IETF-Website verfügbar: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .</span><span class="sxs-lookup"><span data-stu-id="8f44e-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="8f44e-112">TLS-Organisation</span><span class="sxs-lookup"><span data-stu-id="8f44e-112">Organization of TLS</span></span>

<span data-ttu-id="8f44e-113">Die folgenden Schritte sind bei der Verwendung von TLS für die Client/Server-Kommunikation beteiligt:</span><span class="sxs-lookup"><span data-stu-id="8f44e-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="8f44e-114">**So verwenden Sie TLS für die Client/Server-Kommunikation**</span><span class="sxs-lookup"><span data-stu-id="8f44e-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="8f44e-115">Hand Shake-und Chiffre Suite-Aushandlung</span><span class="sxs-lookup"><span data-stu-id="8f44e-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="8f44e-116">Authentifizierung von Parteien</span><span class="sxs-lookup"><span data-stu-id="8f44e-116">Authentication of parties</span></span>
3.  <span data-ttu-id="8f44e-117">Schlüssel bezogener Informationsaustausch</span><span class="sxs-lookup"><span data-stu-id="8f44e-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="8f44e-118">Anwendungsdaten Austausch</span><span class="sxs-lookup"><span data-stu-id="8f44e-118">Application data exchange</span></span>

<span data-ttu-id="8f44e-119">Die Schritte, die TLS bilden, sind in zwei Protokolle unterteilt, die zusammen die Verbindungssicherheit bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="8f44e-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="8f44e-120">[TLS-Handshake-Protokoll](tls-handshake-protocol.md)– (Schritte 1 – 3)</span><span class="sxs-lookup"><span data-stu-id="8f44e-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="8f44e-121">[TLS-Daten Satz Protokoll](tls-record-protocol.md)– (Schritt 4)</span><span class="sxs-lookup"><span data-stu-id="8f44e-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="8f44e-122">SSPI mit TLS-Implementierungen</span><span class="sxs-lookup"><span data-stu-id="8f44e-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="8f44e-123">Da TLS keine GSSAPI-Spezifikation hat, sind TLS-Implementierer möglicherweise nicht mit den SSPI-Funktionen vertraut.</span><span class="sxs-lookup"><span data-stu-id="8f44e-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="8f44e-124">Anwendungen rufen die SSPI-Funktionen zum Auflisten verfügbarer Pakete, zum Erstellen und Bearbeiten von Handles für Anmelde Informationen, zum Erstellen von Sicherheits Kontexten und zum Schutz der Nachrichten Integrität auf.</span><span class="sxs-lookup"><span data-stu-id="8f44e-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="8f44e-125">Um die von Benutzermodusanwendungen verwendeten SSPI-Funktionen zu unterstützen, müssen die Funktionen, die in Funktionen aufgelistet sind, die [von SSP/APS im Benutzermodus implementiert](/windows/desktop/SecAuthN/authentication-functions) werden, von TLS-Implementierungen wie schannel.dll unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8f44e-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="8f44e-126">Ausführliche Informationen zu den SSPI-Funktionen und SSP-Funktionen finden Sie unter [Authentifizierungsfunktionen](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8f44e-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f44e-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f44e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f44e-128">TLS-Verschlüsselungs Sammlungen</span><span class="sxs-lookup"><span data-stu-id="8f44e-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="8f44e-129">TLS und SSL</span><span class="sxs-lookup"><span data-stu-id="8f44e-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
