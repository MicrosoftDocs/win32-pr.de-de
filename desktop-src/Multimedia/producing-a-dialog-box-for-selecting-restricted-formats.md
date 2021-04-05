---
title: Erstellen eines Dialog Felds zum Auswählen von eingeschränkten Formaten
description: Erstellen eines Dialog Felds zum Auswählen von eingeschränkten Formaten
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen von eingeschränkten Formaten
- ACM (Audiokomprimierungs-Manager), auswählen von eingeschränkten Formaten
- ACM-Beispiele, auswählen von eingeschränkten Formaten
- Auswählen von eingeschränkten Formaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800945f4003c0fbe47d7916e0a1bf707745ff6d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037095"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a><span data-ttu-id="80e5b-112">Erstellen eines Dialog Felds zum Auswählen von eingeschränkten Formaten</span><span class="sxs-lookup"><span data-stu-id="80e5b-112">Producing a Dialog Box for Selecting Restricted Formats</span></span>

<span data-ttu-id="80e5b-113">Möglicherweise möchten Sie das Dialogfeld verwenden, das von der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion erstellt wurde, aber beschränken oder Steuern Sie die Formate im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="80e5b-113">You might want to use the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, but limit or control the formats in the dialog box.</span></span> <span data-ttu-id="80e5b-114">Hierfür können Sie das Flag "acmformatchoose \_ stylef \_ ENABLEHOOK" verwenden, um die Dialogfeld Prozedur zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="80e5b-114">You can do this by using the ACMFORMATCHOOSE\_STYLEF\_ENABLEHOOK flag to hook the dialog procedure.</span></span> <span data-ttu-id="80e5b-115">Die Anwendung kann dann die Formate filtern, indem Sie in der Nachrichten Prozedur für das Dialogfeld auf die Meldung [**mm \_ ACM \_ formatchoose**](mm-acm-formatchoose.md) antwortet.</span><span class="sxs-lookup"><span data-stu-id="80e5b-115">The application can then filter the formats by responding to the [**MM\_ACM\_FORMATCHOOSE**](mm-acm-formatchoose.md) message in the message procedure for the dialog box.</span></span>

 

 




