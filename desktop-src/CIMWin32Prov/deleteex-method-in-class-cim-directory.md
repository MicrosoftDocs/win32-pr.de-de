---
description: Die DeleteEx-Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist. Bei dieser Methode handelt es sich um eine erweiterte Version der Delete-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: DeleteEx-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa6427adcc2cf87923b2b76b298cc47373231b56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958317"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a><span data-ttu-id="5df14-104">DeleteEx-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="5df14-104">DeleteEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="5df14-105">Die **DeleteEx** -Methode löscht die logische Datei (oder das Verzeichnis), die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5df14-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="5df14-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**Delete**](delete-method-in-class-cim-directory.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="5df14-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5df14-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5df14-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5df14-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5df14-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5df14-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5df14-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5df14-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5df14-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5df14-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5df14-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="5df14-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5df14-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df14-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5df14-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5df14-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5df14-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="5df14-115">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5df14-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="5df14-116">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5df14-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df14-117">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5df14-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="5df14-118">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="5df14-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="5df14-119">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei (oder das Verzeichnis) ausgeführt, die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5df14-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df14-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5df14-120">Return value</span></span>

<span data-ttu-id="5df14-121">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="5df14-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5df14-122">0</span><span class="sxs-lookup"><span data-stu-id="5df14-122">0</span></span>

<span data-ttu-id="5df14-123">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5df14-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-124">2</span><span class="sxs-lookup"><span data-stu-id="5df14-124">2</span></span>

<span data-ttu-id="5df14-125">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5df14-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-126">8</span><span class="sxs-lookup"><span data-stu-id="5df14-126">8</span></span>

<span data-ttu-id="5df14-127">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="5df14-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-128">9</span><span class="sxs-lookup"><span data-stu-id="5df14-128">9</span></span>

<span data-ttu-id="5df14-129">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="5df14-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-130">10</span><span class="sxs-lookup"><span data-stu-id="5df14-130">10</span></span>

<span data-ttu-id="5df14-131">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5df14-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-132">11</span><span class="sxs-lookup"><span data-stu-id="5df14-132">11</span></span>

<span data-ttu-id="5df14-133">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="5df14-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-134">12</span><span class="sxs-lookup"><span data-stu-id="5df14-134">12</span></span>

<span data-ttu-id="5df14-135">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="5df14-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-136">13</span><span class="sxs-lookup"><span data-stu-id="5df14-136">13</span></span>

<span data-ttu-id="5df14-137">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="5df14-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-138">14</span><span class="sxs-lookup"><span data-stu-id="5df14-138">14</span></span>

<span data-ttu-id="5df14-139">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="5df14-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-140">15</span><span class="sxs-lookup"><span data-stu-id="5df14-140">15</span></span>

<span data-ttu-id="5df14-141">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="5df14-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-142">16</span><span class="sxs-lookup"><span data-stu-id="5df14-142">16</span></span>

<span data-ttu-id="5df14-143">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="5df14-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-144">17</span><span class="sxs-lookup"><span data-stu-id="5df14-144">17</span></span>

<span data-ttu-id="5df14-145">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="5df14-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5df14-146">21</span><span class="sxs-lookup"><span data-stu-id="5df14-146">21</span></span>

<span data-ttu-id="5df14-147">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="5df14-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5df14-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5df14-148">Remarks</span></span>

<span data-ttu-id="5df14-149">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="5df14-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5df14-150">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="5df14-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5df14-151">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5df14-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5df14-152">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5df14-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df14-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5df14-153">Requirements</span></span>



| <span data-ttu-id="5df14-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5df14-154">Requirement</span></span> | <span data-ttu-id="5df14-155">Wert</span><span class="sxs-lookup"><span data-stu-id="5df14-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5df14-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5df14-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5df14-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5df14-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5df14-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5df14-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5df14-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5df14-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5df14-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="5df14-160">Namespace</span></span><br/>                | <span data-ttu-id="5df14-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5df14-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5df14-162">MOF</span><span class="sxs-lookup"><span data-stu-id="5df14-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5df14-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5df14-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5df14-164">DLL</span><span class="sxs-lookup"><span data-stu-id="5df14-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5df14-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5df14-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5df14-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5df14-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df14-167">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="5df14-167">CIM\_Directory</span></span>](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="5df14-168">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="5df14-168">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

