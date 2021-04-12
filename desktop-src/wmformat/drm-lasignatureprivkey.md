---
title: DRM_LASignaturePrivKey
description: Die DRM- \_ lasignatureprivkey-Eigenschaft enthält den privaten Schlüssel, der zum Verschlüsseln des DRM-Headers verwendet wird.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389916"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="fb085-104">DRM- \_ lasignatureprivkey</span><span class="sxs-lookup"><span data-stu-id="fb085-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="fb085-105">Die **DRM- \_ lasignatureprivkey** -Eigenschaft enthält den privaten Schlüssel, der zum Verschlüsseln des DRM-Headers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb085-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="fb085-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="fb085-106">Global Constant</span></span>

<span data-ttu-id="fb085-107">g \_ wszwmdrm \_ lasignatureprivkey</span><span class="sxs-lookup"><span data-stu-id="fb085-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="fb085-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fb085-108">Data Type</span></span>

<span data-ttu-id="fb085-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb085-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="fb085-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb085-110">Remarks</span></span>

<span data-ttu-id="fb085-111">Diese Eigenschaft kann mit der [**iwmdrmwriter:: generatesigningkeypair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) -Methode generiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb085-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="fb085-112">Diese Eigenschaft sollte ein Geheimnis bleiben, das nur vom Inhalts Ersteller bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="fb085-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="fb085-113">Diese Eigenschaft kann mit der [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fb085-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="fb085-114">Das Reader-Objekt ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb085-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb085-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb085-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb085-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="fb085-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




