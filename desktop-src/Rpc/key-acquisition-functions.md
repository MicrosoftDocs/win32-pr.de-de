---
title: Schlüssel Erwerbs Funktionen
description: Standardmäßig stellt der SSP Verschlüsselungsschlüssel für Serverprogramme bereit, von denen diese angefordert werden. Jeder SSP implementiert sein eigenes System zum Erstellen von Schlüsseln. Das Format der vom SSP generierten Schlüssel ist spezifisch für den SSP.
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8c8e8cfb2f3b4f8f241b2401878576cbe7f90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856747"
---
# <a name="key-acquisition-functions"></a><span data-ttu-id="bbd70-105">Schlüssel Erwerbs Funktionen</span><span class="sxs-lookup"><span data-stu-id="bbd70-105">Key Acquisition Functions</span></span>

<span data-ttu-id="bbd70-106">Standardmäßig stellt der SSP Verschlüsselungsschlüssel für Serverprogramme bereit, von denen diese angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="bbd70-106">By default, the SSP supplies encryption keys to server programs that request them.</span></span> <span data-ttu-id="bbd70-107">Jeder SSP implementiert sein eigenes System zum Erstellen von Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="bbd70-107">Each SSP implements its own system of generating keys.</span></span> <span data-ttu-id="bbd70-108">Das Format der vom SSP generierten Schlüssel ist spezifisch für den SSP.</span><span class="sxs-lookup"><span data-stu-id="bbd70-108">The format of the keys that the SSP generates are specific to the SSP.</span></span>

<span data-ttu-id="bbd70-109">RPC bietet Ihnen die Möglichkeit, die Standardmethode zum Erstellen von Verschlüsselungsschlüsseln zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="bbd70-109">RPC provides you with the ability to override the default method of generating encryption keys.</span></span> <span data-ttu-id="bbd70-110">Die Anwendung kann die [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion aufrufen und ihr einen Zeiger auf eine Schlüssel Erwerbs Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="bbd70-110">Your application can call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function and pass it a pointer to a key acquisition function.</span></span> <span data-ttu-id="bbd70-111">Sie können die Schlüssel Erwerbs Funktion so schreiben, dass Sie mit jeder gewählten Methode Schlüssel generiert.</span><span class="sxs-lookup"><span data-stu-id="bbd70-111">You can write the key acquisition function so that it generates keys using any method you choose.</span></span> <span data-ttu-id="bbd70-112">Der an das Serverprogramm übergebenen Schlüssel muss jedoch dem Format entsprechen, das für den SSP erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="bbd70-112">However, the key it passes to the server program must match the format that the SSP requires.</span></span>

> [!Note]  
> <span data-ttu-id="bbd70-113">Die meisten Anwendungen müssen keine Schlüssel Erwerbs Funktionen verwenden und können einfach **null** für alle Parameter angeben, bei denen eine Schlüssel Erwerbs Funktion angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="bbd70-113">Most applications do not need to use key acquisition functions, and can simply supply **NULL** to all parameters where a key acquisition function is requested.</span></span>

 

 

 




