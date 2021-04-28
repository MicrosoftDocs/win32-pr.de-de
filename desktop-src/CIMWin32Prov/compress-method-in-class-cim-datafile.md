---
description: 'Compress-Methode der CIM_DataFile Klasse: Verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objektpfad angegeben ist. Diese Methode wird von CIM \_ LogicalFile geerbt.'
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: Compress-Methode der CIM_DataFile Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cc63ed3cafd676a0d865953c52a14e6247d4b70
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089778"
---
# <a name="compress-method-of-the-cim_datafile-class"></a><span data-ttu-id="44d4c-104">Compress-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="44d4c-104">Compress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="44d4c-105">Die **Compress-Methode** verwendet die NTFS-Komprimierung, um die logische Datei (oder das Verzeichnis) zu komprimieren, die im Objektpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="44d4c-105">The **Compress** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="44d4c-106">Diese Methode wird von [**CIM \_ LogicalFile geerbt.**](cim-logicalfile.md)</span><span class="sxs-lookup"><span data-stu-id="44d4c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44d4c-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44d4c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="44d4c-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="44d4c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="44d4c-109">In diesem Thema wird Managed Object Format -Syntax (MOF) verwendet.</span><span class="sxs-lookup"><span data-stu-id="44d4c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44d4c-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="44d4c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44d4c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="44d4c-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="44d4c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="44d4c-112">Parameters</span></span>

<span data-ttu-id="44d4c-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="44d4c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44d4c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44d4c-114">Return value</span></span>

<span data-ttu-id="44d4c-115">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="44d4c-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="44d4c-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="44d4c-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="44d4c-117">Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="44d4c-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="44d4c-118">**0**</span><span class="sxs-lookup"><span data-stu-id="44d4c-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="44d4c-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-120">**2**</span><span class="sxs-lookup"><span data-stu-id="44d4c-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-121">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="44d4c-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-122">**8**</span><span class="sxs-lookup"><span data-stu-id="44d4c-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-123">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="44d4c-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-124">**9**</span><span class="sxs-lookup"><span data-stu-id="44d4c-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-125">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="44d4c-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-126">**10**</span><span class="sxs-lookup"><span data-stu-id="44d4c-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-127">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="44d4c-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-128">**11**</span><span class="sxs-lookup"><span data-stu-id="44d4c-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-129">Dateisystem, nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="44d4c-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-130">**12**</span><span class="sxs-lookup"><span data-stu-id="44d4c-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-131">Plattform, nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="44d4c-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-132">**13**</span><span class="sxs-lookup"><span data-stu-id="44d4c-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-133">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="44d4c-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-134">**14**</span><span class="sxs-lookup"><span data-stu-id="44d4c-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-135">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="44d4c-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-136">**15**</span><span class="sxs-lookup"><span data-stu-id="44d4c-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-137">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="44d4c-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-138">**16**</span><span class="sxs-lookup"><span data-stu-id="44d4c-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-139">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="44d4c-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-140">**17**</span><span class="sxs-lookup"><span data-stu-id="44d4c-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-141">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="44d4c-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="44d4c-142">**21**</span><span class="sxs-lookup"><span data-stu-id="44d4c-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="44d4c-143">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="44d4c-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44d4c-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44d4c-144">Remarks</span></span>

<span data-ttu-id="44d4c-145">Die **Compress-Methode** in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="44d4c-145">The **Compress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="44d4c-146">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="44d4c-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="44d4c-147">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="44d4c-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d4c-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44d4c-148">Requirements</span></span>



| <span data-ttu-id="44d4c-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44d4c-149">Requirement</span></span> | <span data-ttu-id="44d4c-150">Wert</span><span class="sxs-lookup"><span data-stu-id="44d4c-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44d4c-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44d4c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="44d4c-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44d4c-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44d4c-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44d4c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="44d4c-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44d4c-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44d4c-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="44d4c-155">Namespace</span></span><br/>                | <span data-ttu-id="44d4c-156">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="44d4c-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44d4c-157">MOF</span><span class="sxs-lookup"><span data-stu-id="44d4c-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44d4c-158"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="44d4c-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44d4c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="44d4c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44d4c-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44d4c-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d4c-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="44d4c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d4c-162">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="44d4c-162">**CIM\_DataFile**</span></span>](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="44d4c-163">**CIM \_ DataFile**</span><span class="sxs-lookup"><span data-stu-id="44d4c-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="44d4c-164">WMI-Aufgaben: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="44d4c-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="44d4c-165">**Konstanten für Datei- und Verzeichniszugriffsrechte**</span><span class="sxs-lookup"><span data-stu-id="44d4c-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

