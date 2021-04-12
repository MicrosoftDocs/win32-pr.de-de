---
description: Enthält die CLSID eines Quality Managers für die Medien Sitzung.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: MF_SESSION_QUALITY_MANAGER-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346658"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="18d58-103">\_ \_ Quality Manager- \_ Attribut der MF-Sitzung</span><span class="sxs-lookup"><span data-stu-id="18d58-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="18d58-104">Enthält die CLSID eines Quality Managers für die Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="18d58-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="18d58-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="18d58-105">Data type</span></span>

<span data-ttu-id="18d58-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="18d58-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="18d58-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18d58-107">Remarks</span></span>

<span data-ttu-id="18d58-108">Sie können dieses Attribut verwenden, um einen benutzerdefinierten Quality Manager für die Medien Sitzung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="18d58-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="18d58-109">Legen Sie dieses Attribut mithilfe des Parameters *pconfiguration* der Funktion [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) oder [**mfkreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) fest.</span><span class="sxs-lookup"><span data-stu-id="18d58-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="18d58-110">Wenn dieses Attribut festgelegt ist, ruft die Medien Sitzung **cokreateinstance** mit der angegebenen CLSID auf, um den Qualitäts-Manager zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="18d58-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="18d58-111">Das von dieser CLSID erstellte-Objekt muss die [**imvqualitymanager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="18d58-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="18d58-112">Wenn dieses Attribut nicht festgelegt ist, erstellt die Medien Sitzung den Standard-Quality Manager, der in Media Foundation bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18d58-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="18d58-113">Wenn Sie die Medien Sitzung ohne Quality Manager ausführen möchten, legen Sie dieses Attribut auf **GUID \_ null** fest.</span><span class="sxs-lookup"><span data-stu-id="18d58-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="18d58-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="18d58-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d58-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18d58-115">Requirements</span></span>



| <span data-ttu-id="18d58-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18d58-116">Requirement</span></span> | <span data-ttu-id="18d58-117">Wert</span><span class="sxs-lookup"><span data-stu-id="18d58-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18d58-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18d58-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18d58-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18d58-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="18d58-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18d58-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18d58-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18d58-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18d58-122">Header</span><span class="sxs-lookup"><span data-stu-id="18d58-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18d58-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d58-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d58-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18d58-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d58-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="18d58-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18d58-126">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="18d58-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="18d58-127">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="18d58-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="18d58-128">Medien Sitzungs Attribute</span><span class="sxs-lookup"><span data-stu-id="18d58-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




