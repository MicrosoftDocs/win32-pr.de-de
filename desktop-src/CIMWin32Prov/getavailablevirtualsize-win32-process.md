---
description: Ruft die aktuelle Größe des freien virtuellen Adressraums in Bytes ab, der für den Prozess verfügbar ist.
ms.assetid: 13b3b347-5db1-484f-bd1d-3a604eb6bc5b
ms.tgt_platform: multiple
title: Getavailablevirtualsize-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetAvailableVirtualSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ee6e798b8df32822de481f3af1dc6b21a81d1024
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344351"
---
# <a name="getavailablevirtualsize-method-of-the-win32_process-class"></a><span data-ttu-id="a7302-103">Getavailablevirtualsize-Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="a7302-103">GetAvailableVirtualSize method of the Win32\_Process class</span></span>

<span data-ttu-id="a7302-104">Ruft die aktuelle Größe des freien virtuellen Adressraums in Bytes ab, der für den Prozess verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a7302-104">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7302-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7302-105">Syntax</span></span>


```mof
uint32 GetAvailableVirtualSize(
  [out] uint64 AvailableVirtualSize
);
```



## <a name="parameters"></a><span data-ttu-id="a7302-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7302-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7302-107">*Availablevirtualsize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7302-107">*AvailableVirtualSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7302-108">Der *availablevirtualsize* -Parameter gibt den freien virtuellen Adressraum zurück, der für diesen Prozess verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a7302-108">The *AvailableVirtualSize* parameter returns the free virtual address space available to this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7302-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7302-109">Return value</span></span>

<span data-ttu-id="a7302-110">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a7302-110">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="a7302-111">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="a7302-111">Any other number indicates an error.</span></span> <span data-ttu-id="a7302-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a7302-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a7302-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a7302-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a7302-114">**Erfolgreicher Abschluss**</span><span class="sxs-lookup"><span data-stu-id="a7302-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-115">0</span><span class="sxs-lookup"><span data-stu-id="a7302-115">0</span></span>

<span data-ttu-id="a7302-116">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a7302-116">The operation completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="a7302-117">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="a7302-117">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-118">2</span><span class="sxs-lookup"><span data-stu-id="a7302-118">2</span></span>

<span data-ttu-id="a7302-119">Der Benutzer hat keinen Zugriff auf die angeforderten Informationen.</span><span class="sxs-lookup"><span data-stu-id="a7302-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="a7302-120">**Unzureichende Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="a7302-120">**Insufficient privilege**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-121">3</span><span class="sxs-lookup"><span data-stu-id="a7302-121">3</span></span>

<span data-ttu-id="a7302-122">Der Benutzer verfügt nicht über ausreichende Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="a7302-122">The user does not have sufficient privilege.</span></span>

</dd> <dt>

<span data-ttu-id="a7302-123">**Unbekannter Fehler.**</span><span class="sxs-lookup"><span data-stu-id="a7302-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-124">8</span><span class="sxs-lookup"><span data-stu-id="a7302-124">8</span></span>

<span data-ttu-id="a7302-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a7302-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a7302-126">**Der Pfad wurde nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="a7302-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-127">9</span><span class="sxs-lookup"><span data-stu-id="a7302-127">9</span></span>

<span data-ttu-id="a7302-128">Der angegebene Pfad ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a7302-128">The path specified does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="a7302-129">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="a7302-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-130">21</span><span class="sxs-lookup"><span data-stu-id="a7302-130">21</span></span>

<span data-ttu-id="a7302-131">Der angegebene Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a7302-131">The specified parameter is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a7302-132">**Andere**</span><span class="sxs-lookup"><span data-stu-id="a7302-132">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a7302-133">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="a7302-133">22 4294967295</span></span>

<span data-ttu-id="a7302-134">Weitere Werte als die aufgeführten Werte finden Sie in der Dokumentation zu [System Fehler Codes](/windows/desktop/Debug/system-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="a7302-134">For values other than those listed, refer to the [System Error Codes](/windows/desktop/Debug/system-error-codes) documentation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7302-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7302-135">Requirements</span></span>



| <span data-ttu-id="a7302-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7302-136">Requirement</span></span> | <span data-ttu-id="a7302-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a7302-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7302-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7302-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a7302-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a7302-139">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="a7302-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7302-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a7302-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a7302-141">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="a7302-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7302-142">Namespace</span></span><br/>                | <span data-ttu-id="a7302-143">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a7302-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7302-144">MOF</span><span class="sxs-lookup"><span data-stu-id="a7302-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7302-145"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a7302-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7302-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a7302-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7302-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7302-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7302-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7302-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7302-149">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="a7302-149">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

