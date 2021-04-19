---
description: Ein Sicherheitskontext ist der Satz von Sicherheits Attributen und Regeln, die während einer Kommunikationssitzung wirksam sind.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: SSPI-Kontext Semantik
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362864"
---
# <a name="sspi-context-semantics"></a><span data-ttu-id="e8949-103">SSPI-Kontext Semantik</span><span class="sxs-lookup"><span data-stu-id="e8949-103">SSPI Context Semantics</span></span>

<span data-ttu-id="e8949-104">Ein [*Sicherheitskontext*](../secgloss/s-gly.md) ist der Satz von Sicherheits Attributen und Regeln, die während einer Kommunikationssitzung wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="e8949-104">A [*security context*](../secgloss/s-gly.md) is the set of security attributes and rules in effect during a communication session.</span></span> <span data-ttu-id="e8949-105">Hierzu gehören Informationen wie die Identitäten des Prinzipals und Informationen über die verwendeten Schlüssel, Chiffren und Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="e8949-105">This includes such information as the identities of the principal and information on the keys, ciphers, and algorithms being used.</span></span> <span data-ttu-id="e8949-106">Bei der [*Security Support Provider-Schnittstelle (Security Support Provider Interface*](../secgloss/s-gly.md) , SSPI) ist ein Sicherheitskontext eine nicht transparente Struktur, die über einen Austausch mit der [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) -Funktion und der [**akzeptsecuritycontext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) -Funktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e8949-106">For [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), a security context is an opaque structure that is created through an exchange involving the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function and the [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span>

<span data-ttu-id="e8949-107">Weitere Informationen zu den Kontext Attributen finden Sie unter [Kontext Anforderungen](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8949-107">For more information about the context attributes, see [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="e8949-108">Das SSPI-Modell unterstützt drei Arten von Sicherheits Kontexten.</span><span class="sxs-lookup"><span data-stu-id="e8949-108">The SSPI model supports three types of security contexts.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8949-109">type</span><span class="sxs-lookup"><span data-stu-id="e8949-109">Type</span></span></th>
<th><span data-ttu-id="e8949-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8949-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8949-111"><a href="connection-oriented-contexts.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="e8949-111"><a href="connection-oriented-contexts.md">Connection</a></span></span></td>
<td><span data-ttu-id="e8949-112">Ein Verbindungs orientierter Kontext ist der gängigste Sicherheitskontext und der einfachste zu verwendende <a href="/windows/desktop/SecGloss/c-gly"><em>Kontext</em></a> .</span><span class="sxs-lookup"><span data-stu-id="e8949-112">A connection-oriented <a href="/windows/desktop/SecGloss/c-gly"><em>context</em></a> is the most common security context, and the simplest to use.</span></span> <span data-ttu-id="e8949-113">Der Aufrufer ist für das gesamte Nachrichtenformat und für den Speicherort der Daten in der Nachricht verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e8949-113">The caller is responsible for the overall message format and for the location of the data in the message.</span></span> <span data-ttu-id="e8949-114">Der Aufrufer ist auch für den Speicherort der sicherheitsrelevanten Felder innerhalb einer Nachricht zuständig, wie z. b. den Speicherort der Signatur Daten.</span><span class="sxs-lookup"><span data-stu-id="e8949-114">The caller is also responsible for the location of the security-relevant fields within a message, such as the location of the signature data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8949-115"><a href="datagram-contexts.md">Datagramm</a></span><span class="sxs-lookup"><span data-stu-id="e8949-115"><a href="datagram-contexts.md">Datagram</a></span></span></td>
<td><span data-ttu-id="e8949-116">Ein <a href="/windows/desktop/SecGloss/d-gly"><em>datagrammorientierter</em></a>Kontext bietet zusätzliche Unterstützung für die Datagramm-Kommunikation im DCE-Stil.</span><span class="sxs-lookup"><span data-stu-id="e8949-116">A <a href="/windows/desktop/SecGloss/d-gly"><em>datagram</em></a>-oriented context has extra support for DCE-style datagram communication.</span></span> <span data-ttu-id="e8949-117">Sie kann auch generisch für eine Datagramm-orientierte Transport Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8949-117">It can also be used generically for a datagram-oriented transport application.</span></span><br/>
<blockquote>
<p>[!Important]</p>
<p><span data-ttu-id="e8949-118">Das <a href="microsoft-kerberos.md">Microsoft Kerberos</a> -Paket unterstützt keine datagrammkontexte im Benutzer-zu-Benutzer-Modus.</span><span class="sxs-lookup"><span data-stu-id="e8949-118">The <a href="microsoft-kerberos.md">Microsoft Kerberos</a> package does not support datagram contexts in user-to-user mode.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8949-119"><a href="stream-contexts.md">Datenstrom</a></span><span class="sxs-lookup"><span data-stu-id="e8949-119"><a href="stream-contexts.md">Stream</a></span></span></td>
<td><span data-ttu-id="e8949-120">Ein Datenstrom orientierter Kontext ist für die Blockierung und Nachrichten Formatierung innerhalb des Sicherheitspakets verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e8949-120">A stream-oriented context is responsible for the blocking and message formatting within the security package.</span></span> <span data-ttu-id="e8949-121">Der Aufrufer ist nicht an der Formatierung interessiert, sondern vielmehr an einem unformatierten Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e8949-121">The caller is not interested in formatting, but rather a raw stream of data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e8949-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8949-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8949-123">Kontext Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8949-123">Context Requirements</span></span>](context-requirements.md)
</dt> <dt>

[<span data-ttu-id="e8949-124">Verbindungs orientierte Kontexte</span><span class="sxs-lookup"><span data-stu-id="e8949-124">Connection-Oriented Contexts</span></span>](connection-oriented-contexts.md)
</dt> <dt>

[<span data-ttu-id="e8949-125">Datagramm-Kontexte</span><span class="sxs-lookup"><span data-stu-id="e8949-125">Datagram Contexts</span></span>](datagram-contexts.md)
</dt> <dt>

[<span data-ttu-id="e8949-126">Streamkontexte</span><span class="sxs-lookup"><span data-stu-id="e8949-126">Stream Contexts</span></span>](stream-contexts.md)
</dt> </dl>

 

 
