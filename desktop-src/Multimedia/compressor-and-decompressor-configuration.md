---
title: Konfiguration des Kompressors und dekompressors
description: Konfiguration des Kompressors und dekompressors
ms.assetid: 677241d2-3ddd-423a-a1e7-b5fa3ce0a4eb
keywords:
- Videokomprimierungs-Manager (VCM), Konfigurieren von Kompressoren
- VCM (Videokomprimierungs-Manager), Konfigurieren von Kompressoren
- ICM_CONFIGURE Meldung
- Icqueryconfigure-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38fbbeb852d09296e5be7929738c9d4d71f118e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947642"
---
# <a name="compressor-and-decompressor-configuration"></a><span data-ttu-id="d50ba-107">Konfiguration des Kompressors und dekompressors</span><span class="sxs-lookup"><span data-stu-id="d50ba-107">Compressor and Decompressor Configuration</span></span>

<span data-ttu-id="d50ba-108">Die Anwendung kann den Kompressor oder die Debug-Konfiguration automatisch konfigurieren oder die Konfiguration durch den Benutzer zulassen.</span><span class="sxs-lookup"><span data-stu-id="d50ba-108">Your application can configure the compressor or decompressor automatically, or it can allow the user to configure them.</span></span> <span data-ttu-id="d50ba-109">Wenn dies praktikabel ist, gestatten Sie dem Benutzer die Konfiguration des Kompressors oder der Debug-Konfiguration. Dies gibt Ihnen die Möglichkeit, alle Optionen für den-Kompressor oder-Dekompressor zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="d50ba-109">If it is practical, allow the user to configure the compressor or decompressor; this frees you from considering all the options for the compressor or decompressor.</span></span>

<span data-ttu-id="d50ba-110">Der Benutzer kann den Kompressor oder Dekompressor mithilfe eines Konfigurations Dialogfelds konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d50ba-110">The user can configure the compressor or decompressor by using a configuration dialog box.</span></span> <span data-ttu-id="d50ba-111">Sie können die [**ICM \_ configure**](icm-configure.md) -Nachricht an VCM senden (oder das [**icqueryconfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) -Makro verwenden), um zu bestimmen, ob ein Kompressor oder Dekompressor ein Konfigurations Dialogfeld anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="d50ba-111">You can send the [**ICM\_CONFIGURE**](icm-configure.md) message to VCM (or use the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro) to determine if a compressor or decompressor can display a configuration dialog box.</span></span> <span data-ttu-id="d50ba-112">Wenn dies der Fall ist, senden Sie die ICM- \_ Konfigurations Nachricht (oder verwenden Sie das [**icconfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) -Makro), um Sie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d50ba-112">If so, send the ICM\_CONFIGURE message (or use the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro) to display it.</span></span>

<span data-ttu-id="d50ba-113">Die Anwendung kann die [**ICM \_ GetState**](icm-getstate.md) -und [**ICM \_ SetState**](icm-setstate.md) -Meldungen senden (oder die Makros [**icgetstatesize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**icgetstate**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)und [**icsetstate**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) verwenden), um den Status für einen Kompressor oder Dekompressor zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d50ba-113">Your application can send the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages (or use the [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize), [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate), and [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macros) to get and set the status for a compressor or decompressor.</span></span> <span data-ttu-id="d50ba-114">Wenn die Anwendung den Status erstellt oder ändert, muss Sie vor dem Wiederherstellen des Status das Layout der Daten des Kompressors oder dekompressors abrufen.</span><span class="sxs-lookup"><span data-stu-id="d50ba-114">If your application creates or modifies the status, it must obtain the layout of the compressor or decompressor data before restoring its status.</span></span> <span data-ttu-id="d50ba-115">Wenn Ihre Anwendung den Status von einem Kompressor oder Dekompressor erhält und Sie zum Wiederherstellen des Status in einer nachfolgenden Sitzung verwendet, muss sichergestellt werden, dass nur die Statusinformationen wieder hergestellt werden, die vom verwendeten Kompressor oder Dekompressor abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="d50ba-115">Alternatively, if your application obtains the status from a compressor or decompressor and uses it to restore the status in a subsequent session, it must ensure that it restores only status information obtained from the compressor or decompressor it is currently using.</span></span>

 

 




