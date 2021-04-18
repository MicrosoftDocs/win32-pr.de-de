---
title: DRM_KeySeed
description: Die DRM- \_ keyseed-Eigenschaft enthält den schlüsselseed, der in Verbindung mit der keyid verwendet wird, um den Schlüssel zu erstellen.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340685"
---
# <a name="drm_keyseed"></a><span data-ttu-id="f02e0-104">DRM- \_ keyseed</span><span class="sxs-lookup"><span data-stu-id="f02e0-104">DRM\_KeySeed</span></span>

<span data-ttu-id="f02e0-105">Die **DRM- \_ keyseed** -Eigenschaft enthält den schlüsselseed, der in Verbindung mit der keyid verwendet wird, um den Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f02e0-105">The **DRM\_KeySeed** property contains the key seed that will be used in conjunction with the KeyID to create the key.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f02e0-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="f02e0-106">Global Constant</span></span>

<span data-ttu-id="f02e0-107">g \_ wszwmdrm- \_ keyseed</span><span class="sxs-lookup"><span data-stu-id="f02e0-107">g\_wszWMDRM\_KeySeed</span></span>

## <a name="data-type"></a><span data-ttu-id="f02e0-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f02e0-108">Data Type</span></span>

<span data-ttu-id="f02e0-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f02e0-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="f02e0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f02e0-110">Remarks</span></span>

<span data-ttu-id="f02e0-111">Diese Eigenschaft kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f02e0-111">This property can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span> <span data-ttu-id="f02e0-112">Das Reader-Objekt ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f02e0-112">It is not accessible by the reader object.</span></span>

<span data-ttu-id="f02e0-113">Ein schlüsselseed wird normalerweise verwendet, um mehrere Dateien oder Dateigruppen zu schützen, z. b. alle Dateien, die von einem Lizenzserver ausgestellt werden, oder möglicherweise alle Dateien eines bestimmten Künstlers.</span><span class="sxs-lookup"><span data-stu-id="f02e0-113">A key seed is typically used to protect multiple files or sets of files, for example all the files issued by a license server, or perhaps all the files by a particular artist.</span></span> <span data-ttu-id="f02e0-114">Die keyid ist jedoch für jede Datei eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f02e0-114">The KeyID, however, is unique for each file.</span></span>

<span data-ttu-id="f02e0-115">Der Schlüssel-Seed muss ein Geheimnis bleiben, das nur zwischen dem Inhalts Ersteller und dem Lizenz Verteiler freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f02e0-115">The key seed must remain a secret that is shared only between the content creator and the license distributor.</span></span> <span data-ttu-id="f02e0-116">Dieser Wert wird nicht im DRM-Header gespeichert und ist weder für DRM-Player-Anwendungen noch für den Zugriff verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f02e0-116">This value is not stored in the DRM header and it is neither needed by nor accessible to DRM player applications.</span></span>

<span data-ttu-id="f02e0-117">Ein neuer Schlüssel Ausgangswert kann mithilfe der [**iwmdrmwriter:: generatekeyseed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) -Methode oder durch andere geeignete Mittel generiert werden.</span><span class="sxs-lookup"><span data-stu-id="f02e0-117">A new key seed can be generated using the [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) method or by any other suitable means.</span></span>

## <a name="see-also"></a><span data-ttu-id="f02e0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f02e0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02e0-119">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="f02e0-119">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




