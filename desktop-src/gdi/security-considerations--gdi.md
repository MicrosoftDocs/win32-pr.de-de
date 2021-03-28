---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit GDI. Dieses Thema bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie Sie stattdessen als Ausgangspunkt und Verweis für diesen Technologiebereich.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Sicherheitsüberlegungen: GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960195"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="e43b3-105">Sicherheitsüberlegungen: GDI</span><span class="sxs-lookup"><span data-stu-id="e43b3-105">Security Considerations: GDI</span></span>

<span data-ttu-id="e43b3-106">Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit GDI.</span><span class="sxs-lookup"><span data-stu-id="e43b3-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="e43b3-107">Dieses Thema bietet Ihnen nicht alles, was Sie über Sicherheitsprobleme wissen müssen.</span><span class="sxs-lookup"><span data-stu-id="e43b3-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="e43b3-108">Verwenden Sie Sie stattdessen als Ausgangspunkt und Verweis für diesen Technologiebereich.</span><span class="sxs-lookup"><span data-stu-id="e43b3-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="e43b3-109">GDI weist in der Regel nur wenige Sicherheitsaspekte auf, da Sie anstelle von Eingaben angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e43b3-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="e43b3-110">Im folgenden finden Sie jedoch einige Punkte, die Sie berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="e43b3-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="e43b3-111">Bitmaps, Metadateien und Schriftarten sind komplexe Strukturen, die beschädigt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="e43b3-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="e43b3-112">Es empfiehlt sich, zu versuchen, sicherzustellen, dass diese Elemente nicht beschädigt sind und aus einer vertrauenswürdigen Quelle stammen.</span><span class="sxs-lookup"><span data-stu-id="e43b3-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="e43b3-113">Eine Anwendung kann die Sicherheits Beschreibung für einige der Druck-und spoolingapis angeben.</span><span class="sxs-lookup"><span data-stu-id="e43b3-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="e43b3-114">Beim Festlegen der Sicherheits Beschreibung sollten Sie sorgfältig vorgehen.</span><span class="sxs-lookup"><span data-stu-id="e43b3-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e43b3-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e43b3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e43b3-116">Microsoft Security Central</span><span class="sxs-lookup"><span data-stu-id="e43b3-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="e43b3-117">Security Developer Center</span><span class="sxs-lookup"><span data-stu-id="e43b3-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="e43b3-118">Sicherheits-TechCenter</span><span class="sxs-lookup"><span data-stu-id="e43b3-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



