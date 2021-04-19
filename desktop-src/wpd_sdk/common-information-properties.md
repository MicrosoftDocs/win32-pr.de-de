---
description: Tragbare Windows-Geräte unterstützen die folgenden allgemeinen Informations Eigenschaften.
ms.assetid: eaae7431-d53d-42a1-9286-001c6f5b1641
title: Allgemeine Informations Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Common
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b773d8404997da20b4196c802ba12286679af683
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373880"
---
# <a name="common-information-properties"></a><span data-ttu-id="83fc3-103">Allgemeine Informations Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="83fc3-103">Common Information Properties</span></span>

<span data-ttu-id="83fc3-104">Tragbare Windows-Geräte unterstützen die folgenden allgemeinen Informations Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="83fc3-104">Windows Portable Devices supports the following common information properties.</span></span>



| <span data-ttu-id="83fc3-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="83fc3-105">Property</span></span>                                      | <span data-ttu-id="83fc3-106">VarType</span><span class="sxs-lookup"><span data-stu-id="83fc3-106">VarType</span></span>        | <span data-ttu-id="83fc3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83fc3-107">Description</span></span>                                                                                              |
|-----------------------------------------------|----------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83fc3-108">**\_Allgemeine Informationen zu \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="83fc3-108">**WPD\_COMMON\_INFORMATION\_NOTES**</span></span>           | <span data-ttu-id="83fc3-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="83fc3-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="83fc3-110">Bei Terminen, Tasks und ähnlichen Objekten enthält diese Eigenschaft Notizen für das angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="83fc3-110">For appointments, tasks, and similar objects, this property contains any notes for the given object.</span></span>     |
| <span data-ttu-id="83fc3-111">**häufig verwendeter WPD- \_ \_ Informations \_ Betreff**</span><span class="sxs-lookup"><span data-stu-id="83fc3-111">**WPD\_COMMON\_INFORMATION\_SUBJECT**</span></span>         | <span data-ttu-id="83fc3-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="83fc3-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="83fc3-113">Ein-Wert, der das Betrefffeld dieses-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="83fc3-113">A value that specifies the subject field of this object.</span></span>                                                 |
| <span data-ttu-id="83fc3-114">**Text für den allgemeinen WPD- \_ \_ Informations \_ \_ Text**</span><span class="sxs-lookup"><span data-stu-id="83fc3-114">**WPD\_COMMON\_INFORMATION\_BODY\_TEXT**</span></span>      | <span data-ttu-id="83fc3-115">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="83fc3-115">**VT\_LPWSTR**</span></span> | <span data-ttu-id="83fc3-116">Diese Eigenschaft enthält den Textkörper eines Objekts im Klartext-oder HTML-Format.</span><span class="sxs-lookup"><span data-stu-id="83fc3-116">This property contains the body text of an object, in plaintext or HTML format.</span></span>                          |
| <span data-ttu-id="83fc3-117">**Allgemeine WPD- \_ \_ Informations \_ Priorität**</span><span class="sxs-lookup"><span data-stu-id="83fc3-117">**WPD\_COMMON\_INFORMATION\_PRIORITY**</span></span>        | <span data-ttu-id="83fc3-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="83fc3-118">**VT\_UI4**</span></span>    | <span data-ttu-id="83fc3-119">Ein-Wert, der die Priorität dieses-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="83fc3-119">A value that specifies the priority of this object.</span></span> <span data-ttu-id="83fc3-120">0 gibt die höchste Priorität an.</span><span class="sxs-lookup"><span data-stu-id="83fc3-120">0 indicates the highest priority.</span></span>                    |
| <span data-ttu-id="83fc3-121">**WPD- \_ allgemeine \_ Informationen \_ Start \_ DateTime**</span><span class="sxs-lookup"><span data-stu-id="83fc3-121">**WPD\_COMMON\_INFORMATION\_START\_DATETIME**</span></span> | <span data-ttu-id="83fc3-122">**VT- \_ Datum**</span><span class="sxs-lookup"><span data-stu-id="83fc3-122">**VT\_DATE**</span></span>   | <span data-ttu-id="83fc3-123">Ein-Wert, der das Datum/die Uhrzeit angibt, zu der ein Termin, eine Aufgabe oder ein ähnliches Objekt gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fc3-123">A value that specifies the date/time that an appointment, task, or similar object is scheduled to start.</span></span> |
| <span data-ttu-id="83fc3-124">**DateTime-Wert für WPD- \_ allgemeine \_ Informationen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="83fc3-124">**WPD\_COMMON\_INFORMATION\_END\_DATETIME**</span></span>   | <span data-ttu-id="83fc3-125">**VT- \_ Datum**</span><span class="sxs-lookup"><span data-stu-id="83fc3-125">**VT\_DATE**</span></span>   | <span data-ttu-id="83fc3-126">Ein-Wert, der das Datum/die Uhrzeit angibt, zu der ein Termin, eine Aufgabe oder ein ähnliches Objekt beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83fc3-126">A value that specifies the date/time that an appointment, task, or similar object is scheduled to end.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="83fc3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83fc3-127">Requirements</span></span>



| <span data-ttu-id="83fc3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83fc3-128">Requirement</span></span> | <span data-ttu-id="83fc3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="83fc3-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="83fc3-130">Header</span><span class="sxs-lookup"><span data-stu-id="83fc3-130">Header</span></span><br/> | <dl> <span data-ttu-id="83fc3-131"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="83fc3-131"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83fc3-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83fc3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83fc3-133">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="83fc3-133">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




