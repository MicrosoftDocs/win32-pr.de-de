---
title: DRM_BaseLicenseAcqURL
description: Das DRM- \_ baselicenseacqurl-Attribut enthält eine partielle Basis-URL, zu der eine Player Anwendung navigieren muss, um eine Lizenz für den Inhalt zu erhalten.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101246"
---
# <a name="drm_baselicenseacqurl"></a><span data-ttu-id="b75db-104">DRM- \_ baselicenabacqurl</span><span class="sxs-lookup"><span data-stu-id="b75db-104">DRM\_BaseLicenseAcqURL</span></span>

<span data-ttu-id="b75db-105">Das **DRM- \_ baselicenseacqurl** -Attribut enthält eine partielle Basis-URL, zu der eine Player Anwendung navigieren muss, um eine Lizenz für den Inhalt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b75db-105">The **DRM\_BaseLicenseAcqURL** attribute contains a partial, base URL to which a player application must navigate to obtain a license for the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b75db-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="b75db-106">Global Constant</span></span>

<span data-ttu-id="b75db-107">g \_ wszwmdrm \_ baselicensetup-URL</span><span class="sxs-lookup"><span data-stu-id="b75db-107">g\_wszWMDRM\_BaseLicenseAcqURL</span></span>

## <a name="data-type"></a><span data-ttu-id="b75db-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b75db-108">Data Type</span></span>

<span data-ttu-id="b75db-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b75db-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="b75db-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b75db-110">Remarks</span></span>

<span data-ttu-id="b75db-111">Dies ist eine optionale Eigenschaft mit Lese-/Schreibzugriff, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)festgelegt und abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b75db-111">This is an optional read-write property that is set and retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="b75db-112">Er wird bereitgestellt, damit die Lizenz Verteilungssysteme relative Pfade in den Eigenschaften für die Lizenz Erwerbs-URL verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b75db-112">It is provided to enable license distribution systems to use relative paths in the license acquisition URL properties.</span></span>

<span data-ttu-id="b75db-113">Nachdem Sie diese Eigenschaft festgelegt haben, verfügen alle Teillizenz Erwerbs-URLs in Inhalts Headern über die Basis-URL, die der Vorderseite der partiellen URL hinzugefügt wird, um eine vollständige URL für die Player Anwendung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="b75db-113">After setting this property, all partial license acquisition URLs in content headers will have the base URL added to the front of the partial URL to form a full URL for the player application to navigate to.</span></span> <span data-ttu-id="b75db-114">Das Aufrufen von **iwmdrmreader:: getdrmproperty** für **DRM \_ baselicenseacqurl** funktioniert nur in derselben Sitzung, in der es festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="b75db-114">Calling **IWMDRMReader::GetDRMProperty** for **DRM\_BaseLicenseAcqURL** will only work only in the same session as it was set.</span></span> <span data-ttu-id="b75db-115">Die-Eigenschaft wird nicht im Content-Header gespeichert. Es ist dynamisch, und nur die relative URL werden im Inhalt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b75db-115">The property is not stored in the content header; it is dynamic, and only the relative URL is stored in the content.</span></span>

## <a name="see-also"></a><span data-ttu-id="b75db-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b75db-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75db-117">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="b75db-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




