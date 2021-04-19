---
description: Zertifikate können über einen beliebigen Transportmechanismus angefordert und verteilt werden.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Transport Unabhängigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348472"
---
# <a name="transport-independence"></a><span data-ttu-id="a3cfb-103">Transport Unabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="a3cfb-103">Transport Independence</span></span>

<span data-ttu-id="a3cfb-104">Zertifikate können über einen beliebigen Transportmechanismus angefordert und verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="a3cfb-105">Zertifikat Dienste akzeptieren [*Zertifikat Anforderungen*](../secgloss/c-gly.md) von einem Antragsteller über HTTP, DCOM, RPC, eine Datenträger Datei oder einen benutzerdefinierten Transport.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="a3cfb-106">Zertifikat Dienste stellen Zertifikate an den Antragsteller über HTTP, DCOM, RPC, Datenträger Datei oder benutzerdefinierten Transport.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="a3cfb-107">Transporte werden von Vermittler Anwendungen und Beendigungs Modul-DLLs unterstützt, die in der Regel in C/C++ geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="a3cfb-108">Die zwischengeschalteten Anwendungen und Exit-Module isolieren Zertifikat Dienstfunktionen von der Kommunikation mit einem bestimmten Transport.</span><span class="sxs-lookup"><span data-stu-id="a3cfb-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
