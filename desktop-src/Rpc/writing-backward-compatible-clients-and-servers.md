---
title: Schreiben von abwärts kompatiblen Clients und Servern
description: Theoretisch hilft das Versions Schema von RPC dabei, eine Fehlkommunikation zwischen geänderten Servern und Clients und ihren bereitgestellten Gegenstücken zu verhindern.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- Remote Prozedur Aufruf RPC, bewährte Methoden, Abwärtskompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100666"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="f8b34-104">Schreiben von abwärts kompatiblen Clients und Servern</span><span class="sxs-lookup"><span data-stu-id="f8b34-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="f8b34-105">Theoretisch hilft das Versions Schema von RPC dabei, eine Fehlkommunikation zwischen geänderten Servern und Clients und ihren bereitgestellten Gegenstücken zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f8b34-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="f8b34-106">In der Praxis müssen Entwickler jedoch häufig Änderungen an vorhandenen Schnittstellen vornehmen, ohne die Version zu ändern, da vorherige Clients und Server in der Lage sein müssen, mit neuen zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f8b34-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="f8b34-107">Dies ist ein größeres Problem für Standard-RPC als für com. Abfragen stellen eine natürliche Möglichkeit dar, in com nach unterstützten Schnittstellen zu suchen, während die RPC-Ausnahmebehandlung für eine äquivalente Abdeckung verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f8b34-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="f8b34-108">In diesem Abschnitt werden die besten RPC-Programmiermethoden zum Behandeln dieser Situationen erläutert.</span><span class="sxs-lookup"><span data-stu-id="f8b34-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="f8b34-109">Dieser Abschnitt ist in die folgenden Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="f8b34-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="f8b34-110">Die versionierungstheorie für RPC und com</span><span class="sxs-lookup"><span data-stu-id="f8b34-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="f8b34-111">Ändern von Schnittstellen in abwärts kompatibler Weise</span><span class="sxs-lookup"><span data-stu-id="f8b34-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="f8b34-112">Beispiele für inkompatible Änderungen</span><span class="sxs-lookup"><span data-stu-id="f8b34-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




