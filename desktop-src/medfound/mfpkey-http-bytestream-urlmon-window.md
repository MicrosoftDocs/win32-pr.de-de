---
description: Legt ein Fenster für den Microsoft Media Foundation http-Byte-Stream fest.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: MFPKEY_HTTP_ByteStream_Urlmon_Window-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372466"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="57f88-103">Mfpkey \_ http \_ Bytestream- \_ URLMON- \_ Fenster (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="57f88-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="57f88-104">Legt ein Fenster für den Microsoft Media Foundation http-Byte-Stream fest.</span><span class="sxs-lookup"><span data-stu-id="57f88-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="57f88-105">Das Fenster wird verwendet, um während eines Bindungs Vorgangs Informationen in der Benutzeroberfläche darzustellen.</span><span class="sxs-lookup"><span data-stu-id="57f88-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="57f88-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="57f88-106">Data type</span></span>

<span data-ttu-id="57f88-107">PROPVARIANT-Typ (VT)</span><span class="sxs-lookup"><span data-stu-id="57f88-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="57f88-108">PROPVARIANT-Member</span><span class="sxs-lookup"><span data-stu-id="57f88-108">PROPVARIANT member</span></span>

<span data-ttu-id="57f88-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="57f88-109">**IUnknown\***</span></span>

<span data-ttu-id="57f88-110">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="57f88-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="57f88-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="57f88-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="57f88-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57f88-112">Remarks</span></span>

<span data-ttu-id="57f88-113">Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="57f88-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="57f88-114">Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver.</span><span class="sxs-lookup"><span data-stu-id="57f88-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="57f88-115">Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="57f88-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="57f88-116">Der Wert dieser Eigenschaft ist ein Zeiger auf die **iwindowforbindingui** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="57f88-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="57f88-117">Diese Eigenschaft wird nur angewendet, wenn die Eigenschaft [mfpkey \_ http \_ Bytestream \_ enable \_ URLMON](mfpkey-http-bytestream-enable-urlmon.md) auf **Variant \_ true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="57f88-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f88-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57f88-118">Requirements</span></span>



| <span data-ttu-id="57f88-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57f88-119">Requirement</span></span> | <span data-ttu-id="57f88-120">Wert</span><span class="sxs-lookup"><span data-stu-id="57f88-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57f88-121">Header</span><span class="sxs-lookup"><span data-stu-id="57f88-121">Header</span></span><br/> | <dl> <span data-ttu-id="57f88-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57f88-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f88-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57f88-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f88-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57f88-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
