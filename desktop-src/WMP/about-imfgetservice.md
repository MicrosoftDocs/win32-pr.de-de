---
title: Informationen über "IMF GetService"
description: Informationen über "IMF GetService"
ms.assetid: c71b1362-a596-42e5-b894-f8a3c0e70140
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, IMF-Service-Schnittstelle
- Plug-ins, IMF GetService-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, IMF GetService-Schnittstelle
- DSP-Plug-ins, IMF GetService-Schnittstelle
- IMF GetService-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235b616afe48db9ae772da1f1d74c4f7de1a74a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309375"
---
# <a name="about-imfgetservice"></a><span data-ttu-id="7eb3f-113">Informationen über "IMF GetService"</span><span class="sxs-lookup"><span data-stu-id="7eb3f-113">About IMFGetService</span></span>

<span data-ttu-id="7eb3f-114">Die **imsgetservice** -Schnittstelle ist eine der Schnittstellen, die von einem DSP-Plug-in mit zwei Modi implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-114">The **IMFGetService** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="7eb3f-115">Es verfügt nur über eine Methode, **GetService**.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-115">It has only one method, **GetService**.</span></span> <span data-ttu-id="7eb3f-116">Ein DSP-Plug-in implementiert die **GetService** -Methode, sodass Clients Zeiger auf die vom Plug-in unterstützten Schnittstellen abrufen können, wenn das Plug-in System eigen in der Media Foundation Pipeline ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-116">A DSP plug-in implements the **GetService** method so that clients can obtain pointers to the interfaces supported by the plug-in when the plug-in is running natively in the Media Foundation pipeline.</span></span>

 

 




