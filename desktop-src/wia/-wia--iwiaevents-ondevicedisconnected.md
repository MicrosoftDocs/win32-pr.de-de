---
description: Das Ereignis tritt auf, wenn ein neues Hardware Gerät für die Windows-Abbild Erfassung (WIA) getrennt ist.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: WIA. ondevicedevi-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216060"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="5385a-103">WIA. ondevicedevi-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5385a-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="5385a-104">Das Ereignis tritt auf, wenn ein neues Hardware Gerät für die Windows-Abbild Erfassung (WIA) getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="5385a-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="5385a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5385a-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="5385a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5385a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5385a-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="5385a-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="5385a-108">Eine Zeichenfolge, die die ID des verbundenen Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="5385a-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5385a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5385a-109">Return value</span></span>

<span data-ttu-id="5385a-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5385a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5385a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5385a-111">Remarks</span></span>

<span data-ttu-id="5385a-112">WIA benachrichtigt das Skript oder die Anwendung immer dann, wenn ein Hardware Gerät vom Computer getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="5385a-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="5385a-113">Implementieren Sie die **objwia** \_ **ondevicedevi()** -Unterroutine, damit das Skript oder die Anwendung auf die Trennung des Geräts reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="5385a-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="5385a-114">Beispielsweise möchten Sie möglicherweise ein Skript aktualisieren, um die [**Geräte**](-wia-iwia-devices.md) Sammlung zu aktualisieren, wenn ein Gerät vom Computer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5385a-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5385a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5385a-115">Requirements</span></span>



| <span data-ttu-id="5385a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5385a-116">Requirement</span></span> | <span data-ttu-id="5385a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5385a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5385a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5385a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5385a-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5385a-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5385a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5385a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5385a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5385a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5385a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5385a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5385a-123"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="5385a-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




