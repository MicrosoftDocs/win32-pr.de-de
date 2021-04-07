---
description: Gibt den ursprünglichen Geräte Zeitstempel für das Beispiel an.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: MFSampleExtension_DeviceReferenceSystemTime-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863427"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a><span data-ttu-id="3350a-103">MF Sample Extension \_ devicereferencesystemtime-Attribut</span><span class="sxs-lookup"><span data-stu-id="3350a-103">MFSampleExtension\_DeviceReferenceSystemTime attribute</span></span>

<span data-ttu-id="3350a-104">Gibt den ursprünglichen Geräte Zeitstempel für das Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="3350a-104">Specifies the original device timestamp on the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="3350a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3350a-105">Data type</span></span>

<span data-ttu-id="3350a-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="3350a-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="3350a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3350a-107">Remarks</span></span>

<span data-ttu-id="3350a-108">Dies ist der Zeitstempel eines Geräte Verweises von Medien Beispielen in einer 100-ns-Auflösung.</span><span class="sxs-lookup"><span data-stu-id="3350a-108">This is the a device reference time stamp of media samples in 100ns resolution.</span></span> <span data-ttu-id="3350a-109">Dieser Zeitstempel kann den tatsächlichen Wert des Abfrage Leistungs Zählers (QPC) enthalten, abhängig von der Quelle, die die Beispiele erzeugt.</span><span class="sxs-lookup"><span data-stu-id="3350a-109">This time stamp may or may not carry the actual value of the query performance counter (QPC), depending on the source producing the samples.</span></span> <span data-ttu-id="3350a-110">Dieser Wert kann von anderen Komponenten in der Medien Pipeline geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3350a-110">This value may be modified by other components in the media pipeline.</span></span> <span data-ttu-id="3350a-111">Dieser Wert ist nicht für MFTs verfügbar, die in die Aufzeichnungs Pipeline eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3350a-111">This value is not available to MFTs inserted into the capture pipeline.</span></span>

## <a name="requirements"></a><span data-ttu-id="3350a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3350a-112">Requirements</span></span>



| <span data-ttu-id="3350a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3350a-113">Requirement</span></span> | <span data-ttu-id="3350a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="3350a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3350a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3350a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3350a-116">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="3350a-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3350a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3350a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3350a-118">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3350a-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3350a-119">Header</span><span class="sxs-lookup"><span data-stu-id="3350a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3350a-120"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3350a-120"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="3350a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="3350a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3350a-122"><dt>MF-Engine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3350a-122"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3350a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3350a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3350a-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3350a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




