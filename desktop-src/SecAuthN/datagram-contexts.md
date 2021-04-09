---
description: Die Semantik für Datagramm oder verbindungslose Kontexte unterscheidet sich geringfügig von denen für Verbindungs orientierte Kontexte.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Datagramm-Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129928"
---
# <a name="datagram-contexts"></a><span data-ttu-id="a761d-103">Datagramm-Kontexte</span><span class="sxs-lookup"><span data-stu-id="a761d-103">Datagram Contexts</span></span>

<span data-ttu-id="a761d-104">Die Semantik für [*Datagramm*](/windows/desktop/SecGloss/d-gly)oder verbindungslose Kontexte unterscheidet sich geringfügig von denen für Verbindungs orientierte Kontexte.</span><span class="sxs-lookup"><span data-stu-id="a761d-104">The semantics for [*datagram*](/windows/desktop/SecGloss/d-gly), or connectionless, contexts differ slightly from those for connection-oriented contexts.</span></span> <span data-ttu-id="a761d-105">Im Verbindungs losen [*Kontext*](/windows/desktop/SecGloss/c-gly)eines Datagramms kann ein Server nicht bestimmen, wann die Verbindung vom Client heruntergefahren oder anderweitig beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a761d-105">In a datagram's connectionless [*context*](/windows/desktop/SecGloss/c-gly), a server cannot determine when the client has shut down or otherwise terminated the connection.</span></span> <span data-ttu-id="a761d-106">Anders ausgedrückt: Es wird keine Abbruch Mitteilung von der Transport Anwendung an den Server übermittelt, wie es in einem Verbindungs orientierten Kontext der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="a761d-106">In other words, no termination notice is passed from the transport application to the server as would occur in a connection-oriented context.</span></span>

<span data-ttu-id="a761d-107">Um einen Datagramm-Kontext zu verwenden, legt ein Client das ISC \_ req- \_ Datagramm-Flag im-Befehl der [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="a761d-107">To use a datagram context, a client sets the ISC\_REQ\_DATAGRAM flag in its call to the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a761d-108">Das [Microsoft Kerberos](microsoft-kerberos.md) -Paket unterstützt keine datagrammkontexte im Benutzer-zu-Benutzer-Modus.</span><span class="sxs-lookup"><span data-stu-id="a761d-108">The [Microsoft Kerberos](microsoft-kerberos.md) package does not support datagram contexts in user-to-user mode.</span></span>

 

<span data-ttu-id="a761d-109">Um einige Modelle besser zu unterstützen, insbesondere RPC im DCE-Format, gelten die folgenden Regeln, wenn der Client einen Datagramm-Kontext verwendet:</span><span class="sxs-lookup"><span data-stu-id="a761d-109">To better support some models, particularly DCE-style RPC, the following rules apply when the client uses a datagram context:</span></span>

-   <span data-ttu-id="a761d-110">Das [*Sicherheitspaket*](/windows/desktop/SecGloss/s-gly) erzeugt beim ersten [**InitializeSecurityContext-Befehl (allgemein)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)kein Authentifizierungs- [*BLOB*](/windows/desktop/SecGloss/b-gly) (Binary Large Object).</span><span class="sxs-lookup"><span data-stu-id="a761d-110">The [*security package*](/windows/desktop/SecGloss/s-gly) does not produce an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) (binary large object) on the first call to [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span> <span data-ttu-id="a761d-111">Der Client kann jedoch den zurückgegebenen Sicherheitskontext in einem Rückruf der [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) -Funktion verwenden, um eine Signatur für eine Nachricht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a761d-111">However, the client can use the returned security context in a call to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a signature for a message.</span></span>
-   <span data-ttu-id="a761d-112">Das Sicherheitspaket muss zulassen, dass der Kontext mehrmals wieder hergestellt wird, damit der Server die Verbindung ohne vorherige Ankündigung löschen kann.</span><span class="sxs-lookup"><span data-stu-id="a761d-112">The security package must allow for the context to be re-established multiple times to allow the server to drop the connection without notice.</span></span> <span data-ttu-id="a761d-113">Dies impliziert, dass alle in den Funktionen [**makesignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) und [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) verwendeten Schlüssel in einen konsistenten [*Zustand*](/windows/desktop/SecGloss/s-gly)versetzt werden können.</span><span class="sxs-lookup"><span data-stu-id="a761d-113">This implies that any keys used in the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions can be reset to a consistent [*state*](/windows/desktop/SecGloss/s-gly).</span></span>
-   <span data-ttu-id="a761d-114">Das Sicherheitspaket ermöglicht dem Aufrufer, Sequenz Informationen anzugeben, und stellt diese Sequenz Informationen auf Empfängerseite bereit.</span><span class="sxs-lookup"><span data-stu-id="a761d-114">The security package allows the caller to specify sequence information, and provides that sequence information at the receiver side.</span></span> <span data-ttu-id="a761d-115">Dies gilt zusätzlich zu den vom Paket verwalteten Sequenz Informationen.</span><span class="sxs-lookup"><span data-stu-id="a761d-115">This is in addition to any sequence information maintained by the package.</span></span>

<span data-ttu-id="a761d-116">Ein Sicherheitspaket legt das Datagramm-Flag "secpkg Flag" fest, \_ \_ um anzugeben, dass es datagrammsemantik unterstützt</span><span class="sxs-lookup"><span data-stu-id="a761d-116">A security package sets the SECPKG\_FLAG\_DATAGRAM flag to indicate that it supports datagram semantics.</span></span>

 

 
