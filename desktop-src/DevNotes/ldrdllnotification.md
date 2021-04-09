---
description: Eine Benachrichtigungs Rückruffunktion, die mit der ldrregisterdllnotification-Funktion angegeben wird.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Ldrdllnotification-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860603"
---
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="615e2-103">Ldrdllnotification-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="615e2-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="615e2-104">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="615e2-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="615e2-105">Eine Benachrichtigungs Rückruffunktion, die mit der [**ldrregisterdllnotification**](ldrregisterdllnotification.md) -Funktion angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="615e2-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="615e2-106">Das Lade Modul ruft diese Funktion auf, wenn eine DLL zum ersten Mal geladen wird.</span><span class="sxs-lookup"><span data-stu-id="615e2-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="615e2-107">**Warnung:** Es ist unsicher, dass die Benachrichtigungs Rückruffunktion Funktionen in einer beliebigen DLL aufruft.</span><span class="sxs-lookup"><span data-stu-id="615e2-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="615e2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="615e2-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="615e2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="615e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="615e2-110">*Notificationreason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="615e2-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="615e2-111">Der Grund, warum die Benachrichtigungs Rückruffunktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="615e2-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="615e2-112">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="615e2-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="615e2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="615e2-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="615e2-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="615e2-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="615e2-115"><dt>**LDR \_ DLL- \_ Benachrichtigungs \_ Grund \_ geladen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="615e2-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="615e2-116">Die dll wurde geladen.</span><span class="sxs-lookup"><span data-stu-id="615e2-116">The DLL was loaded.</span></span> <span data-ttu-id="615e2-117">Der *notificationdata* -Parameter verweist auf eine von der **LDR- \_ dll \_ geladene \_ Benachrichtigungs \_ Daten** Struktur.</span><span class="sxs-lookup"><span data-stu-id="615e2-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="615e2-118"><dt>**LDR \_ DLL- \_ Benachrichtigungs \_ Grund \_ entladen**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="615e2-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="615e2-119">Die dll wurde entladen.</span><span class="sxs-lookup"><span data-stu-id="615e2-119">The DLL was unloaded.</span></span> <span data-ttu-id="615e2-120">Der *notificationdata* -Parameter verweist auf eine von der **LDR- \_ dll \_ entladene \_ Benachrichtigungs \_ Daten** Struktur.</span><span class="sxs-lookup"><span data-stu-id="615e2-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="615e2-121">*Notificationdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="615e2-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="615e2-122">Ein Zeiger auf eine Konstante **LDR- \_ dll- \_ Benachrichtigungs** Union, die Benachrichtigungs Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="615e2-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="615e2-123">Diese Union weist die folgende Definition auf:</span><span class="sxs-lookup"><span data-stu-id="615e2-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="615e2-124">Die von der **LDR- \_ dll \_ geladene \_ Benachrichtigungs \_ Daten** Struktur weist die folgende Definition auf:</span><span class="sxs-lookup"><span data-stu-id="615e2-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="615e2-125">Die **\_ \_ ungeladene \_ Benachrichtigungs \_ Datenstruktur der LDR-dll** weist die folgende Definition auf:</span><span class="sxs-lookup"><span data-stu-id="615e2-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

<span data-ttu-id="615e2-126">*Kontext* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="615e2-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="615e2-127">Ein Zeiger auf die Kontext Daten für die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="615e2-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="615e2-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="615e2-128">Return value</span></span>

<span data-ttu-id="615e2-129">Diese Rückruffunktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="615e2-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="615e2-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="615e2-130">Remarks</span></span>

<span data-ttu-id="615e2-131">Die Benachrichtigungs Rückruffunktion wird aufgerufen, bevor dynamische Verknüpfungen stattfinden.</span><span class="sxs-lookup"><span data-stu-id="615e2-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="615e2-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="615e2-132">Requirements</span></span>



| <span data-ttu-id="615e2-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="615e2-133">Requirement</span></span> | <span data-ttu-id="615e2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="615e2-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="615e2-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="615e2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="615e2-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="615e2-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="615e2-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="615e2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="615e2-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="615e2-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="615e2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="615e2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615e2-140">**Ldrregisterdllnotification**</span><span class="sxs-lookup"><span data-stu-id="615e2-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="615e2-141">**Ldrunregisterdllnotification**</span><span class="sxs-lookup"><span data-stu-id="615e2-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




