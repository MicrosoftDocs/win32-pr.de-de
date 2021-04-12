---
title: Konfigurations Persistenz
description: Konfigurations Persistenz
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media-Format-SDK, Persistenz
- Windows Media-Format-SDK, Konfigurations Persistenz
- Advanced Systems Format (ASF), Persistenz
- ASF (Advanced Systems Format), Persistenz
- Advanced Systems Format (ASF), Konfigurations Persistenz
- ASF (Advanced Systems Format), Konfigurations Persistenz
- Konfigurations Persistenz
- Dauerhaftigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389926"
---
# <a name="configuration-persistence"></a><span data-ttu-id="955b2-111">Konfigurations Persistenz</span><span class="sxs-lookup"><span data-stu-id="955b2-111">Configuration Persistence</span></span>

<span data-ttu-id="955b2-112">Keine der in dieser Dokumentation beschriebenen Schreib aktivierten Eigenschaften wird vom Windows Media SDK gespeichert.</span><span class="sxs-lookup"><span data-stu-id="955b2-112">None of the write-enabled properties described in this documentation are saved by the Windows Media SDK.</span></span> <span data-ttu-id="955b2-113">Jede Anwendung, die das SDK verwendet, muss bei Bedarf eigene persistenzprozeduren bereitstellen und die entsprechende Set-Methode für jede Instanz des SDK aufrufen.</span><span class="sxs-lookup"><span data-stu-id="955b2-113">Each application that uses the SDK must provide its own persistence procedures as needed and invoke the appropriate set method upon each instance of the SDK.</span></span> <span data-ttu-id="955b2-114">Auf diese Weise wirken sich Konfigurationsänderungen, die von einer Anwendung vorgenommen werden, nicht auf eine andere Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="955b2-114">In this way, configuration changes made by one application do not affect another application.</span></span> <span data-ttu-id="955b2-115">Beispielsweise wirkt sich das Ändern der Pufferzeit in einem Player nicht auf einen anderen Player aus.</span><span class="sxs-lookup"><span data-stu-id="955b2-115">For example, changing the buffering time in one player does not affect another player.</span></span>

<span data-ttu-id="955b2-116">Die einzige Ausnahme von dieser Regel sind die Informationen zu den Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="955b2-116">The one exception to this rule is for the credentials information.</span></span> <span data-ttu-id="955b2-117">Wenn die Anwendung anzeigt, dass die Benutzer-ID und die Kenn Wort Informationen in der Rückgabe vom **acquirecredensted** -Befehl beibehalten werden müssen, speichert das SDK diese Informationen.</span><span class="sxs-lookup"><span data-stu-id="955b2-117">If the application indicates, in its return from the **AcquireCredentials** call, that the user ID and password information must be persisted, the SDK saves this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="955b2-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="955b2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="955b2-119">**Implementieren von Netzwerkfunktionen**</span><span class="sxs-lookup"><span data-stu-id="955b2-119">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="955b2-120">**Iwmkredentialcallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="955b2-120">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




