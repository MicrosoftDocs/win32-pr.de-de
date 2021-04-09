---
title: DRM_Rights
description: Die DRM- \_ Rechte Eigenschaft gibt die Rechte an, die die Anwendung beim nächsten Versuch benötigt, eine geschützte Datei zu öffnen.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038536"
---
# <a name="drm_rights"></a><span data-ttu-id="c54f2-104">DRM- \_ Rechte</span><span class="sxs-lookup"><span data-stu-id="c54f2-104">DRM\_Rights</span></span>

<span data-ttu-id="c54f2-105">Die **DRM- \_ Rechte** Eigenschaft gibt die Rechte an, die die Anwendung beim nächsten Versuch benötigt, eine geschützte Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c54f2-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c54f2-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="c54f2-106">Global Constant</span></span>

<span data-ttu-id="c54f2-107">g \_ wszwmdrm- \_ Rechte</span><span class="sxs-lookup"><span data-stu-id="c54f2-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="c54f2-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c54f2-108">Data Type</span></span>

<span data-ttu-id="c54f2-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c54f2-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c54f2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c54f2-110">Remarks</span></span>

<span data-ttu-id="c54f2-111">Dabei handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) abgerufen und entweder mithilfe von [**iwmdrmreader:: setdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) oder [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c54f2-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="c54f2-112">In der folgenden Tabelle sind die unterstützten Rechte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c54f2-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="c54f2-113">Rechts</span><span class="sxs-lookup"><span data-stu-id="c54f2-113">Right</span></span>                                           | <span data-ttu-id="c54f2-114">Zeichenfolgenliteral</span><span class="sxs-lookup"><span data-stu-id="c54f2-114">String literal</span></span>      | <span data-ttu-id="c54f2-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c54f2-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54f2-116">g \_ wszwmdrm- \_ Rechte \_ Sicherung</span><span class="sxs-lookup"><span data-stu-id="c54f2-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="c54f2-117">„Backup“</span><span class="sxs-lookup"><span data-stu-id="c54f2-117">"Backup"</span></span>            | <span data-ttu-id="c54f2-118">Recht zum Sichern der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="c54f2-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="c54f2-119">g \_ wszwmdrm \_ right \_ COLLABORATIVE \_ Play</span><span class="sxs-lookup"><span data-stu-id="c54f2-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="c54f2-120">"Kollaborativeplay"</span><span class="sxs-lookup"><span data-stu-id="c54f2-120">"CollaborativePlay"</span></span> | <span data-ttu-id="c54f2-121">Das Recht, die Datei im Rahmen einer Zusammenarbeits Wiedergabe Wiedergabe wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="c54f2-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="c54f2-122">g \_ wszwmdrm- \_ Rechte \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="c54f2-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="c54f2-123">"Kopieren"</span><span class="sxs-lookup"><span data-stu-id="c54f2-123">"Copy"</span></span>              | <span data-ttu-id="c54f2-124">Recht zum Kopieren der Datei auf ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="c54f2-124">Right to copy the file to a device.</span></span> <span data-ttu-id="c54f2-125">Dieses Recht ersetzt die älteren Kopierrechte (g \_ wszwmdrm \_ right \_ Copy \_ to \_ CD, g \_ wszwmdrm \_ right \_ Copy \_ to \_ Non \_ SDMI \_ Device und g \_ wszwmdrm right Copy \_ \_ \_ to \_ SDMI \_ Device).</span><span class="sxs-lookup"><span data-stu-id="c54f2-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="c54f2-126">g \_ wszwmdrm \_ - \_ Rechte \_ auf \_ CD kopieren</span><span class="sxs-lookup"><span data-stu-id="c54f2-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="c54f2-127">"Print. Redbook"</span><span class="sxs-lookup"><span data-stu-id="c54f2-127">"Print.redbook"</span></span>     | <span data-ttu-id="c54f2-128">Rechts zum Kopieren der Datei auf eine CD (rotes Buchformat). In Windows Media DRM 10 wird dieses Recht durch g \_ wszwmdrm \_ right Copy ersetzt \_ .</span><span class="sxs-lookup"><span data-stu-id="c54f2-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="c54f2-129">g \_ wszwmdrm- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät kopieren</span><span class="sxs-lookup"><span data-stu-id="c54f2-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="c54f2-130">"Transfer. nonsdmi"</span><span class="sxs-lookup"><span data-stu-id="c54f2-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="c54f2-131">Recht zum Kopieren der Datei auf ein nicht-SDMI-Gerät. In Windows Media DRM 10 wird dieses Recht durch g \_ wszwmdrm \_ right Copy ersetzt \_ .</span><span class="sxs-lookup"><span data-stu-id="c54f2-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="c54f2-132">g \_ wszwmdrm- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren</span><span class="sxs-lookup"><span data-stu-id="c54f2-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="c54f2-133">"Transfer. SDMI"</span><span class="sxs-lookup"><span data-stu-id="c54f2-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="c54f2-134">Recht zum Kopieren der Datei auf ein SDMI-kompatibles Gerät. In Windows Media DRM 10 wird dieses Recht durch g \_ wszwmdrm \_ right Copy ersetzt \_ .</span><span class="sxs-lookup"><span data-stu-id="c54f2-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="c54f2-135">g \_ wszwmdrm \_ right- \_ Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="c54f2-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="c54f2-136">Theater</span><span class="sxs-lookup"><span data-stu-id="c54f2-136">"Play"</span></span>              | <span data-ttu-id="c54f2-137">Das Recht, die Mediendatei wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="c54f2-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="c54f2-138">Diese Eigenschaft enthält eine Zeichenfolge mit breit Zeichen von mindestens einer durch Semikolons getrennten Berechtigung, z. b.: L "Wiedergabe; Skopie Kollaborativeplay ".</span><span class="sxs-lookup"><span data-stu-id="c54f2-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="c54f2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c54f2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c54f2-140">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="c54f2-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





