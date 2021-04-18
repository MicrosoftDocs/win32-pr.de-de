---
description: Die im Objekt Pfad angegebene Datei (oder das Verzeichnis) für das logische Verzeichnis wird von deinstalkomprimiert. Bei dieser Methode handelt es sich um eine erweiterte Version der uncompress-Methode, die von der CIM \_ LogicalFile geerbt wird.
ms.assetid: ef5b7c90-5013-4ec0-bfa6-c32428ffb501
ms.tgt_platform: multiple
title: UncompressEx-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af74132ceeb67e48d39c22bd0172954f26707f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524123"
---
# <a name="uncompressex-method-of-the-cim_directory-class"></a><span data-ttu-id="de0ae-104">UncompressEx-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="de0ae-104">UncompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="de0ae-105">Durch die **UncompressEx** -Methode wird die im Objekt Pfad angegebene Datei für das logische Verzeichnis (oder das Verzeichnis) entkomprimiert.</span><span class="sxs-lookup"><span data-stu-id="de0ae-105">The **UncompressEx** method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="de0ae-106">Bei dieser Methode handelt es sich um eine erweiterte Version der [**uncompress**](uncompress-method-in-class-cim-directory.md) -Methode, die von der [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="de0ae-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de0ae-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="de0ae-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="de0ae-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="de0ae-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="de0ae-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="de0ae-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="de0ae-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="de0ae-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="de0ae-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="de0ae-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="de0ae-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="de0ae-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0ae-113">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de0ae-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de0ae-114">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="de0ae-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="de0ae-115">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="de0ae-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="de0ae-116">*Startdateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de0ae-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de0ae-117">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="de0ae-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="de0ae-118">In der Regel handelt es sich bei diesem Parameter um den *StopFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen</span><span class="sxs-lookup"><span data-stu-id="de0ae-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="de0ae-119">Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de0ae-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="de0ae-120">*Rekursiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de0ae-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de0ae-121">**True** gibt an, dass die Methode rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM- \_ Verzeichnis**](cim-directory.md) Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="de0ae-121">If **TRUE**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="de0ae-122">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="de0ae-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0ae-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de0ae-123">Return value</span></span>

<span data-ttu-id="de0ae-124">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="de0ae-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-125">0</span><span class="sxs-lookup"><span data-stu-id="de0ae-125">0</span></span>

<span data-ttu-id="de0ae-126">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="de0ae-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-127">2</span><span class="sxs-lookup"><span data-stu-id="de0ae-127">2</span></span>

<span data-ttu-id="de0ae-128">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="de0ae-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-129">8</span><span class="sxs-lookup"><span data-stu-id="de0ae-129">8</span></span>

<span data-ttu-id="de0ae-130">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="de0ae-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-131">9</span><span class="sxs-lookup"><span data-stu-id="de0ae-131">9</span></span>

<span data-ttu-id="de0ae-132">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="de0ae-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-133">10</span><span class="sxs-lookup"><span data-stu-id="de0ae-133">10</span></span>

<span data-ttu-id="de0ae-134">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="de0ae-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-135">11</span><span class="sxs-lookup"><span data-stu-id="de0ae-135">11</span></span>

<span data-ttu-id="de0ae-136">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="de0ae-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-137">12</span><span class="sxs-lookup"><span data-stu-id="de0ae-137">12</span></span>

<span data-ttu-id="de0ae-138">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="de0ae-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-139">13</span><span class="sxs-lookup"><span data-stu-id="de0ae-139">13</span></span>

<span data-ttu-id="de0ae-140">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="de0ae-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-141">14</span><span class="sxs-lookup"><span data-stu-id="de0ae-141">14</span></span>

<span data-ttu-id="de0ae-142">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="de0ae-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-143">15</span><span class="sxs-lookup"><span data-stu-id="de0ae-143">15</span></span>

<span data-ttu-id="de0ae-144">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="de0ae-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-145">16</span><span class="sxs-lookup"><span data-stu-id="de0ae-145">16</span></span>

<span data-ttu-id="de0ae-146">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="de0ae-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-147">17</span><span class="sxs-lookup"><span data-stu-id="de0ae-147">17</span></span>

<span data-ttu-id="de0ae-148">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="de0ae-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="de0ae-149">21</span><span class="sxs-lookup"><span data-stu-id="de0ae-149">21</span></span>

<span data-ttu-id="de0ae-150">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="de0ae-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de0ae-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de0ae-151">Remarks</span></span>

<span data-ttu-id="de0ae-152">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="de0ae-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="de0ae-153">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="de0ae-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="de0ae-154">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="de0ae-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="de0ae-155">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="de0ae-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="de0ae-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de0ae-156">Requirements</span></span>



| <span data-ttu-id="de0ae-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de0ae-157">Requirement</span></span> | <span data-ttu-id="de0ae-158">Wert</span><span class="sxs-lookup"><span data-stu-id="de0ae-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de0ae-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de0ae-159">Minimum supported client</span></span><br/> | <span data-ttu-id="de0ae-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de0ae-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de0ae-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de0ae-161">Minimum supported server</span></span><br/> | <span data-ttu-id="de0ae-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de0ae-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de0ae-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="de0ae-163">Namespace</span></span><br/>                | <span data-ttu-id="de0ae-164">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="de0ae-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de0ae-165">MOF</span><span class="sxs-lookup"><span data-stu-id="de0ae-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de0ae-166"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="de0ae-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de0ae-167">DLL</span><span class="sxs-lookup"><span data-stu-id="de0ae-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de0ae-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de0ae-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0ae-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de0ae-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0ae-170">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="de0ae-170">**CIM\_Directory**</span></span>](uncompressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="de0ae-171">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="de0ae-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

