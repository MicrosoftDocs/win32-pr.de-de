---
description: Tragbare Windows-Geräte unterstützen die folgenden SMS-Eigenschaften.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: SMS-Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359302"
---
# <a name="sms-properties"></a><span data-ttu-id="346e5-103">SMS-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="346e5-103">SMS Properties</span></span>

<span data-ttu-id="346e5-104">Tragbare Windows-Geräte unterstützen die folgenden SMS-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="346e5-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="346e5-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="346e5-105">Property</span></span>                   | <span data-ttu-id="346e5-106">VarType</span><span class="sxs-lookup"><span data-stu-id="346e5-106">VarType</span></span>        | <span data-ttu-id="346e5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="346e5-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346e5-108">**WPD- \_ SMS- \_ Codierung**</span><span class="sxs-lookup"><span data-stu-id="346e5-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="346e5-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="346e5-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="346e5-110">Ein Wert, der angibt, wie der Treiber die vom Client gesendete Textnachricht codieren soll.</span><span class="sxs-lookup"><span data-stu-id="346e5-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="346e5-111">Dies ist eine schreibgeschützte Eigenschaft. der Client kann nicht angeben, welchen Codierungstyp ein Gerät zum Senden von Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="346e5-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="346e5-112">Diese Werte duplizieren die Enumerationswerte der [**WPD- \_ SMS- \_ Codierungen \_**](wpd-sms-encoding-types.md) .</span><span class="sxs-lookup"><span data-stu-id="346e5-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="346e5-113">**\_ \_ Maximale Nutzlast für WPD SMS \_**</span><span class="sxs-lookup"><span data-stu-id="346e5-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="346e5-114">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="346e5-114">**VT\_UI4**</span></span>    | <span data-ttu-id="346e5-115">Die maximale Anzahl von Bytes, die in einer Nachricht enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="346e5-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="346e5-116">**WPD- \_ SMS- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="346e5-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="346e5-117">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="346e5-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="346e5-118">Der Name des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="346e5-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="346e5-119">**WPD- \_ SMS- \_ Timeout**</span><span class="sxs-lookup"><span data-stu-id="346e5-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="346e5-120">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="346e5-120">**VT\_UI4**</span></span>    | <span data-ttu-id="346e5-121">Die Anzahl von Millisekunden, bis ein Timeout zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="346e5-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="346e5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="346e5-122">Requirements</span></span>



| <span data-ttu-id="346e5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="346e5-123">Requirement</span></span> | <span data-ttu-id="346e5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="346e5-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="346e5-125">Header</span><span class="sxs-lookup"><span data-stu-id="346e5-125">Header</span></span><br/> | <dl> <span data-ttu-id="346e5-126"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="346e5-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346e5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="346e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346e5-128">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="346e5-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




