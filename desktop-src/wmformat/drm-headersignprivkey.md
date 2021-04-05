---
title: DRM_HeaderSignPrivKey
description: Die DRM- \_ Eigenschaft "headersignprivkey" enthält den privaten Schlüssel, der zum Signieren des ASF-Headers verwendet wird.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723488"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="3c457-104">DRM \_ headersignprivkey</span><span class="sxs-lookup"><span data-stu-id="3c457-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="3c457-105">Die DRM-Eigenschaft " **\_ headersignprivkey** " enthält den privaten Schlüssel, der zum Signieren des ASF-Headers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c457-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="3c457-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="3c457-106">Global Constant</span></span>

<span data-ttu-id="3c457-107">g \_ wszwmdrm \_ headersignprivkey</span><span class="sxs-lookup"><span data-stu-id="3c457-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="3c457-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3c457-108">Data Type</span></span>

<span data-ttu-id="3c457-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c457-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="3c457-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c457-110">Remarks</span></span>

<span data-ttu-id="3c457-111">Diese Eigenschaft wird mit dem [**iwmdrmwriter:: generatesigningkeypair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)generiert.</span><span class="sxs-lookup"><span data-stu-id="3c457-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="3c457-112">Behalten Sie diesen geheimen Schlüssel bei, und geben Sie den öffentlichen Schlüssel nur mit dem Lizenz Dienst frei.</span><span class="sxs-lookup"><span data-stu-id="3c457-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="3c457-113">Nachdem Sie diesen Schlüssel festgelegt haben, wird er von der DRM-Komponente zum Signieren des ASF-Datei Headers verwendet (nicht der DRM-Header, der mit den digitalen Signatur Objekt Werten wie z. b. DRM \_ lasignatureprivkey signiert ist).</span><span class="sxs-lookup"><span data-stu-id="3c457-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="3c457-114">Natürlich ist **DRM \_ headersignprivkey** nicht in der Datei headert enthalten.</span><span class="sxs-lookup"><span data-stu-id="3c457-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="3c457-115">Auf diese Eigenschaft kann nicht über das Reader-Objekt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="3c457-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="3c457-116">Sie kann über das Writer-Objekt mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3c457-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="3c457-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c457-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c457-118">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="3c457-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




