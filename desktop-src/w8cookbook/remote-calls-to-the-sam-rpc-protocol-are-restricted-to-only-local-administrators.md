---
title: Remote Aufrufe des Sam RPC-Protokolls sind nur auf lokale Administratoren beschränkt.
description: Das Sam-RPC-Protokoll wird eingeschränkt. Dies bedeutet, dass nur Mitglieder der lokalen Administrator Gruppe Remote Aufrufe für Methoden in diesem Protokoll durchführen können. Active Directory Domänen Controller Verhalten ist nicht betroffen.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100818"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a><span data-ttu-id="2bc95-105">Remote Aufrufe des Sam RPC-Protokolls sind nur auf lokale Administratoren beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2bc95-105">Remote calls to the SAM RPC protocol are restricted to only local administrators</span></span>

<span data-ttu-id="2bc95-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2bc95-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2bc95-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2bc95-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2bc95-108">Das Sam-RPC-Protokoll wird eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="2bc95-108">The SAM RPC protocol is being restricted.</span></span> <span data-ttu-id="2bc95-109">Dies bedeutet, dass nur Mitglieder der lokalen Administrator Gruppe Remote Aufrufe für Methoden in diesem Protokoll durchführen können.</span><span class="sxs-lookup"><span data-stu-id="2bc95-109">This means that only members of the local Administrator group can make remote calls against methods in this protocol.</span></span> <span data-ttu-id="2bc95-110">Active Directory Domänen Controller Verhalten ist nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="2bc95-110">Active Directory domain controller behavior is unaffected.</span></span>

## <a name="mitigations"></a><span data-ttu-id="2bc95-111">Gegenmaßnahmen</span><span class="sxs-lookup"><span data-stu-id="2bc95-111">Mitigations</span></span>

<span data-ttu-id="2bc95-112">Stellen Sie sicher, dass die richtigen Benutzer auf dem PC als Administratoren festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="2bc95-112">Ensure that the right users are set as administrators on the PC.</span></span> <span data-ttu-id="2bc95-113">Die für die Zugriffs Überprüfung verwendete ACL ist über die Gruppenrichtlinie konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="2bc95-113">The ACL used for the access check is configurable via group policy.</span></span>

 

 




