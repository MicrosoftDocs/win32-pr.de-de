---
title: Konfigurieren von Skript Datenströmen
description: Konfigurieren von Skript Datenströmen
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- Streams, Konfigurieren von Skript Datenströmen
- Codecs, Konfigurieren von Skript Datenströmen
- Skripterstellung, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036835"
---
# <a name="configuring-script-streams"></a><span data-ttu-id="c4923-106">Konfigurieren von Skript Datenströmen</span><span class="sxs-lookup"><span data-stu-id="c4923-106">Configuring Script Streams</span></span>

<span data-ttu-id="c4923-107">Wie bei allen beliebigen Streamtypen müssen für Skript Datenströme eine Bitrate und ein Puffer Fenster definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4923-107">Like all arbitrary stream types, script streams need to have a bit rate and buffer window defined for them.</span></span> <span data-ttu-id="c4923-108">Der Haupt Medientyp in der [**WM \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur muss auf wmmediatype-Skript festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="c4923-108">The major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure must be set to WMMEDIATYPE\_Script.</span></span>

<span data-ttu-id="c4923-109">Für Skript Datenströme muss der **Format Type** -Member des **WM- \_ Medien \_ Typs** auf wmformat-Skript festgelegt sein \_ , was darauf hinweist, dass der **pbformat** -Member auf eine [**wmscriptformat**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) -Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="c4923-109">Script streams need to have the **formattype** member of **WM\_MEDIA\_TYPE** set to WMFORMAT\_Script, which indicates that the **pbFormat** member points to a [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) structure.</span></span>

<span data-ttu-id="c4923-110">Es gibt nur einen unterstützten Skripttyp, wmscripttype \_ twostrings.</span><span class="sxs-lookup"><span data-stu-id="c4923-110">There is only one supported script type, WMSCRIPTTYPE\_TwoStrings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4923-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4923-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4923-112">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="c4923-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="c4923-113">**Konfigurieren beliebiger Streamtypen**</span><span class="sxs-lookup"><span data-stu-id="c4923-113">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="c4923-114">**Skriptbefehle**</span><span class="sxs-lookup"><span data-stu-id="c4923-114">**Script Commands**</span></span>](script-commands.md)
</dt> </dl>

 

 




