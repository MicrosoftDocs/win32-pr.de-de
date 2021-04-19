---
description: Das dvdnotify-Ereignis benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Disk-Anweisungen.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: Dvdnotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371600"
---
# <a name="dvdnotify"></a><span data-ttu-id="9b7a7-103">Dvdnotify</span><span class="sxs-lookup"><span data-stu-id="9b7a7-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="9b7a7-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9b7a7-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9b7a7-106">Das `DVDNotify` Ereignis benachrichtigt eine Anwendung über viele verschiedene DVD-Ereignisse und Disk-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="9b7a7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b7a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b7a7-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="9b7a7-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="9b7a7-109">Gibt den DVD-Ereignis Benachrichtigungs Code an.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9b7a7-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span><span class="sxs-lookup"><span data-stu-id="9b7a7-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="9b7a7-111">Kann zusätzliche Informationen enthalten, die sich auf das Ereignis beziehen.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="9b7a7-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="9b7a7-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="9b7a7-113">Kann zusätzliche Informationen enthalten, die sich auf das Ereignis beziehen.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b7a7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b7a7-114">Remarks</span></span>

<span data-ttu-id="9b7a7-115">Mit [DVD-Ereignis Benachrichtigungs Codes](dvd-notification-codes.md) erhalten Sie eine vollständige Erläuterung aller DVD-Ereignis Benachrichtigungs Codes und ihrer Parameter.</span><span class="sxs-lookup"><span data-stu-id="9b7a7-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b7a7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b7a7-116">Requirements</span></span>



| <span data-ttu-id="9b7a7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b7a7-117">Requirement</span></span> | <span data-ttu-id="9b7a7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9b7a7-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b7a7-119">Header</span><span class="sxs-lookup"><span data-stu-id="9b7a7-119">Header</span></span><br/> | <dl> <span data-ttu-id="9b7a7-120"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b7a7-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




