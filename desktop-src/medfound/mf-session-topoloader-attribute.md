---
description: Enthält die CLSID eines topologieladers für die Medien Sitzung.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359528"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="00665-103">MF- \_ Sitzungs \_ topoloader-Attribut</span><span class="sxs-lookup"><span data-stu-id="00665-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="00665-104">Enthält die CLSID eines topologieladers für die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="00665-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="00665-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="00665-105">Data type</span></span>

<span data-ttu-id="00665-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="00665-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="00665-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00665-107">Remarks</span></span>

<span data-ttu-id="00665-108">Sie können dieses Attribut verwenden, um ein benutzerdefiniertes topologielader für die Medien Sitzung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="00665-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="00665-109">Legen Sie dieses Attribut mithilfe des Parameters *pconfiguration* der Funktion [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) oder der Funktion [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) fest.</span><span class="sxs-lookup"><span data-stu-id="00665-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="00665-110">Wenn dieses Attribut festgelegt ist, ruft die Medien Sitzung **cokreateinstance** mit der angegebenen CLSID auf, wenn das topologielader erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="00665-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="00665-111">Das von dieser CLSID erstellte-Objekt muss die [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="00665-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="00665-112">Wenn dieses Attribut nicht festgelegt ist, erstellt die Medien Sitzung das standardmäßige topologielader, das in Media Foundation bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="00665-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="00665-113">Ein topologielader muss Multithread-Apartments unterstützen.</span><span class="sxs-lookup"><span data-stu-id="00665-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="00665-114">Registrieren Sie den topologielader als ThreadingModel = "both".</span><span class="sxs-lookup"><span data-stu-id="00665-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="00665-115">Wenn Sie das topologielader innerhalb des geschützten Medien Pfads (PMP) verwenden, muss das topologieloader auch eine vertrauenswürdige Komponente sein.</span><span class="sxs-lookup"><span data-stu-id="00665-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="00665-116">Weitere Informationen finden Sie unter [geschützter Medien Pfad](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="00665-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="00665-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="00665-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="00665-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00665-118">Requirements</span></span>



| <span data-ttu-id="00665-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00665-119">Requirement</span></span> | <span data-ttu-id="00665-120">Wert</span><span class="sxs-lookup"><span data-stu-id="00665-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00665-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00665-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00665-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00665-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00665-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00665-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00665-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00665-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00665-125">Header</span><span class="sxs-lookup"><span data-stu-id="00665-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00665-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00665-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00665-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00665-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00665-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="00665-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00665-129">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="00665-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="00665-130">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="00665-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="00665-131">Medien Sitzungs Attribute</span><span class="sxs-lookup"><span data-stu-id="00665-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="00665-132">Benutzerdefinierte topologielader</span><span class="sxs-lookup"><span data-stu-id="00665-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




