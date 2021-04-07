---
title: ADSI-LDAP-Anbieter
description: Der ADSI LDAP-Anbieter implementiert eine Reihe von ADSI-Objekten, die verschiedene ADSI-Schnittstellen unterstützen. Um auf den LDAP-Anbieter zuzugreifen, binden Sie mithilfe des LDAP-ADsPath an eines der ADSI LDAP-Objekte.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- ADSI-LDAP-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855360"
---
# <a name="adsi-ldap-provider"></a><span data-ttu-id="0cfe9-105">ADSI-LDAP-Anbieter</span><span class="sxs-lookup"><span data-stu-id="0cfe9-105">ADSI LDAP Provider</span></span>

<span data-ttu-id="0cfe9-106">Der ADSI LDAP-Anbieter implementiert eine Reihe von ADSI-Objekten, die verschiedene ADSI-Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0cfe9-106">The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces.</span></span> <span data-ttu-id="0cfe9-107">Um auf den LDAP-Anbieter zuzugreifen, binden Sie mithilfe des LDAP-ADsPath an eines der ADSI LDAP-Objekte.</span><span class="sxs-lookup"><span data-stu-id="0cfe9-107">To access the LDAP provider, bind to any of the ADSI LDAP objects, using the LDAP ADsPath.</span></span>

<span data-ttu-id="0cfe9-108">Adsldp.dll, Adsldpc.dll, Adsmsext.dll und Activeds.dll müssen auf dem Client Computer installiert sein, um mit dem Anbieter zusammenarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="0cfe9-108">You must have Adsldp.dll, Adsldpc.dll, Adsmsext.dll, and Activeds.dll installed on your client computer to work with the provider.</span></span>

> [!Note]  
> <span data-ttu-id="0cfe9-109">Der standardmäßige ADSI LDAP-Anbieter kann nicht als vollständig Thread sicher angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="0cfe9-109">The default ADSI LDAP provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="0cfe9-110">Writer von Multithreadanwendungen sollten den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungs Objekten, wie z. b. Semaphore, Mutexen, kritischen Abschnitten usw., ordnungsgemäß koordinieren.</span><span class="sxs-lookup"><span data-stu-id="0cfe9-110">Writers of multithreaded applications should properly coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




