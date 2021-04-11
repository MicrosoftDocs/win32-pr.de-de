---
description: Das Ereignis tritt auf, wenn ein neues Hardware Gerät für Windows-Abbild Beschaffung (WIA) verbunden ist.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: WIA. onabviceconnected-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216061"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="b2597-103">WIA. onabviceconnected-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b2597-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="b2597-104">Das Ereignis tritt auf, wenn ein neues Hardware Gerät für Windows-Abbild Beschaffung (WIA) verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b2597-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2597-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2597-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="b2597-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2597-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="b2597-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="b2597-108">Eine Zeichenfolge, die die ID des verbundenen Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="b2597-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2597-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2597-109">Return value</span></span>

<span data-ttu-id="b2597-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2597-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2597-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2597-111">Remarks</span></span>

<span data-ttu-id="b2597-112">WIA benachrichtigt das Skript oder die Anwendung immer dann, wenn ein neues Hardware Gerät mit dem Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b2597-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="b2597-113">Implementieren Sie die **objwia** \_ **ondeviceconnected ()** -Unterroutine, damit das Skript oder die Anwendung auf die Geräte Verbindung reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="b2597-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="b2597-114">Beispielsweise kann es sein, dass ein Skript die [**Geräte**](-wia-iwia-devices.md) Sammlung aktualisiert, wenn ein neues Gerät installiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2597-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2597-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2597-115">Requirements</span></span>



| <span data-ttu-id="b2597-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2597-116">Requirement</span></span> | <span data-ttu-id="b2597-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b2597-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2597-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2597-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2597-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2597-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2597-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2597-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2597-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2597-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b2597-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b2597-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2597-123"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b2597-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




