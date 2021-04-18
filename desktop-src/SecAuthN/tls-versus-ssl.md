---
description: TLS ist ein Standard, der eng mit SSL 3,0 verknüpft ist, und wird manchmal auch als "&\# 0034;" bezeichnet. SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS und SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352242"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="287c5-103">TLS und SSL</span><span class="sxs-lookup"><span data-stu-id="287c5-103">TLS vs. SSL</span></span>

<span data-ttu-id="287c5-104">TLS ist ein Standard, der eng mit SSL 3,0 verknüpft ist, und wird manchmal als "SSL 3,1" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="287c5-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="287c5-105">TLS ersetzt SSL 2,0 und sollte bei der neuen Entwicklung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="287c5-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="287c5-106">Ab Windows 10, Version 1607 und Windows Server 2016, wurde SSL 2,0 entfernt und wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="287c5-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="287c5-107">Anwendungen, die ein hohes Maß an Interoperabilität erfordern, sollten SSL 3,0 und TLS unterstützen.</span><span class="sxs-lookup"><span data-stu-id="287c5-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="287c5-108">Aufgrund der Ähnlichkeiten zwischen diesen beiden Protokollen sind SSL-Details in dieser Dokumentation nicht enthalten, es sei denn, Sie unterscheiden sich von TLS.</span><span class="sxs-lookup"><span data-stu-id="287c5-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="287c5-109">In [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt)ist Folgendes zu finden:</span><span class="sxs-lookup"><span data-stu-id="287c5-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="287c5-110">"Die Unterschiede zwischen diesem Protokoll und SSL 3,0 sind nicht dramatisch, aber Sie sind so bedeutend genug, dass TLS 1,0 und SSL 3,0 nicht zusammenarbeiten (obwohl TLS 1,0 einen Mechanismus integriert, mit dem eine TLS-Implementierung auf SSL-3,0 zurückgreifen kann)."</span><span class="sxs-lookup"><span data-stu-id="287c5-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



