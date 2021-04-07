---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der Delete-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4e68e7118088b9da1f1a1e2990c0a253ac85714
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748153"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="1687f-104">DeleteEx-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="1687f-104">DeleteEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="1687f-105">Die **DeleteEx** -Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1687f-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="1687f-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**Delete**](delete-method-in-class-cim-devicefile.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="1687f-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1687f-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1687f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1687f-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1687f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1687f-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="1687f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1687f-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1687f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1687f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1687f-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="1687f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1687f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1687f-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1687f-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1687f-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1687f-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="1687f-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1687f-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1687f-116">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1687f-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1687f-117">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1687f-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="1687f-118">In der Regel ist der Parameter " **StartFileName** " der Parameter " **StopFileName** ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler im vorherigen Methoden aufrufstyp aufgetreten</span><span class="sxs-lookup"><span data-stu-id="1687f-118">Typically, the **StartFileName** parameter is the **StopFileName** parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1687f-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1687f-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1687f-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1687f-120">Return value</span></span>

<span data-ttu-id="1687f-121">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="1687f-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="1687f-122">0</span><span class="sxs-lookup"><span data-stu-id="1687f-122">0</span></span>

<span data-ttu-id="1687f-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1687f-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-124">2</span><span class="sxs-lookup"><span data-stu-id="1687f-124">2</span></span>

<span data-ttu-id="1687f-125">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="1687f-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-126">8</span><span class="sxs-lookup"><span data-stu-id="1687f-126">8</span></span>

<span data-ttu-id="1687f-127">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1687f-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-128">9</span><span class="sxs-lookup"><span data-stu-id="1687f-128">9</span></span>

<span data-ttu-id="1687f-129">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="1687f-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-130">10</span><span class="sxs-lookup"><span data-stu-id="1687f-130">10</span></span>

<span data-ttu-id="1687f-131">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1687f-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-132">11</span><span class="sxs-lookup"><span data-stu-id="1687f-132">11</span></span>

<span data-ttu-id="1687f-133">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="1687f-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-134">12</span><span class="sxs-lookup"><span data-stu-id="1687f-134">12</span></span>

<span data-ttu-id="1687f-135">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="1687f-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-136">13</span><span class="sxs-lookup"><span data-stu-id="1687f-136">13</span></span>

<span data-ttu-id="1687f-137">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="1687f-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-138">14</span><span class="sxs-lookup"><span data-stu-id="1687f-138">14</span></span>

<span data-ttu-id="1687f-139">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="1687f-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-140">15</span><span class="sxs-lookup"><span data-stu-id="1687f-140">15</span></span>

<span data-ttu-id="1687f-141">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="1687f-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-142">16</span><span class="sxs-lookup"><span data-stu-id="1687f-142">16</span></span>

<span data-ttu-id="1687f-143">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="1687f-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-144">17</span><span class="sxs-lookup"><span data-stu-id="1687f-144">17</span></span>

<span data-ttu-id="1687f-145">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="1687f-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1687f-146">21</span><span class="sxs-lookup"><span data-stu-id="1687f-146">21</span></span>

<span data-ttu-id="1687f-147">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="1687f-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1687f-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1687f-148">Remarks</span></span>

<span data-ttu-id="1687f-149">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="1687f-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1687f-150">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="1687f-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1687f-151">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1687f-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1687f-152">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1687f-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1687f-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1687f-153">Requirements</span></span>



| <span data-ttu-id="1687f-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1687f-154">Requirement</span></span> | <span data-ttu-id="1687f-155">Wert</span><span class="sxs-lookup"><span data-stu-id="1687f-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1687f-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1687f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="1687f-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1687f-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1687f-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1687f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="1687f-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1687f-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1687f-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="1687f-160">Namespace</span></span><br/>                | <span data-ttu-id="1687f-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1687f-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1687f-162">MOF</span><span class="sxs-lookup"><span data-stu-id="1687f-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1687f-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1687f-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1687f-164">DLL</span><span class="sxs-lookup"><span data-stu-id="1687f-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1687f-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1687f-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1687f-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1687f-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1687f-167">CIM- \_ Devicefile</span><span class="sxs-lookup"><span data-stu-id="1687f-167">CIM\_DeviceFile</span></span>](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="1687f-168">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="1687f-168">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

