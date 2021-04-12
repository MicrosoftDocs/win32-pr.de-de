---
description: Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: WIA. ontransfercomplete-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216059"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="a5f4b-103">WIA. ontransfercomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a5f4b-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="a5f4b-104">Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f4b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5f4b-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="a5f4b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5f4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f4b-107">*Element*</span><span class="sxs-lookup"><span data-stu-id="a5f4b-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="a5f4b-108">Das übermittelte [**Element**](-wia-item.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="a5f4b-109">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="a5f4b-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="a5f4b-110">Der Pfad und der Dateiname des übertragenen Bilds.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f4b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5f4b-111">Return value</span></span>

<span data-ttu-id="a5f4b-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f4b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5f4b-113">Remarks</span></span>

<span data-ttu-id="a5f4b-114">WIA benachrichtigt das Skript oder die Anwendung, wenn eine Datenübertragung, ein Bild oder ein Sound erfolgreich abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="a5f4b-115">Implementieren Sie die **objwia** \_ **ontransfercomplete ()** -Unterroutine, damit das Skript oder die Anwendung auf den Abschluss der Datenübertragung reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="a5f4b-116">Beispielsweise kann es sein, dass ein Skript nach der Übertragung ein Bild anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a5f4b-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f4b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5f4b-117">Requirements</span></span>



| <span data-ttu-id="a5f4b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5f4b-118">Requirement</span></span> | <span data-ttu-id="a5f4b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a5f4b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f4b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5f4b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f4b-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5f4b-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5f4b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5f4b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f4b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5f4b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a5f4b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a5f4b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5f4b-125"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a5f4b-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




