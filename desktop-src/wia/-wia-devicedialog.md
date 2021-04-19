---
description: Wird von Anwendungen verwendet, um dem Benutzer ein Dialogfeld für das Gerät anzuzeigen.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Devicedialog-Funktion (wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349429"
---
# <a name="devicedialog-function"></a><span data-ttu-id="15a32-103">Devicedialog-Funktion</span><span class="sxs-lookup"><span data-stu-id="15a32-103">DeviceDialog function</span></span>

<span data-ttu-id="15a32-104">Wird von Anwendungen verwendet, um dem Benutzer ein Dialogfeld für das Gerät anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="15a32-104">Used by applications to display a device dialog box to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a32-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15a32-105">Syntax</span></span>


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="15a32-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15a32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a32-107">*pdevicedialogdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15a32-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a32-108">Typ: **pdevicedialogdata**</span><span class="sxs-lookup"><span data-stu-id="15a32-108">Type: **PDEVICEDIALOGDATA**</span></span>

<span data-ttu-id="15a32-109">Die [**devicedialogdata**](-wia-devicedialogdata.md) , die zum Erstellen des Dialog Felds für das Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15a32-109">The [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) to use to create the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a32-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15a32-110">Return value</span></span>

<span data-ttu-id="15a32-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15a32-111">Type: **HRESULT**</span></span>

<span data-ttu-id="15a32-112">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="15a32-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15a32-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="15a32-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a32-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15a32-114">Requirements</span></span>



| <span data-ttu-id="15a32-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15a32-115">Requirement</span></span> | <span data-ttu-id="15a32-116">Wert</span><span class="sxs-lookup"><span data-stu-id="15a32-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15a32-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15a32-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15a32-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15a32-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="15a32-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15a32-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15a32-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15a32-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15a32-121">Header</span><span class="sxs-lookup"><span data-stu-id="15a32-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="15a32-122"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="15a32-122"><dt>Wiadevd.h</dt></span></span> </dl>   |
| <span data-ttu-id="15a32-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15a32-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="15a32-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15a32-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a32-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15a32-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a32-126">**Devicedialogdata**</span><span class="sxs-lookup"><span data-stu-id="15a32-126">**DEVICEDIALOGDATA**</span></span>](-wia-devicedialogdata.md)
</dt> </dl>

 

 




