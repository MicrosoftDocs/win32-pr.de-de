---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Windows Media Player Online Stores, Background Intelligent Transfer Service (Bits)
- Online Stores, Background Intelligent Transfer Service (Bits)
- Typ 2 Online Stores, Background Intelligent Transfer Service (Bits)
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Bits (Background Intelligent Transfer Service)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315471"
---
# <a name="bits"></a><span data-ttu-id="cd133-108">BITS</span><span class="sxs-lookup"><span data-stu-id="cd133-108">BITS</span></span>

<span data-ttu-id="cd133-109">Der [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) ist eine Funktion des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="cd133-109">The [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) is a feature of the Windows operating system.</span></span> <span data-ttu-id="cd133-110">Bits überträgt Dateien (Downloads oder Uploads) zwischen einem Client und einem Server und stellt Statusinformationen zu den Übertragungen bereit.</span><span class="sxs-lookup"><span data-stu-id="cd133-110">BITS transfers files (downloads or uploads) between a client and server, and provides progress information related to the transfers.</span></span> <span data-ttu-id="cd133-111">Wenn Sie Dateien mithilfe von C++-Code übertragen möchten, ist Bits die richtige zu verwendende Technologie.</span><span class="sxs-lookup"><span data-stu-id="cd133-111">If you want to transfer files using C++ code, BITS is the correct technology to use.</span></span> <span data-ttu-id="cd133-112">Wenn Sie Dateien mithilfe von JScript-Code auf Ihrer Online Store-Webseite übertragen möchten, verwenden Sie stattdessen den Download-Manager.</span><span class="sxs-lookup"><span data-stu-id="cd133-112">If you want to transfer files using JScript code in your online store webpage, use the Download Manager instead.</span></span>

<span data-ttu-id="cd133-113">Da der Windows Media Player Download-Manager Bits verwendet, können Sie Schritte ausführen, um ihre Bits-Kopieraufträge so zu konfigurieren, dass Windows Media Player die Aufträge für Sie verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cd133-113">Because the Windows Media Player Download Manager uses BITS, you can take steps to configure your BITS copy jobs in such a way that Windows Media Player manages the jobs for you.</span></span> <span data-ttu-id="cd133-114">Zu diesem Zweck müssen Sie der im Abschnitt [Windows Media Player Bits-Auftrags Konvention](windows-media-player-bits-job-convention.md) beschriebenen Konvention folgen, wenn Sie Ihre Aufträge der Bits-Übertragungs Warteschlange hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd133-114">To do this, you must follow the convention described in the [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md) section when adding your jobs to the BITS transfer queue.</span></span> <span data-ttu-id="cd133-115">In diesem Abschnitt wird auch ein Mechanismus zum Abrufen von Informationen zu ihren Bits-Aufträgen von Ihrer Online Store-Webseite beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd133-115">This section also describes a mechanism for retrieving information about your BITS jobs from your online stores webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd133-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd133-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd133-117">**Verwenden des Download-Managers**</span><span class="sxs-lookup"><span data-stu-id="cd133-117">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> <dt>

[<span data-ttu-id="cd133-118">**Informationen zu Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="cd133-118">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> </dl>

 

 