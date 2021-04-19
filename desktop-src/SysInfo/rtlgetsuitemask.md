---
description: Ruft eine Bitmaske ab, die die im System verfügbaren Produkt Suites identifiziert. Wenn diese Funktion in einer Anwendung aufgerufen wird, die im Kontext eines Server Silos ausgeführt wird, wird stattdessen die Sammlungs Maske für das Server Silo abgerufen.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Rtlgetsuitemask-Funktion (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356915"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="4fa11-104">Rtlgetsuitemask-Funktion</span><span class="sxs-lookup"><span data-stu-id="4fa11-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="4fa11-105">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="4fa11-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4fa11-106">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="4fa11-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4fa11-107">Ruft eine Bitmaske ab, die die im System verfügbaren Produkt Suites identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="4fa11-108">Wenn diese Funktion in einer Anwendung aufgerufen wird, die im Kontext eines Server Silos ausgeführt wird, wird stattdessen die Sammlungs Maske für das Server Silo abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4fa11-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa11-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fa11-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="4fa11-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fa11-110">Parameters</span></span>

<span data-ttu-id="4fa11-111">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4fa11-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4fa11-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fa11-112">Return value</span></span>

<span data-ttu-id="4fa11-113">Eine Bitmaske, die die im System verfügbaren Produkt Suites identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="4fa11-114">Die Bitmaske kann die folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="4fa11-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="4fa11-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fa11-115">Return value</span></span>                                                                          | <span data-ttu-id="4fa11-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fa11-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fa11-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4fa11-118">Microsoft Small Business Server wurde auf dem System installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fa11-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="4fa11-119">Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="4fa11-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="4fa11-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="4fa11-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="4fa11-122">Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="4fa11-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="4fa11-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="4fa11-124">Microsoft BackOffice-Komponenten werden installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="4fa11-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="4fa11-126">Communications Server 2003, Communications Server 2005, Communications Server 2007 oder Communications Server 2007 R2 ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="4fa11-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="4fa11-128">Terminal Dienste sind installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-128">Terminal Services is installed.</span></span> <span data-ttu-id="4fa11-129">Dieser Wert ist immer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fa11-129">This value is always set.</span></span><br/> <span data-ttu-id="4fa11-130">Wenn **Terminalserver** festgelegt ist, aber **singleuserts** nicht festgelegt ist, wird das System im Anwendungsserver Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fa11-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4fa11-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="4fa11-132">Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz in Kraft installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="4fa11-133">Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="4fa11-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="4fa11-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="4fa11-135">Windows XP Embedded ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="4fa11-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="4fa11-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="4fa11-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="4fa11-139">Remotedesktop wird unterstützt, es wird jedoch nur eine interaktive Sitzung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4fa11-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="4fa11-140">Dieser Wert wird festgelegt, es sei denn, das System wird im Anwendungsserver Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fa11-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="4fa11-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="4fa11-142">Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="4fa11-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="4fa11-144">Windows Server 2003, Web Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="4fa11-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="4fa11-146">Windows Storage Server 2003 R2 oder Windows Storage Server 2003 ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="4fa11-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="4fa11-148">Windows Server 2003, Compute Cluster Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="4fa11-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="4fa11-150">Windows Home Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4fa11-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="4fa11-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fa11-151">Remarks</span></span>

<span data-ttu-id="4fa11-152">Sie sollten nicht nur auf das 0x00000001-Flag zurückgreifen, um zu bestimmen, ob Small Business Server auf dem System installiert ist, da sowohl dieses Flag als auch das 0x00000020-Flag festgelegt werden, wenn diese Produktsuite installiert wird.</span><span class="sxs-lookup"><span data-stu-id="4fa11-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="4fa11-153">Wenn Sie diese Installation auf Windows Server Standard Edition upgraden, wird das 0x00000020-Flag nicht gelöscht, aber das 0x00000001-Flag bleibt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fa11-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="4fa11-154">In diesem Fall ist dies ein Hinweis darauf, dass Small Business Server auf diesem System installiert war.</span><span class="sxs-lookup"><span data-stu-id="4fa11-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="4fa11-155">Wenn diese Installation ein weiteres Upgrade auf Windows Server Enterprise Edition durchführt, bleibt das Flag 0x00000001 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fa11-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa11-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fa11-156">Requirements</span></span>



| <span data-ttu-id="4fa11-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fa11-157">Requirement</span></span> | <span data-ttu-id="4fa11-158">Wert</span><span class="sxs-lookup"><span data-stu-id="4fa11-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa11-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fa11-159">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa11-160">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fa11-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4fa11-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fa11-161">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa11-162">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fa11-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4fa11-163">Header</span><span class="sxs-lookup"><span data-stu-id="4fa11-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fa11-164"><dt>Ntddk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fa11-165">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4fa11-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fa11-166"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="4fa11-167">DLL</span><span class="sxs-lookup"><span data-stu-id="4fa11-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fa11-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fa11-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




