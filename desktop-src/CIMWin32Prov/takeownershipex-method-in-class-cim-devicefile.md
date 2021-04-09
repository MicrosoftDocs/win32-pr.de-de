---
description: Ruft den Besitz der logischen Gerätedatei ab, die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der TakeOwnership-Methode, die von CIM \_ LogicalFile geerbt wird.
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: Takebesitzshipex-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c36239d7d0ea6b0bf3bfa67bfb2f59617ab209a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860631"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="0af09-104">Takebesitzshipex-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0af09-104">TakeOwnerShipEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="0af09-105">Die Methode " **takebesitzshipex** " erhält den Besitz der Datei im logischen Gerät, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0af09-105">The **TakeOwnerShipEx** method obtains ownership of the logical device file specified in the object path.</span></span> <span data-ttu-id="0af09-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**TakeOwnership**](takeownership-method-in-class-cim-devicefile.md) -Methode, die von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="0af09-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="0af09-107">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv durchlaufen und übernimmt den Besitz aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0af09-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0af09-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0af09-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0af09-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0af09-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0af09-110">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0af09-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0af09-111">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0af09-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0af09-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="0af09-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0af09-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0af09-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0af09-114">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0af09-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0af09-115">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0af09-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0af09-116">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0af09-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0af09-117">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0af09-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af09-118">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0af09-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="0af09-119">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten</span><span class="sxs-lookup"><span data-stu-id="0af09-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0af09-120">Wenn dieser Parameter **null** ist, wird der Vorgang für die im **ExecMethod** -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0af09-120">If this parameter is **null**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="0af09-121">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0af09-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af09-122">**True** gibt an, dass die Methode auch rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ Devicefile**](cim-devicefile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0af09-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="0af09-123">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0af09-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0af09-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0af09-124">Return value</span></span>

<span data-ttu-id="0af09-125">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="0af09-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0af09-126">0</span><span class="sxs-lookup"><span data-stu-id="0af09-126">0</span></span>

<span data-ttu-id="0af09-127">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0af09-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-128">2</span><span class="sxs-lookup"><span data-stu-id="0af09-128">2</span></span>

<span data-ttu-id="0af09-129">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="0af09-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-130">8</span><span class="sxs-lookup"><span data-stu-id="0af09-130">8</span></span>

<span data-ttu-id="0af09-131">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0af09-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-132">9</span><span class="sxs-lookup"><span data-stu-id="0af09-132">9</span></span>

<span data-ttu-id="0af09-133">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="0af09-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-134">10</span><span class="sxs-lookup"><span data-stu-id="0af09-134">10</span></span>

<span data-ttu-id="0af09-135">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0af09-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-136">11</span><span class="sxs-lookup"><span data-stu-id="0af09-136">11</span></span>

<span data-ttu-id="0af09-137">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="0af09-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-138">12</span><span class="sxs-lookup"><span data-stu-id="0af09-138">12</span></span>

<span data-ttu-id="0af09-139">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0af09-139">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-140">13</span><span class="sxs-lookup"><span data-stu-id="0af09-140">13</span></span>

<span data-ttu-id="0af09-141">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0af09-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-142">14</span><span class="sxs-lookup"><span data-stu-id="0af09-142">14</span></span>

<span data-ttu-id="0af09-143">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="0af09-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-144">15</span><span class="sxs-lookup"><span data-stu-id="0af09-144">15</span></span>

<span data-ttu-id="0af09-145">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="0af09-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-146">16</span><span class="sxs-lookup"><span data-stu-id="0af09-146">16</span></span>

<span data-ttu-id="0af09-147">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="0af09-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-148">17</span><span class="sxs-lookup"><span data-stu-id="0af09-148">17</span></span>

<span data-ttu-id="0af09-149">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0af09-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0af09-150">21</span><span class="sxs-lookup"><span data-stu-id="0af09-150">21</span></span>

<span data-ttu-id="0af09-151">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="0af09-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0af09-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0af09-152">Remarks</span></span>

<span data-ttu-id="0af09-153">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="0af09-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0af09-154">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="0af09-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0af09-155">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="0af09-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0af09-156">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0af09-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af09-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0af09-157">Requirements</span></span>



| <span data-ttu-id="0af09-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0af09-158">Requirement</span></span> | <span data-ttu-id="0af09-159">Wert</span><span class="sxs-lookup"><span data-stu-id="0af09-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0af09-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0af09-160">Minimum supported client</span></span><br/> | <span data-ttu-id="0af09-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0af09-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0af09-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0af09-162">Minimum supported server</span></span><br/> | <span data-ttu-id="0af09-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0af09-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0af09-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="0af09-164">Namespace</span></span><br/>                | <span data-ttu-id="0af09-165">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0af09-165">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0af09-166">MOF</span><span class="sxs-lookup"><span data-stu-id="0af09-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0af09-167"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0af09-167"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0af09-168">DLL</span><span class="sxs-lookup"><span data-stu-id="0af09-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0af09-169"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0af09-169"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af09-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0af09-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af09-171">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="0af09-171">CIM\_DeviceFile</span></span>](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="0af09-172">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="0af09-172">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

