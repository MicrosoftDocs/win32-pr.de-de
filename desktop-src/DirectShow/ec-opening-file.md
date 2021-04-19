---
description: Das Diagramm öffnet eine Datei, oder das Öffnen einer Datei ist abgeschlossen.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361455"
---
# <a name="ec_opening_file"></a><span data-ttu-id="1696e-103">EC- \_ öffnende \_ Datei</span><span class="sxs-lookup"><span data-stu-id="1696e-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="1696e-104">Das Diagramm öffnet eine Datei, oder das Öffnen einer Datei ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1696e-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="1696e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1696e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1696e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1696e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1696e-107">**True** , wenn das Diagramm beginnt, eine Datei zu öffnen, oder **false** , wenn das Diagramm die Datei nicht mehr öffnet.</span><span class="sxs-lookup"><span data-stu-id="1696e-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="1696e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1696e-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1696e-109">Keinen.</span><span class="sxs-lookup"><span data-stu-id="1696e-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="1696e-110">Standardaktion</span><span class="sxs-lookup"><span data-stu-id="1696e-110">Default Action</span></span>

<span data-ttu-id="1696e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1696e-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="1696e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1696e-112">Remarks</span></span>

<span data-ttu-id="1696e-113">Ein Filter kann dieses Ereignis senden, wenn es eine beträchtliche Zeit zum Öffnen einer Datei verbringt.</span><span class="sxs-lookup"><span data-stu-id="1696e-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="1696e-114">(Die Datei befindet sich z. b. möglicherweise in einem Netzwerk.) Die Anwendung kann dieses Ereignis verwenden, um die Benutzeroberfläche anzupassen.</span><span class="sxs-lookup"><span data-stu-id="1696e-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1696e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1696e-115">Requirements</span></span>



| <span data-ttu-id="1696e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1696e-116">Requirement</span></span> | <span data-ttu-id="1696e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1696e-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1696e-118">Header</span><span class="sxs-lookup"><span data-stu-id="1696e-118">Header</span></span><br/> | <dl> <span data-ttu-id="1696e-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="1696e-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1696e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1696e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1696e-121">Ereignis Benachrichtigungs Codes</span><span class="sxs-lookup"><span data-stu-id="1696e-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1696e-122">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="1696e-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




