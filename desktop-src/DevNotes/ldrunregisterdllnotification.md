---
description: Bricht die dll-Lade Benachrichtigung ab, die zuvor durch Aufrufen der ldrregisterdllnotification-Funktion registriert wurde.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Ldrunregisterdllnotification-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392922"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="1ac0c-103">Ldrunregisterdllnotification-Funktion</span><span class="sxs-lookup"><span data-stu-id="1ac0c-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="1ac0c-104">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1ac0c-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="1ac0c-105">Bricht die dll-Lade Benachrichtigung ab, die zuvor durch Aufrufen der [**ldrregisterdllnotification**](ldrregisterdllnotification.md) -Funktion registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac0c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ac0c-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="1ac0c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ac0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac0c-108">*Cookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac0c-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac0c-109">Ein Zeiger auf den Rückruf Bezeichner, der vom [**ldrregisterdllnotification**](ldrregisterdllnotification.md) -Befehl empfangen wurde, der für die Benachrichtigung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac0c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ac0c-110">Return value</span></span>

<span data-ttu-id="1ac0c-111">Gibt den **NTSTATUS** -oder-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="1ac0c-112">Wenn die Funktion erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="1ac0c-113">Wenn die Rückruffunktion nicht gefunden wird, gibt die Funktion die **Status- \_ dll \_ nicht \_ gefunden** zurück.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="1ac0c-114">Die Formulare und die Bedeutung von **NTSTATUS** -Fehlercodes sind in der Header Datei "NTSTATUS. h" aufgeführt, die im WDK verfügbar ist, und werden in der WDK-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac0c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ac0c-115">Remarks</span></span>

<span data-ttu-id="1ac0c-116">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-116">This function has no associated header file.</span></span> <span data-ttu-id="1ac0c-117">Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="1ac0c-118">Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac0c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ac0c-119">Requirements</span></span>



| <span data-ttu-id="1ac0c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ac0c-120">Requirement</span></span> | <span data-ttu-id="1ac0c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1ac0c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac0c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ac0c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ac0c-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ac0c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1ac0c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ac0c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ac0c-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ac0c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ac0c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1ac0c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ac0c-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ac0c-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ac0c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ac0c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac0c-129">**Ldrregisterdllnotification**</span><span class="sxs-lookup"><span data-stu-id="1ac0c-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
