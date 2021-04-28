---
description: 'SPFILENOTIFY_STARTREGISTRATION Meldung: Wenn sie die INF-Direktive RegisterDlls verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von SetupInstallFromInfSection möglicherweise Benachrichtigungen zu jeder Datei, während sie registriert oder nicht registriert ist.'
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION Meldung (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094498"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="dac49-103">SPFILENOTIFY \_ STARTREGISTRATION-Meldung</span><span class="sxs-lookup"><span data-stu-id="dac49-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="dac49-104">Wenn Sie die INF-Direktive **RegisterDlls** verwenden, um DLLs selbst zu registrieren, erhalten Aufrufer von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen für jede Datei, während sie registriert oder nicht registriert ist.</span><span class="sxs-lookup"><span data-stu-id="dac49-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="dac49-105">Um eine **SPFILENOTIFY \_ STARTREGISTRATION-Benachrichtigung** einmal vor dem Registrieren einer Datei an die Rückrufroutine zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ REGSVR in den *Flags-Parameter* von **SetupInstallFromInfSection** ein.</span><span class="sxs-lookup"><span data-stu-id="dac49-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="dac49-106">Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie SPINST \_ REGISTERCALLBACKAWARE plus SPINST \_ UNREGSVR in den *Flags-Parameter* ein.</span><span class="sxs-lookup"><span data-stu-id="dac49-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="dac49-107">Die vom *MsgHandler-Parameter* von [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegebene Rückrufroutine muss vom Typ [PSP \_ FILE \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)sein.</span><span class="sxs-lookup"><span data-stu-id="dac49-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="dac49-108">Legen Sie den *Context-Parameter* auf den gleichen *Kontext* fest, der in **SetupInstallFromInfSection** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="dac49-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="dac49-109">Legen Sie den *Notification-Parameter* auf **SPFILENOTIFY \_ STARTREGISTRATION** fest.</span><span class="sxs-lookup"><span data-stu-id="dac49-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="dac49-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dac49-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac49-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="dac49-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="dac49-112">Zeiger auf eine [**SP \_ REGISTER CONTROL \_ \_ STATUS-Struktur,**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) die Informationen zur registrierten oder nicht registrierten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="dac49-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="dac49-113">Der **Member cbsize** sollte auf die Größe der -Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dac49-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="dac49-114">Der **FileName-Member** sollte auf den vollqualifizierten Pfad der zu registrierenden Datei festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dac49-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="dac49-115">**Win32Error** wird nicht verwendet und sollte auf NO ERROR festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="dac49-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="dac49-116">**FailureCode** wird nicht verwendet und sollte auf SPREG SUCCESS festgelegt \_ werden.</span><span class="sxs-lookup"><span data-stu-id="dac49-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="dac49-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="dac49-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="dac49-118">Wenn die Datei registriert wird, sollte *Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dac49-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="dac49-119">Wenn die Registrierung der Datei aufgehoben wird, sollte *Param2* auf einen Zeiger auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dac49-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac49-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dac49-120">Return value</span></span>

<span data-ttu-id="dac49-121">Nach dem Empfang der Benachrichtigung gibt die Rückruffunktion möglicherweise einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="dac49-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="dac49-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dac49-122">Return code</span></span>                                                                                  | <span data-ttu-id="dac49-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dac49-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dac49-124"><dt>**FILEOP \_ ABORT**</dt></span><span class="sxs-lookup"><span data-stu-id="dac49-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="dac49-125">Registrieren Oder aufheben Sie die Registrierung der Datei nicht, und beenden Sie die Verarbeitung des INF-Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="dac49-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="dac49-126"><dt>**FILEOP \_ DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="dac49-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="dac49-127">Registrieren Oder aufheben Sie die Registrierung der Datei, und fahren Sie mit der Verarbeitung des INF-Abschnitts fort.</span><span class="sxs-lookup"><span data-stu-id="dac49-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="dac49-128"><dt>**DATEI \_ ÜBERSPRINGEN**</dt></span><span class="sxs-lookup"><span data-stu-id="dac49-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="dac49-129">Überspringen der Registrierung oder Aufhebung der Registrierung der Datei, aber Fortsetzen der Verarbeitung des INF-Abschnitts</span><span class="sxs-lookup"><span data-stu-id="dac49-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dac49-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dac49-130">Requirements</span></span>



| <span data-ttu-id="dac49-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dac49-131">Requirement</span></span> | <span data-ttu-id="dac49-132">Wert</span><span class="sxs-lookup"><span data-stu-id="dac49-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dac49-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dac49-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dac49-134">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dac49-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dac49-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dac49-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dac49-136">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dac49-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dac49-137">Header</span><span class="sxs-lookup"><span data-stu-id="dac49-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac49-138"><dt>Setupapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="dac49-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac49-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dac49-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac49-140">Übersicht</span><span class="sxs-lookup"><span data-stu-id="dac49-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="dac49-141">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="dac49-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="dac49-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="dac49-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="dac49-143">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="dac49-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

