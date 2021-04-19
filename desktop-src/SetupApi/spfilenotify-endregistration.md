---
description: Bei der Verwendung der RegisterDLLs-INF-Direktive für die Selbstregistrierung von DLLs erhalten Aufrufer von setupinstallfrominfsection möglicherweise Benachrichtigungen zu jeder Datei, während Sie registriert oder deren Registrierung aufgehoben wird.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: SPFILENOTIFY_ENDREGISTRATION Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360854"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="e9cbf-103">Spfilenotify- \_ endregistrierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="e9cbf-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="e9cbf-104">Bei der Verwendung der **RegisterDLLs** -INF-Direktive für die Selbstregistrierung von DLLs erhalten Aufrufer von [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen zu jeder Datei, während Sie registriert oder deren Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="e9cbf-105">Um eine **spfilenotify- \_ endregistrierungs** Benachrichtigung an eine Rückruf Routine zu senden, nachdem Sie eine Datei registriert oder die Registrierung aufgehoben haben, schließen Sie spinst \_ registercallbackaware Plus spinst \_ REGSVR in den *Flags* -Parameter von **setupinstallfrominfsection** ein.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="e9cbf-106">Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie spinst \_ registercallbackaware Plus spinst \_ unregsvr in den *Flags* -Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="e9cbf-107">Die Rückruf Routine, die vom *msghandler* -Parameter von [**setupinstallfrominfisection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegeben wird, muss der Datentyp " [PSP \_ file \_ Callback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)" sein.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="e9cbf-108">Legen Sie den *context* -Parameter auf denselben *Kontext* fest, der in **setupinstallfrominfsection** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="e9cbf-109">Legen Sie den *Benachrichtigungs* Parameter auf **spfilenotify \_ endregistration** fest.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="e9cbf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9cbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cbf-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="e9cbf-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cbf-112">Zeiger auf eine [**SP- \_ Register \_ Steuer \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) Element-Status Struktur, die Informationen über die Datei enthält, die registriert oder nicht registriert wird.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="e9cbf-113">Der Member **CBSIZE** sollte auf die Größe der Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="e9cbf-114">Der **Dateiname** sollte auf den voll qualifizierten Pfad der Datei festgelegt werden, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="e9cbf-115">**Win32Error** sollte auf einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes) festgelegt werden, der auf einen erweiterten Fehlercode hinweist.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="e9cbf-116">**FailureCode** sollte auf einen der gültigen Fehlercodes festgelegt werden, der das Ergebnis der Registrierung angibt.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="e9cbf-117">Gültige Fehlercodes finden Sie unter [**SP \_ Register Control- \_ \_ Status**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="e9cbf-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="e9cbf-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e9cbf-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e9cbf-119">Wenn die Datei registriert wird, sollte *Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="e9cbf-120">Wenn die Registrierung der Datei aufgehoben wird, muss *Param2* auf einen Zeiger auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cbf-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9cbf-121">Return value</span></span>

<span data-ttu-id="e9cbf-122">Nach dem Empfang der Benachrichtigung kann die Rückruffunktion einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="e9cbf-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e9cbf-123">Return code</span></span>                                                                                  | <span data-ttu-id="e9cbf-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9cbf-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e9cbf-125"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbf-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="e9cbf-126">Beendet die Verarbeitung des INF-Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="e9cbf-127"><dt>**fileOp- \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbf-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="e9cbf-128">Fahren Sie mit der Verarbeitung des INF-Abschnitts fort.</span><span class="sxs-lookup"><span data-stu-id="e9cbf-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="e9cbf-129"><dt>**Datei \_ übersprungen**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbf-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="e9cbf-130">Fortsetzen der Verarbeitung des INF-Abschnitts</span><span class="sxs-lookup"><span data-stu-id="e9cbf-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="e9cbf-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9cbf-131">Requirements</span></span>



| <span data-ttu-id="e9cbf-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9cbf-132">Requirement</span></span> | <span data-ttu-id="e9cbf-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e9cbf-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cbf-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9cbf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e9cbf-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9cbf-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e9cbf-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9cbf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e9cbf-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9cbf-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9cbf-138">Header</span><span class="sxs-lookup"><span data-stu-id="e9cbf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9cbf-139"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9cbf-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cbf-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9cbf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cbf-141">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e9cbf-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e9cbf-142">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e9cbf-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e9cbf-143">**Setupinstallfrominf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="e9cbf-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="e9cbf-144">**spfilenotify \_ startregistration**</span><span class="sxs-lookup"><span data-stu-id="e9cbf-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

