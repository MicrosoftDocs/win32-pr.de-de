---
description: Enthält Definitionen von Sicherheits Begriffen, die mit dem Buchstaben I beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: af511aed-88f5-4b12-ad44-317925297f70
title: I (Sicherheits Glossar)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d3e727128c2494f313bdffc879b5c5e47a28ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042600"
---
# <a name="i-security-glossary"></a><span data-ttu-id="054be-103">I (Sicherheits Glossar)</span><span class="sxs-lookup"><span data-stu-id="054be-103">I (Security Glossary)</span></span>

<span data-ttu-id="054be-104">[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="054be-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) I J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="054be-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**Ausschalten**</span><span class="sxs-lookup"><span data-stu-id="054be-105"><span id="_security_iis_gly"></span><span id="_SECURITY_IIS_GLY"></span>**IIS**</span></span>
</dt> <dd>

<span data-ttu-id="054be-106">Software Dienste, die die Erstellung, Konfiguration und Verwaltung von Websites sowie andere Internet Funktionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="054be-106">Software services that support website creation, configuration, and management, along with other Internet functions.</span></span> <span data-ttu-id="054be-107">Internetinformationsdienste include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP) und Simple Mail Transfer Protocol (SMTP).</span><span class="sxs-lookup"><span data-stu-id="054be-107">Internet Information Services include Network News Transfer Protocol (NNTP), File Transfer Protocol (FTP), and Simple Mail Transfer Protocol (SMTP).</span></span> <span data-ttu-id="054be-108">IIS umfasst verschiedene Funktionen für die Sicherheit, ermöglicht CGI-Anwendungen und bietet Gopher-und FTP-Server.</span><span class="sxs-lookup"><span data-stu-id="054be-108">IIS incorporates various functions for security, allows for CGI applications, and provides for Gopher and FTP servers.</span></span>

</dd> <dt>

<span data-ttu-id="054be-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**Identitätswechsel**</span><span class="sxs-lookup"><span data-stu-id="054be-109"><span id="_security_impersonation_gly"></span><span id="_SECURITY_IMPERSONATION_GLY"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="054be-110">Ein Mechanismus, mit dem ein Server Prozess mithilfe der Sicherheits Anmelde Informationen des Clients oder eines anderen Benutzers ausgeführt werden kann, der die Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="054be-110">A mechanism that allows a server process to run by using the security credentials of the client or some other user using the credentials.</span></span> <span data-ttu-id="054be-111">Wenn der Server die Identität des Clients annimmt, werden alle Vorgänge, die vom Server ausgeführt werden, mithilfe der Anmelde Informationen des Clients (Identität des Benutzers) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="054be-111">When the server is impersonating the client, any operations performed by the server are performed by using the client's (impersonating user's) credentials.</span></span> <span data-ttu-id="054be-112">Durch den Identitätswechsel kann der Server nicht auf Remote Ressourcen im Namen des Clients zugreifen.</span><span class="sxs-lookup"><span data-stu-id="054be-112">Impersonation does not allow the server to access remote resources on behalf of the client.</span></span> <span data-ttu-id="054be-113">Hierfür ist eine Delegierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="054be-113">This requires delegation.</span></span>

</dd> <dt>

<span data-ttu-id="054be-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**Identitätswechsel Token**</span><span class="sxs-lookup"><span data-stu-id="054be-114"><span id="_security_impersonation_token_gly"></span><span id="_SECURITY_IMPERSONATION_TOKEN_GLY"></span>**impersonation token**</span></span>
</dt> <dd>

<span data-ttu-id="054be-115">Ein Zugriffs Token, das erstellt wurde, um die Sicherheitsinformationen eines Client Prozesses zu erfassen, sodass ein Server die Identität des Client Prozesses in sicherheitsvorgängen annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="054be-115">An access token that has been created to capture the security information of a client process, allowing a server to "impersonate" the client process in security operations.</span></span>

