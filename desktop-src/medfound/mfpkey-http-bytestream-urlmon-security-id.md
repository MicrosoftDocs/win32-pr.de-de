---
description: Legt die Stamm Sicherheits-ID für den Microsoft Media Foundation http-Byte-Stream fest.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361482"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="f828a-103">Mfpkey \_ http \_ Bytestream- \_ URLMON- \_ Sicherheits-ID ( \_ Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f828a-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="f828a-104">Legt die Stamm Sicherheits-ID für den Microsoft Media Foundation http-Byte-Stream fest.</span><span class="sxs-lookup"><span data-stu-id="f828a-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="f828a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f828a-105">Data type</span></span>

<span data-ttu-id="f828a-106">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="f828a-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f828a-107">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="f828a-107">PROPVARIANT member</span></span>

<span data-ttu-id="f828a-108">**Caub**</span><span class="sxs-lookup"><span data-stu-id="f828a-108">**CAUB**</span></span>

<span data-ttu-id="f828a-109">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="f828a-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="f828a-110">**Caub**</span><span class="sxs-lookup"><span data-stu-id="f828a-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="f828a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f828a-111">Remarks</span></span>

<span data-ttu-id="f828a-112">Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f828a-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="f828a-113">Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="f828a-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="f828a-114">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f828a-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="f828a-115">Diese Eigenschaft wird nur angewendet, wenn die Eigenschaft [mfpkey \_ http \_ Bytestream \_ enable \_ URLMON](mfpkey-http-bytestream-enable-urlmon.md) auf **Variant \_ true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f828a-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f828a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f828a-116">Requirements</span></span>



| <span data-ttu-id="f828a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f828a-117">Requirement</span></span> | <span data-ttu-id="f828a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f828a-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f828a-119">Header</span><span class="sxs-lookup"><span data-stu-id="f828a-119">Header</span></span><br/> | <dl> <span data-ttu-id="f828a-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f828a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f828a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f828a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f828a-122">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f828a-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
