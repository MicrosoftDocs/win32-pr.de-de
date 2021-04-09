---
description: Bestimmt, ob der Aufrufer über die aggregierten Berechtigungen für das CIM \_ LogicalFile-Objekt und die Freigabe, auf der sich die Datei oder das Verzeichnis befindet, gemäß der Angabe des Berechtigungs Arguments verfügt.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Geteffectiveberechtigungs Methode der CIM_LogicalFile-Klasse (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cc578436c5d116e202911d2bb68edf7369564a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126499"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="23841-103">Geteffectiveberechtigungs Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="23841-103">GetEffectivePermission method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="23841-104">Die **geteffectiveberechtigungs** Methode bestimmt, ob der Aufrufer über die aggregierten Berechtigungen für das [**CIM \_ LogicalFile**](cim-logicalfile.md) -Objekt und die Freigabe, auf der sich die Datei oder das Verzeichnis befindet, gemäß dem *Berechtigungs* Argument festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="23841-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_LogicalFile**](cim-logicalfile.md) object, and the share on which the file or directory resides, as specified by the *Permissions* argument.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23841-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="23841-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="23841-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="23841-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="23841-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="23841-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="23841-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="23841-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="23841-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="23841-109">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="23841-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="23841-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23841-111">*Berechtigungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23841-111">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23841-112">Liste der Berechtigungen, über die der Benutzer Nachfragen können.</span><span class="sxs-lookup"><span data-stu-id="23841-112">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="23841-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="23841-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="23841-114">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="23841-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="23841-115">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="23841-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="23841-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="23841-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="23841-117">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="23841-117">Grants the right to write data to the file.</span></span> <span data-ttu-id="23841-118">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23841-118">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="23841-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Datei \_ \_Daten anfügen (Datei) oder \_ \_ Unterverzeichnis für Datei hinzufügen (Verzeichnis)** (4)</span><span class="sxs-lookup"><span data-stu-id="23841-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="23841-120">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="23841-120">Grants the right to append data to the file.</span></span> <span data-ttu-id="23841-121">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="23841-121">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="23841-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="23841-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="23841-123">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="23841-123">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="23841-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="23841-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="23841-125">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="23841-125">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="23841-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="23841-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="23841-127">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="23841-127">Grants the right to execute a file.</span></span> <span data-ttu-id="23841-128">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="23841-128">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="23841-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="23841-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="23841-130">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="23841-130">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="23841-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="23841-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="23841-132">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="23841-132">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="23841-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="23841-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="23841-134">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="23841-134">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="23841-135"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="23841-135"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="23841-136">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="23841-136">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="23841-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="23841-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="23841-138">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="23841-138">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="23841-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="23841-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="23841-140">Gewährt Schreibzugriff auf die freigegebene ACL.</span><span class="sxs-lookup"><span data-stu-id="23841-140">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="23841-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="23841-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="23841-142">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="23841-142">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="23841-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="23841-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="23841-144">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="23841-144">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23841-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23841-145">Return value</span></span>

<span data-ttu-id="23841-146">Gibt **true** zurück, wenn der-Befehl über die erforderliche Berechtigung verfügt. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23841-146">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="23841-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23841-147">Remarks</span></span>

<span data-ttu-id="23841-148">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="23841-148">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="23841-149">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="23841-149">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="23841-150">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="23841-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="23841-151">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="23841-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="23841-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23841-152">Requirements</span></span>



| <span data-ttu-id="23841-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23841-153">Requirement</span></span> | <span data-ttu-id="23841-154">Wert</span><span class="sxs-lookup"><span data-stu-id="23841-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23841-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23841-155">Minimum supported client</span></span><br/> | <span data-ttu-id="23841-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23841-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23841-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23841-157">Minimum supported server</span></span><br/> | <span data-ttu-id="23841-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23841-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23841-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="23841-159">Namespace</span></span><br/>                | <span data-ttu-id="23841-160">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="23841-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="23841-161">Header</span><span class="sxs-lookup"><span data-stu-id="23841-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="23841-162"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="23841-162"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="23841-163">MOF</span><span class="sxs-lookup"><span data-stu-id="23841-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23841-164"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="23841-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="23841-165">DLL</span><span class="sxs-lookup"><span data-stu-id="23841-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23841-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23841-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23841-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23841-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23841-168">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="23841-168">**CIM\_LogicalFile**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="23841-169">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="23841-169">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

