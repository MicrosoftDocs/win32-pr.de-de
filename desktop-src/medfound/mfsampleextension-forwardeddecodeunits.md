---
description: Ruft ein Objekt vom Typ imbercollection ab, das imbersample-Objekte enthält, die von einem Decoder weitergeleitete Einheiten für die Netzwerk Abstraktionsschicht (nalus) und zusätzliche Erweiterungs Informationen (was) enthalten.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350582"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a><span data-ttu-id="28892-103">MF SampleExtension \_ forwardeddecodeunits-Attribut</span><span class="sxs-lookup"><span data-stu-id="28892-103">MFSampleExtension\_ForwardedDecodeUnits attribute</span></span>

<span data-ttu-id="28892-104">Ruft ein Objekt vom Typ [**imbercollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) ab, das [**imbersample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Objekte enthält, die von einem Decoder weitergeleitete Einheiten für die Netzwerk Abstraktionsschicht (nalus) und zusätzliche Erweiterungs Informationen (was) enthalten.</span><span class="sxs-lookup"><span data-stu-id="28892-104">Gets an object of type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) containing [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) objects which contain network abstraction layer units (NALUs) and Supplemental Enhancement Information (SEI) units forwarded by a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="28892-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="28892-105">Data type</span></span>

<span data-ttu-id="28892-106">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="28892-106">**IUnknown**</span></span>

## <a name="remarks"></a><span data-ttu-id="28892-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28892-107">Remarks</span></span>

<span data-ttu-id="28892-108">Die Auflistung enthält alle benutzerdefinierten Nalu/ist-Einheiten seit dem vorherigen Frame mit entfernten Emulations bytes.</span><span class="sxs-lookup"><span data-stu-id="28892-108">The collection contains all custom NALU/SEI units since previous frame with emulation prevention bytes removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="28892-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28892-109">Requirements</span></span>



| <span data-ttu-id="28892-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28892-110">Requirement</span></span> | <span data-ttu-id="28892-111">Wert</span><span class="sxs-lookup"><span data-stu-id="28892-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28892-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28892-112">Minimum supported client</span></span><br/> | <span data-ttu-id="28892-113">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28892-113">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="28892-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28892-114">Minimum supported server</span></span><br/> | <span data-ttu-id="28892-115">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28892-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28892-116">Header</span><span class="sxs-lookup"><span data-stu-id="28892-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="28892-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28892-117"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




