---
description: Tragbare Windows-Geräte unterstützen die folgenden Termin Eigenschaften.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Termin Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362072"
---
# <a name="appointment-properties"></a><span data-ttu-id="330b2-103">Termin Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="330b2-103">Appointment Properties</span></span>

<span data-ttu-id="330b2-104">Tragbare Windows-Geräte unterstützen die folgenden Termin Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="330b2-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="330b2-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="330b2-105">Property</span></span>                                   | <span data-ttu-id="330b2-106">VarType</span><span class="sxs-lookup"><span data-stu-id="330b2-106">VarType</span></span>        | <span data-ttu-id="330b2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="330b2-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="330b2-108">**der WPD- \_ Termin \_ akzeptierte \_ Teilnehmer**</span><span class="sxs-lookup"><span data-stu-id="330b2-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="330b2-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-110">Durch Semikolons getrennte Liste von Teilnehmern, die den Termin akzeptiert haben.</span><span class="sxs-lookup"><span data-stu-id="330b2-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="330b2-111">**WPD- \_ Termin hat \_ \_ Teilnehmer abgelehnt**</span><span class="sxs-lookup"><span data-stu-id="330b2-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="330b2-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-113">Durch Semikolons getrennte Liste von Teilnehmern, die den Termin abgelehnt haben.</span><span class="sxs-lookup"><span data-stu-id="330b2-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="330b2-114">**WPD- \_ Termin \_ Speicherort**</span><span class="sxs-lookup"><span data-stu-id="330b2-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="330b2-115">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="330b2-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="330b2-116">Ein leserfreundlicher Ort des Termins, z. b. "Gebäude 5, Raum 7".</span><span class="sxs-lookup"><span data-stu-id="330b2-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="330b2-117">**\_ \_ optionale \_ Teilnehmer für WPD-Termin**</span><span class="sxs-lookup"><span data-stu-id="330b2-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="330b2-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-119">Eine durch Semikolons getrennte Liste der optionalen Teilnehmer für den Termin.</span><span class="sxs-lookup"><span data-stu-id="330b2-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="330b2-120">**für WPD- \_ Termin \_ erforderliche \_ Teilnehmer**</span><span class="sxs-lookup"><span data-stu-id="330b2-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="330b2-121">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-122">Durch Semikolons getrennte Liste der erforderlichen Teilnehmer für den Termin.</span><span class="sxs-lookup"><span data-stu-id="330b2-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="330b2-123">**WPD- \_ Termin \_ Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="330b2-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="330b2-124">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-125">Durch Semikolons getrennte Liste der für den Termin erforderlichen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="330b2-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="330b2-126">**\_ \_ vorläufige \_ Teilnehmer für WPD-Termin**</span><span class="sxs-lookup"><span data-stu-id="330b2-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="330b2-127">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-128">Eine durch Semikolons getrennte Liste von Teilnehmern, die den Termin vorläufig akzeptiert haben.</span><span class="sxs-lookup"><span data-stu-id="330b2-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="330b2-129">**WPD \_ - \_ ereigtentyp**</span><span class="sxs-lookup"><span data-stu-id="330b2-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="330b2-130">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="330b2-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="330b2-131">Der Typ des Termins, z. b. "persönlich", "Business" usw.</span><span class="sxs-lookup"><span data-stu-id="330b2-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="330b2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="330b2-132">Requirements</span></span>



| <span data-ttu-id="330b2-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="330b2-133">Requirement</span></span> | <span data-ttu-id="330b2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="330b2-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="330b2-135">Header</span><span class="sxs-lookup"><span data-stu-id="330b2-135">Header</span></span><br/> | <dl> <span data-ttu-id="330b2-136"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="330b2-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330b2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="330b2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330b2-138">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="330b2-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




