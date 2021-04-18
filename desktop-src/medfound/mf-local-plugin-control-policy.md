---
description: Gibt eine lokale Plug-in-Steuerungs Richtlinie an.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: MF_LOCAL_PLUGIN_CONTROL_POLICY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351155"
---
# <a name="mf_local_plugin_control_policy-attribute"></a><span data-ttu-id="fc598-103">\_ \_ \_ Richtlinien Attribut für lokales MF-Plug-in \_</span><span class="sxs-lookup"><span data-stu-id="fc598-103">MF\_LOCAL\_PLUGIN\_CONTROL\_POLICY attribute</span></span>

<span data-ttu-id="fc598-104">Gibt eine lokale Plug-in-Steuerungs Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="fc598-104">Specifies a local plugin control policy.</span></span>

## <a name="data-type"></a><span data-ttu-id="fc598-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fc598-105">Data type</span></span>

<span data-ttu-id="fc598-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fc598-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fc598-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc598-107">Remarks</span></span>

<span data-ttu-id="fc598-108">Legen Sie dieses Attribut auf eines der MF-Plug-in- [**\_ \_ Steuerungs \_ Richtlinien**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) Werte fest.</span><span class="sxs-lookup"><span data-stu-id="fc598-108">Set this attribute to one of the [**MF\_PLUGIN\_CONTROL\_POLICY**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) values.</span></span>

<span data-ttu-id="fc598-109">Diese Attribute ermöglichen der APP, eine restriktivere lokale Richtlinie als die Prozess weite Richtlinie anzugeben, die von [**imfplugincontrol**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="fc598-109">This attributes allows the app to specify a more restrictive local policy than the process-wide policy configured by [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc598-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc598-110">Requirements</span></span>



| <span data-ttu-id="fc598-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc598-111">Requirement</span></span> | <span data-ttu-id="fc598-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fc598-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fc598-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc598-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fc598-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc598-114">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc598-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc598-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fc598-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc598-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fc598-117">Header</span><span class="sxs-lookup"><span data-stu-id="fc598-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc598-118"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc598-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc598-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc598-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc598-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="fc598-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc598-121">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="fc598-121">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




