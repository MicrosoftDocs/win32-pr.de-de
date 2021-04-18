---
description: Tragbare Windows-Geräte unterstützen die folgenden Aufgaben Eigenschaften.
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: Task Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368358"
---
# <a name="task-properties"></a><span data-ttu-id="61fdd-103">Task-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="61fdd-103">Task Properties</span></span>

<span data-ttu-id="61fdd-104">Tragbare Windows-Geräte unterstützen die folgenden Aufgaben Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61fdd-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="61fdd-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="61fdd-105">Property</span></span>                         | <span data-ttu-id="61fdd-106">VarType</span><span class="sxs-lookup"><span data-stu-id="61fdd-106">VarType</span></span>        | <span data-ttu-id="61fdd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61fdd-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fdd-108">**WPD- \_ Aufgaben \_ Besitzer**</span><span class="sxs-lookup"><span data-stu-id="61fdd-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="61fdd-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="61fdd-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="61fdd-110">Der Besitzer der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="61fdd-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="61fdd-111">**Ausführung der WPD- \_ Aufgabe in \_ Prozent \_**</span><span class="sxs-lookup"><span data-stu-id="61fdd-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="61fdd-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="61fdd-112">**VT\_UI4**</span></span>    | <span data-ttu-id="61fdd-113">Eine Zahl zwischen 0 und 100, die angibt, wie die Aufgabe fertiggestellt wird.</span><span class="sxs-lookup"><span data-stu-id="61fdd-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="61fdd-114">**Datum der WPD- \_ Task \_ Erinnerung \_**</span><span class="sxs-lookup"><span data-stu-id="61fdd-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="61fdd-115">**VT- \_ Datum**</span><span class="sxs-lookup"><span data-stu-id="61fdd-115">**VT\_DATE**</span></span>   | <span data-ttu-id="61fdd-116">Ein-Wert, der angibt, wann eine Erinnerung gesendet werden soll, um die Aufgabe auszuführen, wenn Sie nicht vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="61fdd-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="61fdd-117">**WPD- \_ Task \_ Status**</span><span class="sxs-lookup"><span data-stu-id="61fdd-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="61fdd-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="61fdd-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="61fdd-119">Eine Zeichen folgen Beschreibung des Status der Aufgabe, z. b. "in Bearbeitung".</span><span class="sxs-lookup"><span data-stu-id="61fdd-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="61fdd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61fdd-120">Requirements</span></span>



| <span data-ttu-id="61fdd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61fdd-121">Requirement</span></span> | <span data-ttu-id="61fdd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="61fdd-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fdd-123">Header</span><span class="sxs-lookup"><span data-stu-id="61fdd-123">Header</span></span><br/> | <dl> <span data-ttu-id="61fdd-124"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="61fdd-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fdd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61fdd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fdd-126">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="61fdd-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




