---
description: 'SPFILENOTIFY_ENDREGISTRATION: Wenn Sie die RegisterDlls INF-Direktive verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von SetupInstallFromInfSection möglicherweise Benachrichtigungen zu jeder Datei, wenn sie registriert oder nicht registriert ist.'
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: SPFILENOTIFY_ENDREGISTRATION (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec341c26f9f88390ff1b807e6e932b3b381cd57
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094508"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="e23fb-103">SPFILENOTIFY \_ ENDREGISTRATION-Meldung</span><span class="sxs-lookup"><span data-stu-id="e23fb-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="e23fb-104">Wenn Sie die **RegisterDlls** INF-Direktive verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen zu jeder Datei, wenn sie registriert oder nicht registriert ist.</span><span class="sxs-lookup"><span data-stu-id="e23fb-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="e23fb-105">Um eine **SPFILENOTIFY \_ ENDREGISTRATION-Benachrichtigung** einmal nach dem Registrieren oder Aufheben der Registrierung einer Datei an eine Rückrufroutine zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ REGSVR in den *Flags-Parameter* von **SetupInstallFromInfSection** ein.</span><span class="sxs-lookup"><span data-stu-id="e23fb-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="e23fb-106">Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ UNREGSVR in den *Flags-Parameter* ein.</span><span class="sxs-lookup"><span data-stu-id="e23fb-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="e23fb-107">Die rückrufroutine, die durch den *MsgHandler-Parameter* von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegeben wird, muss vom [Typ PSP \_ FILE \_ CALLBACK sein.](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)</span><span class="sxs-lookup"><span data-stu-id="e23fb-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="e23fb-108">Legen Sie *den Context-Parameter* auf denselben *Kontext fest,* der in **SetupInstallFromInfSection angegeben ist.**</span><span class="sxs-lookup"><span data-stu-id="e23fb-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="e23fb-109">Legen Sie den *Notification-Parameter* **auf SPFILENOTIFY \_ ENDREGISTRATION fest.**</span><span class="sxs-lookup"><span data-stu-id="e23fb-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="e23fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e23fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e23fb-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="e23fb-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e23fb-112">Zeiger auf eine [**SP \_ REGISTER CONTROL \_ \_ STATUS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) die Informationen zur registrierten oder nicht registrierten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="e23fb-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="e23fb-113">Der Member **cbsize** sollte auf die Größe der -Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e23fb-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="e23fb-114">**FileName** sollte auf den vollqualifizierten Pfad der Datei festgelegt werden, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="e23fb-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="e23fb-115">**Win32Error** sollte auf einen Systemfehlercode [festgelegt werden,](/windows/desktop/Debug/system-error-codes) der einen erweiterten Fehlercode angibt.</span><span class="sxs-lookup"><span data-stu-id="e23fb-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="e23fb-116">**FailureCode** sollte auf einen der gültigen Fehlercodes festgelegt werden, die das Ergebnis der Registrierung angeben.</span><span class="sxs-lookup"><span data-stu-id="e23fb-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="e23fb-117">Gültige Fehlercodes finden Sie unter [**SP \_ REGISTER CONTROL \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="e23fb-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="e23fb-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e23fb-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e23fb-119">Wenn die Datei registriert wird, sollte *Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e23fb-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="e23fb-120">Wenn die Registrierung der Datei aufgehoben wird, sollte *Param2* auf einen Zeiger auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e23fb-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e23fb-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e23fb-121">Return value</span></span>

<span data-ttu-id="e23fb-122">Nach dem Empfang der Benachrichtigung gibt die Rückruffunktion möglicherweise einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e23fb-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="e23fb-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e23fb-123">Return code</span></span>                                                                                  | <span data-ttu-id="e23fb-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e23fb-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e23fb-125"><dt>**FILEOP \_ ABORT**</dt></span><span class="sxs-lookup"><span data-stu-id="e23fb-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="e23fb-126">Beenden Sie die Verarbeitung des INF-Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="e23fb-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="e23fb-127"><dt>**FILEOP \_ DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="e23fb-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="e23fb-128">Fahren Sie mit der Verarbeitung des Abschnitts INF fort.</span><span class="sxs-lookup"><span data-stu-id="e23fb-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="e23fb-129"><dt>**FILE \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="e23fb-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="e23fb-130">Fortsetzen der Verarbeitung des INF-Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e23fb-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="e23fb-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e23fb-131">Requirements</span></span>



| <span data-ttu-id="e23fb-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e23fb-132">Requirement</span></span> | <span data-ttu-id="e23fb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e23fb-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e23fb-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e23fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e23fb-135">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e23fb-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e23fb-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e23fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e23fb-137">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e23fb-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e23fb-138">Header</span><span class="sxs-lookup"><span data-stu-id="e23fb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e23fb-139"><dt>Setupapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="e23fb-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e23fb-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e23fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23fb-141">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e23fb-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e23fb-142">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e23fb-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e23fb-143">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="e23fb-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="e23fb-144">**SPFILENOTIFY \_ STARTREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="e23fb-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