<span data-ttu-id="054be-116">Siehe auch [*Zugriffs Token*](a-gly.md) und [*primäres Token*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="054be-116">See also [*access token*](a-gly.md) and [*primary token*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="054be-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**Initialisierungs Vektor**</span><span class="sxs-lookup"><span data-stu-id="054be-117"><span id="_security_initialization_vector_gly"></span><span id="_SECURITY_INITIALIZATION_VECTOR_GLY"></span>**initialization vector**</span></span>
</dt> <dd>

<span data-ttu-id="054be-118">(IV) eine Sequenz zufälliger bytes, die vor der Verschlüsselung durch eine Blockchiffre an den Anfang des Klartext angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="054be-118">(IV) A sequence of random bytes appended to the front of the plaintext before encryption by a block cipher.</span></span> <span data-ttu-id="054be-119">Wenn Sie den Initialisierungs Vektor am Anfang des Klartext hinzufügen, ist es nicht mehr möglich, den ursprünglichen Chiffre Text für zwei Nachrichten gleich zu lassen.</span><span class="sxs-lookup"><span data-stu-id="054be-119">Adding the initialization vector to the beginning of the plaintext eliminates the possibility of having the initial ciphertext block the same for any two messages.</span></span> <span data-ttu-id="054be-120">Wenn Nachrichten z. b. immer mit einem gemeinsamen Header (einem Brief Kopf oder einer "von"-Zeile) beginnen, wäre Ihr ursprünglicher Chiffre Text immer identisch, wobei angenommen wird, dass derselbe Kryptografiealgorithmus und derselbe symmetrische Schlüssel verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="054be-120">For example, if messages always start with a common header (a letterhead or "From" line) their initial ciphertext would always be the same, assuming that the same cryptographic algorithm and symmetric key was used.</span></span> <span data-ttu-id="054be-121">Durch das Hinzufügen eines zufälligen Initialisierungs Vektors wird dies vermieden.</span><span class="sxs-lookup"><span data-stu-id="054be-121">Adding a random initialization vector eliminates this from happening.</span></span>

</dd> <dt>

<span data-ttu-id="054be-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**Innere Daten**</span><span class="sxs-lookup"><span data-stu-id="054be-122"><span id="_security_inner_data_gly"></span><span id="_SECURITY_INNER_DATA_GLY"></span>**inner data**</span></span>
</dt> <dd>

<span data-ttu-id="054be-123">Alle codierten Daten, die als Nachricht für eine andere codierte Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="054be-123">Any encoded data used as the message for another encoded message.</span></span> <span data-ttu-id="054be-124">Eine eingeschlossene Nachricht und Ihr Hashwert können z. b. die inneren Daten für eine zweite Nachricht sein.</span><span class="sxs-lookup"><span data-stu-id="054be-124">For example, an enveloped message and its hash value may be the inner data for a second message.</span></span>

</dd> <dt>

<span data-ttu-id="054be-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**innerer Inhalt**</span><span class="sxs-lookup"><span data-stu-id="054be-125"><span id="_security_inner_content_gly"></span><span id="_SECURITY_INNER_CONTENT_GLY"></span>**inner content**</span></span>
</dt> <dd>

<span data-ttu-id="054be-126">Erweiterte Daten, z. b. mit einer digitalen Signatur.</span><span class="sxs-lookup"><span data-stu-id="054be-126">Data that is enhanced, such as with a digital signature.</span></span> <span data-ttu-id="054be-127">Dieser Begriff wird hauptsächlich bei der Erörterung von erweiterten Daten in einer PKCS \# 7-Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="054be-127">This term is used primarily when discussing enhanced data in a PKCS \#7 message.</span></span>

</dd> <dt>

<span data-ttu-id="054be-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**Integrität**</span><span class="sxs-lookup"><span data-stu-id="054be-128"><span id="_security_integrity_gly"></span><span id="_SECURITY_INTEGRITY_GLY"></span>**integrity**</span></span>
</dt> <dd>

<span data-ttu-id="054be-129">Die Vollständigkeit und Genauigkeit einer Nachricht, nachdem Sie gesendet oder gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="054be-129">The completeness and accuracy of a message after it has been sent or stored.</span></span>

</dd> <dt>

<span data-ttu-id="054be-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**Integritäts-sid**</span><span class="sxs-lookup"><span data-stu-id="054be-130"><span id="_security_integrity_sid_gly"></span><span id="_SECURITY_INTEGRITY_SID_GLY"></span>**integrity SID**</span></span>
</dt> <dd>

<span data-ttu-id="054be-131">Eine [*Sicherheits*](s-gly.md) -ID (SID), die eine Integritäts Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="054be-131">A [*security identifier*](s-gly.md) (SID) that represents an integrity level.</span></span> <span data-ttu-id="054be-132">Eine Integritäts-sid in der [*System-Zugriffs Steuerungs Liste*](s-gly.md) (SACL) der Sicherheits Beschreibung eines Objekts gibt die Integritäts Stufe des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="054be-132">An integrity SID in the [*system access control list*](s-gly.md) (SACL) of an object's security descriptor specifies the integrity level of the object.</span></span> <span data-ttu-id="054be-133">Integritäts-SIDs in einem Zugriffs Token geben die Integritäts Stufe des Tokens an.</span><span class="sxs-lookup"><span data-stu-id="054be-133">Integrity SIDs in an access token specify the integrity level of the token.</span></span>

</dd> <dt>

<span data-ttu-id="054be-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span><span class="sxs-lookup"><span data-stu-id="054be-134"><span id="_security_interrupt_request_level_gly"></span><span id="_SECURITY_INTERRUPT_REQUEST_LEVEL_GLY"></span>**IRQL**</span></span>
</dt> <dd>

<span data-ttu-id="054be-135">Eine Interrupt Request Level (unql) definiert die Hardware Priorität, mit der ein Prozessor zu einem beliebigen Zeitpunkt arbeitet.</span><span class="sxs-lookup"><span data-stu-id="054be-135">An interrupt request level (IRQL) defines the hardware priority at which a processor operates at any given time.</span></span> <span data-ttu-id="054be-136">In der Windows-Treibermodell kann ein Thread, der mit einem niedrigen "iriql" ausgeführt wird, unterbrochen werden, um Code bei einem höheren "iriql" auszuführen.</span><span class="sxs-lookup"><span data-stu-id="054be-136">In the Windows Driver Model, a thread running at a low IRQL can be interrupted to run code at a higher IRQL.</span></span>

</dd> <dt>

<span data-ttu-id="054be-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**Heinrich**</span><span class="sxs-lookup"><span data-stu-id="054be-137"><span id="_security_iv_gly"></span><span id="_SECURITY_IV_GLY"></span>**IV**</span></span>
</dt> <dd>

<span data-ttu-id="054be-138">Siehe *Initialisierungs Vektor*.</span><span class="sxs-lookup"><span data-stu-id="054be-138">See *initialization vector*.</span></span>

</dd> </dl>

 

 



