---
description: Wird für Benachrichtigungen registriert, wenn eine DLL zum ersten Mal geladen wird. Diese Benachrichtigung tritt auf, bevor die dynamische Verknüpfung stattfindet.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Ldrregisterdllnotification-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041345"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="d0a59-104">Ldrregisterdllnotification-Funktion</span><span class="sxs-lookup"><span data-stu-id="d0a59-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="d0a59-105">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="d0a59-106">Wird für Benachrichtigungen registriert, wenn eine DLL zum ersten Mal geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d0a59-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="d0a59-107">Diese Benachrichtigung tritt auf, bevor die dynamische Verknüpfung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="d0a59-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a59-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0a59-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="d0a59-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a59-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a59-111">Dieser Parameter muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d0a59-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d0a59-112">*Notificationfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a59-113">Ein Zeiger auf eine [*ldrdllnotification*](ldrdllnotification.md) -Rückruffunktion, die aufgerufen wird, wenn die dll geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d0a59-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d0a59-114">*Kontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a59-115">Ein Zeiger auf die Kontext Daten für die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="d0a59-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d0a59-116">*Cookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a59-117">Ein Zeiger auf eine Variable, um einen Bezeichner für die Rückruffunktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d0a59-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="d0a59-118">Dieser Bezeichner wird verwendet, um die Registrierung der Benachrichtigungs Rückruffunktion aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="d0a59-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a59-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0a59-119">Return value</span></span>

<span data-ttu-id="d0a59-120">Wenn die Funktion erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0a59-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="d0a59-121">Die Formulare und die Bedeutung von **NTSTATUS** -Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d0a59-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a59-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0a59-122">Remarks</span></span>

<span data-ttu-id="d0a59-123">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d0a59-123">This function has no associated header file.</span></span> <span data-ttu-id="d0a59-124">Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d0a59-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="d0a59-125">Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d0a59-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a59-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0a59-126">Requirements</span></span>



| <span data-ttu-id="d0a59-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0a59-127">Requirement</span></span> | <span data-ttu-id="d0a59-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d0a59-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a59-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0a59-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a59-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d0a59-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0a59-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a59-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a59-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0a59-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d0a59-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0a59-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0a59-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a59-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0a59-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a59-136">*Ldrdllnotification*</span><span class="sxs-lookup"><span data-stu-id="d0a59-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="d0a59-137">**Ldrunregisterdllnotification**</span><span class="sxs-lookup"><span data-stu-id="d0a59-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
