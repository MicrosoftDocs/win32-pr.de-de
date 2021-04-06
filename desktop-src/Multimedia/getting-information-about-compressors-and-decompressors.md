---
title: Informationen zu Kompressoren und Dekompressoren erhalten
description: Informationen zu Kompressoren und Dekompressoren erhalten
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- Videokomprimierungs-Manager (VCM), Informationen zu Kompressoren erhalten
- VCM (Videokomprimierungs-Manager), Informationen zu Kompressoren erhalten
- Icgetinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947761"
---
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="4e9ea-106">Informationen zu Kompressoren und Dekompressoren erhalten</span><span class="sxs-lookup"><span data-stu-id="4e9ea-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="4e9ea-107">Um allgemeine Informationen zu einem Kompressor oder Dekompressor zu erhalten, kann die Anwendung die [**icgetinfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e9ea-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="4e9ea-108">Diese Funktion füllt eine [**icinfo**](/windows/desktop/api/Vfw/ns-vfw-icinfo) -Struktur mit Informationen über den Kompressor oder Dekompressor.</span><span class="sxs-lookup"><span data-stu-id="4e9ea-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="4e9ea-109">Die Anwendung muss den Arbeitsspeicher für die **icinfo** -Struktur zuordnen und in **icgetinfo** einen Zeiger darauf übergeben.</span><span class="sxs-lookup"><span data-stu-id="4e9ea-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="4e9ea-110">Wenn Ihre Anwendung nicht nach einem bestimmten Kompressor oder Dekompressor sucht, stellen die Flags in der **icinfo** -Struktur die nützlichsten Informationen zu den Funktionen eines Kompressors oder dekompressors bereit.</span><span class="sxs-lookup"><span data-stu-id="4e9ea-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="4e9ea-111">Um die standardmäßige Keyframerate und den Standardwert für die Qualität eines Kompressors oder dekompressors zu erhalten, kann Ihre Anwendung die [**ICM \_ getdefaultkeyframerate**](icm-getdefaultkeyframerate.md) -und [**ICM \_ getdefaultquality**](icm-getdefaultquality.md) -Meldungen senden (oder die Makros [**icgetdefaultkeyframerate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) und [**icgetdefaultquality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) verwenden).</span><span class="sxs-lookup"><span data-stu-id="4e9ea-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="4e9ea-112">Um das beste Anzeige Format eines Kompressors oder dekompressors zu ermitteln, kann die Anwendung die [**icgetdisplayformat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e9ea-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="4e9ea-113">Um zu ermitteln, ob ein "Info"-Dialogfeld von einem Kompressor oder Dekompressor angezeigt werden kann, senden Sie den [**ICM \_ über**](icm-about.md) die Nachricht (oder verwenden Sie das [**icqueryabout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) -Makro).</span><span class="sxs-lookup"><span data-stu-id="4e9ea-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="4e9ea-114">Sie können auch das Dialogfeld Info eines Kompressors oder dekompressors anzeigen, indem Sie den ICM \_ über eine Nachricht senden und den Wert des *wParam* -Parameters (oder mithilfe des [**icabout**](/windows/desktop/api/Vfw/nf-vfw-icabout) -Makros) ändern.</span><span class="sxs-lookup"><span data-stu-id="4e9ea-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




