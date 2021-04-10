---
title: Portabilitäts Makros (RPC. h)
description: Die RPC-Tools erreichen die Unabhängigkeit von Modellen, aufrufen und Benennungs Konventionen durch Zuordnen von Datentypen und Funktions Rückgabe Typen in den generierten Stubdateien und Header Dateien mit Definitionen, die für die einzelnen Plattformen spezifisch sind.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- Portabilitäts Makros RPC
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "103961083"
---
# <a name="portability-macros"></a><span data-ttu-id="a60e7-104">Portabilitäts Makros</span><span class="sxs-lookup"><span data-stu-id="a60e7-104">Portability Macros</span></span>

<span data-ttu-id="a60e7-105">Die RPC-Tools erreichen die Unabhängigkeit von Modellen, aufrufen und Benennungs Konventionen durch Zuordnen von Datentypen und Funktions Rückgabe Typen in den generierten Stubdateien und Header Dateien mit Definitionen, die für die einzelnen Plattformen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="a60e7-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="a60e7-106">Mit diesen Makro Definitionen wird sichergestellt, dass alle Datentypen und Funktionen, die die Bezeichnung " **\_ \_ weit** " erfordern, als Objekte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="a60e7-107">In der folgenden Abbildung werden die Makro Definitionen veranschaulicht, die der Mittelwert Compiler für Funktionsaufrufe zwischen RPC-Komponenten anwendet:</span><span class="sxs-lookup"><span data-stu-id="a60e7-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![Das Diagramm, in dem die Makro Definitionen der Mittel l für Funktionsaufrufe angewendet werden.](images/prog-a29.png)

<span data-ttu-id="a60e7-109">RPC-Makros werden wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="a60e7-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="a60e7-110">Definition</span><span class="sxs-lookup"><span data-stu-id="a60e7-110">Definition</span></span>    | <span data-ttu-id="a60e7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a60e7-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a60e7-112">\_\_RPC- \_ API</span><span class="sxs-lookup"><span data-stu-id="a60e7-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="a60e7-113">Wird auf Aufrufe angewendet, die vom Stub für die Benutzeranwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="a60e7-114">Beide Funktionen befinden sich in demselben ausführbaren Programm.</span><span class="sxs-lookup"><span data-stu-id="a60e7-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="a60e7-115">\_\_RPC- \_ weit</span><span class="sxs-lookup"><span data-stu-id="a60e7-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="a60e7-116">Wird auf die standardmäßige Makro Definition für Zeiger angewendet.</span><span class="sxs-lookup"><span data-stu-id="a60e7-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="a60e7-117">Diese Makro Definition sollte als Teil der Signatur aller vom Benutzer bereitgestellten Funktionen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="a60e7-118">\_\_RPC- \_ Stub</span><span class="sxs-lookup"><span data-stu-id="a60e7-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="a60e7-119">Wird auf Aufrufe der Lauf Zeit Bibliothek auf den Stub angewendet.</span><span class="sxs-lookup"><span data-stu-id="a60e7-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="a60e7-120">Diese Aufrufe können als privat angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="a60e7-121">\_\_RPC- \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="a60e7-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="a60e7-122">Gilt für Aufrufe, die von der Lauf Zeit Bibliothek für die Benutzeranwendung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="a60e7-123">Diese überschreiten die Grenzen zwischen einer DLL und einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a60e7-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="a60e7-124">RPC- \_ Eintrag</span><span class="sxs-lookup"><span data-stu-id="a60e7-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="a60e7-125">Gilt für Aufrufe, die von der Anwendung oder dem Stub für die Lauf Zeit Bibliothek durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="a60e7-126">Diese Makro Definition wird auf alle RPC-Lauf Zeitfunktionen angewendet.</span><span class="sxs-lookup"><span data-stu-id="a60e7-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="a60e7-127">Zum ordnungsgemäßen verknüpfen mit den Microsoft RPC-Laufzeitbibliotheken,-Stub-und-Unterstützungs Routinen müssen einige benutzerdefinierte Funktionen diese Makros ebenfalls in die Funktionsdefinition einschließen.</span><span class="sxs-lookup"><span data-stu-id="a60e7-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="a60e7-128">Verwenden Sie die Makro- **\_ \_ RPC- \_ API** , wenn Sie die der Speicherverwaltung zugeordneten Funktionen, benutzerdefinierte Bindungs Handles und das Attribut "über **tragen \_ als** " definieren und den RPC-Makro **\_ \_ \_ Benutzer** verwenden, wenn Sie die dem Kontext Handle zugeordnete Kontext-Lauf Zeit Routine definieren.</span><span class="sxs-lookup"><span data-stu-id="a60e7-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="a60e7-129">Geben Sie die Funktionen wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="a60e7-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="a60e7-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC- \_ Benutzer- *mittlere \_ Benutzer* Zuordnungen \_ (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_\_ *\_ Benutzer* kostenlos für RPC-Benutzer \_ (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC \_ - *benutzertypbindung* \_ (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_Aufheben der Bindung des RPC- \_ Benutzer *handtyps* \_ (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC \_ - *Benutzertyp* \_ zu \_ lokal</span><span class="sxs-lookup"><span data-stu-id="a60e7-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC \_ - *Benutzertyp* \_ aus \_ lokalem</span><span class="sxs-lookup"><span data-stu-id="a60e7-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC- \_ Benutzertyp \_ in \_ xmit (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC \_ - *Benutzertyp* \_ von \_ xmit (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC \_ - *Benutzertyp* \_ Free \_ lokal</span><span class="sxs-lookup"><span data-stu-id="a60e7-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC \_ - *Benutzertyp* \_ freie \_ inst (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC \_ - *Benutzertyp*" \_ freier \_ xmit (...)"</span><span class="sxs-lookup"><span data-stu-id="a60e7-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a60e7-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC- \_ Benutzer Kontext- \_ Rundown (...)</span><span class="sxs-lookup"><span data-stu-id="a60e7-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="a60e7-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a60e7-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="a60e7-143">Alle Zeiger Parameter in diesen Funktionen müssen mit dem gesamten RPC- **\_ \_ RPC \_**-Typ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a60e7-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a60e7-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a60e7-144">Requirements</span></span>



| <span data-ttu-id="a60e7-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a60e7-145">Requirement</span></span> | <span data-ttu-id="a60e7-146">Wert</span><span class="sxs-lookup"><span data-stu-id="a60e7-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a60e7-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a60e7-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a60e7-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a60e7-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a60e7-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a60e7-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a60e7-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a60e7-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a60e7-151">Header</span><span class="sxs-lookup"><span data-stu-id="a60e7-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a60e7-152"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="a60e7-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





