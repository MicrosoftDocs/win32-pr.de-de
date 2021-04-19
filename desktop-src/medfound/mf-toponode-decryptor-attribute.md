---
description: Gibt an, ob ein-Objekt, das dem-Objekt zugrunde liegt, eine Entschlüsselung ist.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: MF_TOPONODE_DECRYPTOR-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363375"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="dd6a7-103">MF- \_ Attribut "toponode \_ decryptor"</span><span class="sxs-lookup"><span data-stu-id="dd6a7-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="dd6a7-104">Gibt an, ob das zugrunde liegende Objekt eines topologiedjektes eine Entschlüsselung ist.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="dd6a7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="dd6a7-105">Data type</span></span>

<span data-ttu-id="dd6a7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dd6a7-106">**UINT32**</span></span>

<span data-ttu-id="dd6a7-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd6a7-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd6a7-108">Remarks</span></span>

<span data-ttu-id="dd6a7-109">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="dd6a7-110">Wenn der Wert dieses Attributs ungleich 0 (null) ist, ist das zugrunde liegende Objekt des Knotens eine Entschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="dd6a7-111">Anwendungen verwenden dieses Attribut in der Regel nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="dd6a7-112">Die Medien Sitzung legt dieses Attribut fest, wenn ein Knoten für eine Entschlüsselung erstellt wird, die von der [**imfinputtrustauthority:: getdecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) -Methode abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="dd6a7-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="dd6a7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd6a7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd6a7-114">Requirements</span></span>



| <span data-ttu-id="dd6a7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd6a7-115">Requirement</span></span> | <span data-ttu-id="dd6a7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dd6a7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd6a7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd6a7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd6a7-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd6a7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dd6a7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd6a7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd6a7-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd6a7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dd6a7-121">Header</span><span class="sxs-lookup"><span data-stu-id="dd6a7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd6a7-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd6a7-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd6a7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd6a7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd6a7-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="dd6a7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dd6a7-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dd6a7-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dd6a7-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dd6a7-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dd6a7-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="dd6a7-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="dd6a7-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="dd6a7-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




