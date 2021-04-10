---
title: DRM_KeyID
description: Das DRM- \_ keyid-Attribut enthält den Schlüssel Bezeichner.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038588"
---
# <a name="drm_keyid"></a><span data-ttu-id="a2875-104">DRM- \_ Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="a2875-104">DRM\_KeyID</span></span>

<span data-ttu-id="a2875-105">Das **DRM- \_ keyid** -Attribut enthält den Schlüssel Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a2875-105">The **DRM\_KeyID** attribute contains the key identifier.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a2875-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="a2875-106">Global Constant</span></span>

<span data-ttu-id="a2875-107">Schlüssel-ID für g \_ wszwmdrm \_</span><span class="sxs-lookup"><span data-stu-id="a2875-107">g\_wszWMDRM\_KeyID</span></span>

## <a name="data-type"></a><span data-ttu-id="a2875-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2875-108">Data Type</span></span>

<span data-ttu-id="a2875-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a2875-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="a2875-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2875-110">Remarks</span></span>

<span data-ttu-id="a2875-111">Dieses Attribut ist nur für den DRM-Inhalt der DRM-Version 7 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a2875-111">This attribute is present for DRM Version 7 content only.</span></span> <span data-ttu-id="a2875-112">Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a2875-112">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span> <span data-ttu-id="a2875-113">Das gleiche Datei Attribut kann mit der [**DRM- \_ drmHeader- \_ keyid**](drm-drmheader-keyid.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a2875-113">The same file attribute can be retrieved using [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

<span data-ttu-id="a2875-114">Die Schlüssel-ID wird zusammen mit dem Schlüssel-Seed zum Erstellen des Inhalts Schlüssels verwendet, der zum Verschlüsseln und Entschlüsseln der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2875-114">The key ID is used in conjunction with the key seed to create the content key which is used to encrypt and decrypt the file.</span></span> <span data-ttu-id="a2875-115">Die Writer-Anwendung verwendet die Schlüssel-ID, um die Datei zu verschlüsseln, und speichert dann die Schlüssel-ID im Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="a2875-115">The writer application uses the key ID to encrypt the file and then it stores the key ID in the file header.</span></span> <span data-ttu-id="a2875-116">Wenn eine Player Anwendung eine Lizenz für eine Datei anfordert, sendet die DRM-Komponente die Schlüssel-ID (zusammen mit dem Rest des DRM-Headers) an den Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="a2875-116">When a player application requests a license for a file, the DRM component sends the key ID (along with the rest of the DRM header) to the license server.</span></span> <span data-ttu-id="a2875-117">Der Lizenzserver, der über den Wert des geheimen Schlüssels verfügt, verwendet ihn und die Schlüssel-ID, um einen Schlüssel für die Datei zu erstellen, der dann zusammen mit den verschiedenen rechten, die auf die Datei angewendet werden, in eine Lizenz eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a2875-117">The license server, which has the secret key seed, uses it and the key ID to create a key for the file, which it then inserts into a license along with the various rights that will be applied to the file.</span></span>

<span data-ttu-id="a2875-118">In der Regel wird ein Schlüssel-Seed mit vielen Schlüssel-IDs verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2875-118">Typically, one key seed is used with many key IDs.</span></span> <span data-ttu-id="a2875-119">Der Schlüsselwert ist ein geheimer Schlüssel, der nur vom Inhalts Ersteller und dem Lizenz Verteiler gemeinsam verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2875-119">The key seed is a secret shared only by the content creator and the license distributor.</span></span> <span data-ttu-id="a2875-120">Die Schlüssel-ID wird von DRM-Client Anwendungen verwendet und im DRM-Header unverschlüsselt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a2875-120">The key ID is used by DRM client applications and is stored in the DRM header in the clear.</span></span>

<span data-ttu-id="a2875-121">Dieses Attribut ist mit der [**DRM- \_ drmHeader- \_ keyid**](drm-drmheader-keyid.md)identisch.</span><span class="sxs-lookup"><span data-stu-id="a2875-121">This attribute is the same as [**DRM\_DRMHeader\_KeyID**](drm-drmheader-keyid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a2875-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2875-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2875-123">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="a2875-123">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




