---
description: Bei der Verwendung der RegisterDLLs-INF-Direktive für die Selbstregistrierung von DLLs erhalten Aufrufer von setupinstallfrominfsection möglicherweise Benachrichtigungen zu jeder Datei, während Sie registriert oder deren Registrierung aufgehoben wird.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355310"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="2534b-103">Spfilenotify- \_ startregitionsnachricht</span><span class="sxs-lookup"><span data-stu-id="2534b-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="2534b-104">Bei der Verwendung der **RegisterDLLs** -INF-Direktive für die Selbstregistrierung von DLLs erhalten Aufrufer von [**setupinstallfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) möglicherweise Benachrichtigungen zu jeder Datei, während Sie registriert oder deren Registrierung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="2534b-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="2534b-105">Wenn Sie eine **spfilenotify- \_ startregitionsbenachrichtigung** an die Rückruf Routine senden möchten, bevor Sie eine Datei registrieren, schließen Sie spinst \_ registercallbackaware Plus spinst \_ REGSVR in den *Flags* -Parameter von **setupinstallfrominfsection** ein.</span><span class="sxs-lookup"><span data-stu-id="2534b-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="2534b-106">Um eine Benachrichtigung über die Aufhebung der Registrierung zu senden, schließen Sie spinst \_ registercallbackaware Plus spinst \_ unregsvr in den *Flags* -Parameter ein.</span><span class="sxs-lookup"><span data-stu-id="2534b-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="2534b-107">Die Rückruf Routine, die vom *msghandler* -Parameter von [**setupinstallfrominfisection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) angegeben wird, muss der Datentyp " [PSP \_ file \_ Callback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)" sein.</span><span class="sxs-lookup"><span data-stu-id="2534b-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="2534b-108">Legen Sie den *context* -Parameter auf denselben *Kontext* fest, der in **setupinstallfrominfsection** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2534b-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="2534b-109">Legen Sie den *Benachrichtigungs* Parameter auf **spfilenotify \_ startregistration** fest.</span><span class="sxs-lookup"><span data-stu-id="2534b-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="2534b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2534b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2534b-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="2534b-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="2534b-112">Zeiger auf eine [**SP- \_ Register \_ Steuer \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) Element-Status Struktur, die Informationen über die Datei enthält, die registriert oder nicht registriert wird.</span><span class="sxs-lookup"><span data-stu-id="2534b-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="2534b-113">Der Member **CBSIZE** sollte auf die Größe der Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2534b-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="2534b-114">Der **Dateiname** muss auf den voll qualifizierten Pfad der Datei festgelegt werden, die registriert wird.</span><span class="sxs-lookup"><span data-stu-id="2534b-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="2534b-115">**Win32Error** wird nicht verwendet und sollte auf keinen Fehler festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="2534b-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="2534b-116">" **FailureCode** " wird nicht verwendet und sollte auf "auf der festgelegte Ausführung" festgelegt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="2534b-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="2534b-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="2534b-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="2534b-118">Wenn die Datei registriert wird, sollte *Param2* auf einen Zeiger auf einen Wert ungleich 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2534b-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="2534b-119">Wenn die Registrierung der Datei aufgehoben wird, muss *Param2* auf einen Zeiger auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2534b-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2534b-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2534b-120">Return value</span></span>

<span data-ttu-id="2534b-121">Nach dem Empfang der Benachrichtigung kann die Rückruffunktion einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2534b-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="2534b-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2534b-122">Return code</span></span>                                                                                  | <span data-ttu-id="2534b-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2534b-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2534b-124"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="2534b-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="2534b-125">Registrieren oder heben Sie die Registrierung der Datei nicht auf, und deaktivieren Sie die Verarbeitung des INF-Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="2534b-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="2534b-126"><dt>**fileOp- \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="2534b-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="2534b-127">Registrieren oder Aufheben der Registrierung der Datei und Fortsetzen der Verarbeitung des INF-Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="2534b-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="2534b-128"><dt>**Datei \_ übersprungen**</dt></span><span class="sxs-lookup"><span data-stu-id="2534b-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="2534b-129">Registrierung oder Aufhebung der Registrierung der Datei überspringen, die Verarbeitung des INF-Abschnitts fortsetzen</span><span class="sxs-lookup"><span data-stu-id="2534b-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2534b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2534b-130">Requirements</span></span>



| <span data-ttu-id="2534b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2534b-131">Requirement</span></span> | <span data-ttu-id="2534b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2534b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2534b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2534b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2534b-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2534b-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2534b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2534b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2534b-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2534b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2534b-137">Header</span><span class="sxs-lookup"><span data-stu-id="2534b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2534b-138"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2534b-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2534b-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2534b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2534b-140">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2534b-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="2534b-141">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="2534b-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="2534b-142">**Setupinstallfrominf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="2534b-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="2534b-143">**spfilenotify- \_ endregistrierung**</span><span class="sxs-lookup"><span data-stu-id="2534b-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

