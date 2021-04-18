---
title: Clientspec-Enumeration
description: Wird mit der clientprotocolspec-Eigenschaft zum Angeben des Remote Desktop Protokolls verwendet, das zwischen dem Client und dem Server verwendet wird.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Clientspec-Enumeration Remotedesktopdienste
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337296"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="2c822-104">Clientspec-Enumeration</span><span class="sxs-lookup"><span data-stu-id="2c822-104">ClientSpec enumeration</span></span>

<span data-ttu-id="2c822-105">Wird mit der [**clientprotocolspec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) -Eigenschaft zum Angeben des Remote Desktop Protokolls verwendet, das zwischen dem Client und dem Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c822-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c822-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c822-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="2c822-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="2c822-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2c822-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**Fullmode**</span><span class="sxs-lookup"><span data-stu-id="2c822-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="2c822-109">Das Protokoll ist vollständiges Windows 8-Remotedesktop Protokoll.</span><span class="sxs-lookup"><span data-stu-id="2c822-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="2c822-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**Thinclientmode**</span><span class="sxs-lookup"><span data-stu-id="2c822-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="2c822-111">Das Protokoll ist auf die Verwendung von Windows 7 mit SP1 remotefx-Codec und einem kleineren Cache beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2c822-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="2c822-112">Alle anderen Codecs sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2c822-112">All other codecs are disabled.</span></span> <span data-ttu-id="2c822-113">Dieses Protokoll verfügt über den kleinsten Speicherbedarf.</span><span class="sxs-lookup"><span data-stu-id="2c822-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="2c822-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**Smallcachemode**</span><span class="sxs-lookup"><span data-stu-id="2c822-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="2c822-115">Das Protokoll ist mit dem **fullmode** identisch, mit dem Unterschied, dass es einen kleineren Cache verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c822-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c822-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c822-116">Requirements</span></span>



| <span data-ttu-id="2c822-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c822-117">Requirement</span></span> | <span data-ttu-id="2c822-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2c822-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c822-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c822-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c822-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2c822-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="2c822-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c822-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c822-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c822-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2c822-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2c822-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c822-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c822-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c822-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c822-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c822-126">**IMsRdpClientAdvancedSettings8:: clientprotocolspec**</span><span class="sxs-lookup"><span data-stu-id="2c822-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





