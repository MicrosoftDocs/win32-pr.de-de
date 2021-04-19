---
description: Tragbare Windows-Geräte unterstützen die folgenden e-Mail-Eigenschaften.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: E-Mail-Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361535"
---
# <a name="email-properties"></a><span data-ttu-id="42b75-103">E-Mail-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42b75-103">Email Properties</span></span>

<span data-ttu-id="42b75-104">Tragbare Windows-Geräte unterstützen die folgenden e-Mail-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42b75-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="42b75-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="42b75-105">Property</span></span>                         | <span data-ttu-id="42b75-106">VarType</span><span class="sxs-lookup"><span data-stu-id="42b75-106">VarType</span></span>        | <span data-ttu-id="42b75-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42b75-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b75-108">**WPD \_ -e-Mail \_ Bcc- \_ Zeile**</span><span class="sxs-lookup"><span data-stu-id="42b75-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="42b75-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="42b75-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="42b75-110">Die Bcc-Empfänger der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="42b75-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="42b75-111">BCC-Empfänger erhalten eine Kopie der e-Mail, deren Namen jedoch nicht als Empfänger angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="42b75-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="42b75-112">**WPD \_ -e-Mail- \_ \_ Leitung**</span><span class="sxs-lookup"><span data-stu-id="42b75-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="42b75-113">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="42b75-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="42b75-114">Die CC-Empfänger der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="42b75-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="42b75-115">CC-Empfänger erhalten eine Kopie der e-Mail-Nachricht, deren Namen als Empfänger angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="42b75-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="42b75-116">**WPD \_ -e-Mail \_ enthält \_ Anlagen**</span><span class="sxs-lookup"><span data-stu-id="42b75-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="42b75-117">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="42b75-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="42b75-118">Ein boolescher Wert, der angibt, ob diese e-Mail über Anlagen verfügt.</span><span class="sxs-lookup"><span data-stu-id="42b75-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="42b75-119">**WPD \_ -e-Mail \_ \_ wurde \_ gelesen**</span><span class="sxs-lookup"><span data-stu-id="42b75-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="42b75-120">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="42b75-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="42b75-121">Ein boolescher Wert, der angibt, ob diese e-Mail-Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="42b75-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="42b75-122">**\_empfangene WPD-e-Mail \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42b75-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="42b75-123">**VT- \_ Datum**</span><span class="sxs-lookup"><span data-stu-id="42b75-123">**VT\_DATE**</span></span>   | <span data-ttu-id="42b75-124">Ein Wert, der angibt, wann die e-Mail-Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="42b75-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="42b75-125">**WPD \_ -e-Mail \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42b75-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="42b75-126">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="42b75-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="42b75-127">Die E-Mail-Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="42b75-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="42b75-128">**WPD \_ -e-Mail \_ an \_ Zeile**</span><span class="sxs-lookup"><span data-stu-id="42b75-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="42b75-129">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="42b75-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="42b75-130">Die Hauptempfänger der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="42b75-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="42b75-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42b75-131">Requirements</span></span>



| <span data-ttu-id="42b75-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42b75-132">Requirement</span></span> | <span data-ttu-id="42b75-133">Wert</span><span class="sxs-lookup"><span data-stu-id="42b75-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b75-134">Header</span><span class="sxs-lookup"><span data-stu-id="42b75-134">Header</span></span><br/> | <dl> <span data-ttu-id="42b75-135"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="42b75-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b75-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42b75-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b75-137">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="42b75-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




