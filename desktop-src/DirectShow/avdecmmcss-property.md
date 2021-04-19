---
description: Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungs Thread an.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Avdecmmcss-Eigenschaft (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370815"
---
# <a name="avdecmmcss-property"></a><span data-ttu-id="bf44a-103">Avdecmmcss (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bf44a-103">AVDecMmcss property</span></span>

<span data-ttu-id="bf44a-104">Gibt die MMCSS-Klasse (Multimedia Class Scheduler Service) für den Decodierungs Thread an.</span><span class="sxs-lookup"><span data-stu-id="bf44a-104">Specifies the Multimedia Class Scheduler Service (MMCSS) class for the decoding thread.</span></span>

<span data-ttu-id="bf44a-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bf44a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bf44a-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bf44a-106">Data type</span></span>

<span data-ttu-id="bf44a-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="bf44a-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bf44a-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="bf44a-108">Property GUID</span></span>

<span data-ttu-id="bf44a-109">**Codecapi \_ avdecmmcssclass**</span><span class="sxs-lookup"><span data-stu-id="bf44a-109">**CODECAPI\_AVDecMmcssClass**</span></span>

## <a name="property-value"></a><span data-ttu-id="bf44a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="bf44a-110">Property value</span></span>

<span data-ttu-id="bf44a-111">Der Wert dieser Eigenschaft ist der Name der MMCSS-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bf44a-111">The value of this property is the name of the MMCSS class.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf44a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf44a-112">Remarks</span></span>

<span data-ttu-id="bf44a-113">Mit MMCSS können Anwendungen sicherstellen, dass die Zeit empfindliche Verarbeitung einen priorisierten Zugriff auf CPU-Ressourcen hat.</span><span class="sxs-lookup"><span data-stu-id="bf44a-113">MMCSS enables applications to ensure that time-sensitive processing has prioritized access to CPU resources.</span></span> <span data-ttu-id="bf44a-114">Dies funktioniert, indem registrierte Threads auf höhere Thread Prioritäten erhöht werden, während ihre Prioritäten in regelmäßigen Abständen gesenkt werden, um Zeit für andere Prozesse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="bf44a-114">It works by elevating registered threads to higher thread priorities while periodically decreasing their priorities to yield time to other processes.</span></span>

<span data-ttu-id="bf44a-115">Der empfohlene Wert für Audiodecoder lautet "Audiodatei", und der empfohlene Wert für Video-Decoder ist "Wiedergabe".</span><span class="sxs-lookup"><span data-stu-id="bf44a-115">The recommended value for audio decoders is "Audio," and the recommended value for video decoders is "Playback."</span></span>

<span data-ttu-id="bf44a-116">Wenn der MMCSS-Dienst nicht verfügbar ist oder die angegebene MMCSS-Klasse nicht vorhanden ist, hat das Festlegen der-Eigenschaft keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="bf44a-116">If the MMCSS service is not available or the specified MMCSS class does not exist, setting the property has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf44a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf44a-117">Requirements</span></span>



| <span data-ttu-id="bf44a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf44a-118">Requirement</span></span> | <span data-ttu-id="bf44a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bf44a-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf44a-120">Header</span><span class="sxs-lookup"><span data-stu-id="bf44a-120">Header</span></span><br/> | <dl> <span data-ttu-id="bf44a-121"><dt>UUIDs. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf44a-121"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf44a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf44a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf44a-123">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="bf44a-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bf44a-124">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bf44a-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




