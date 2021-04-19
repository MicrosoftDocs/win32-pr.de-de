---
description: Cryptographic Message Syntax (CMS), abgeleitet von PKCS \# 7 Version 1,5, ist die Syntax, die zum Hashen, digitalen Signieren, authentifizieren und verschlüsseln beliebiger Nachrichten verwendet wird.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: CMS-Ergänzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372959"
---
# <a name="cms-additions"></a><span data-ttu-id="e5346-103">CMS-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="e5346-103">CMS Additions</span></span>

<span data-ttu-id="e5346-104">Cryptographic Message Syntax (CMS), abgeleitet von PKCS \# 7 Version 1,5, ist die Syntax, die zum [*Hashen*](../secgloss/h-gly.md), [*digitalen Signieren*](../secgloss/d-gly.md), authentifizieren und verschlüsseln beliebiger Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5346-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="e5346-105">Wenn möglich, wird die Abwärtskompatibilität beibehalten. Es wurden jedoch Änderungen vorgenommen, um Attribut Zertifikat Übertragung und Schlüssel Übereinstimmungs Verfahren für die Schlüsselverwaltung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e5346-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="e5346-106">CMS ermöglicht mehrere Kapselung, sodass ein Kapselungs Umschlag in einen anderen geschachtelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5346-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="e5346-107">Außerdem kann eine Partei zuvor gekapselte Daten digital signieren. beliebige Attribute, z. b. die Signatur Zeit, können zusammen mit dem Nachrichten Inhalt signiert werden. das-Attribut und das-Attribut, wie z. b. [*countersignaturen*](../secgloss/c-gly.md), können einer Signatur zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="e5346-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="e5346-108">CMS kann eine Vielzahl von Architekturen für die Zertifikat basierte Schlüsselverwaltung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e5346-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="e5346-109">Um zusätzliche CMS-Funktionen zu unterstützen, wurden den zugrunde liegenden Datenstrukturen neue Felder zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e5346-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="e5346-110">Neue Flags und Parameterwerte wurden ebenfalls hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e5346-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="e5346-111">Alle Datenstrukturen und alle APIs, die CMS verwenden, sind 100 Prozent abwärts kompatibel mit PKCS \# 7, Version 1,5.</span><span class="sxs-lookup"><span data-stu-id="e5346-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="e5346-112">Zu den Ergänzungen zählen eingeschlossene [Daten Ergänzungen](enveloped-data-additions.md) und [signierte Daten Ergänzungen](signed-data-additions.md).</span><span class="sxs-lookup"><span data-stu-id="e5346-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
