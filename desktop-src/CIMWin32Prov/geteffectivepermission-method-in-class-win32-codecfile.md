---
description: Verwendet die Werte, die im Berechtigungs Parameter festgelegt sind, um zu bestimmen, ob der Benutzer über die angegebenen Berechtigungen in der accessMask-Eigenschaft des Win32- \_ codecfile-Objekts verfügt, das die Codec-Datei darstellt.
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: Geteffectiveberechtigungs Methode der Win32_CodecFile-Klasse (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc2f24071d5ab864e06686f094707d9111ea07ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860948"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a><span data-ttu-id="dedc0-103">Geteffectiveberechtigungs Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="dedc0-103">GetEffectivePermission method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="dedc0-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode [**geteffectiveberechtigungs**](geteffectivepermission-method-in-class-win32-shortcutfile.md) Parameter verwendet die Werte, die im *Berechtigungs* Parameter festgelegt sind, um zu bestimmen, ob der Benutzer über die angegebenen Berechtigungen in der **AccessMask** -Eigenschaft des [**Win32 \_ codecfile**](win32-codecfile.md) -Objekts verfügt, das die Codec-Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="dedc0-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses the values set in the *Permissions* parameter to determine whether the user has the specified permissions set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object that represents the codec file.</span></span> <span data-ttu-id="dedc0-105">Die Berechtigungen gelten für die Datei, das Verzeichnis, in dem sich die Datei befindet, und die Freigabe, wenn sich entweder das Verzeichnis oder die Datei in einer Freigabe befinden.</span><span class="sxs-lookup"><span data-stu-id="dedc0-105">The permissions apply to the file, the directory in which the file resides, and the share, if either the directory or the file are in a share.</span></span>

<span data-ttu-id="dedc0-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="dedc0-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dedc0-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dedc0-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dedc0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dedc0-108">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="dedc0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dedc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dedc0-110">*Berechtigungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dedc0-110">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dedc0-111">Bitmap der Berechtigungen, die in der **AccessMask** -Eigenschaft des [**Win32- \_ codecfile**](win32-codecfile.md) -Objekts festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dedc0-111">Bitmap of permissions that are set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="dedc0-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ \_Datei \_ Listen \_ Verzeichnis (Verzeichnis) lesen** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="dedc0-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-113">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="dedc0-113">Grants the right to read data from the file.</span></span> <span data-ttu-id="dedc0-114">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="dedc0-114">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="dedc0-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Datei zum \_ Hinzufügen von Daten schreiben (Datei) Datei \_ Hinzufügen \_ (Verzeichnis)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="dedc0-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-116">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dedc0-116">Grants the right to write data to the file.</span></span> <span data-ttu-id="dedc0-117">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dedc0-117">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="dedc0-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Datei \_ Anfügen von \_ Daten (Datei) \_ \_ Unterverzeichnis (Verzeichnis) hinzufügen** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="dedc0-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-119">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="dedc0-119">Grants the right to append data to the file.</span></span> <span data-ttu-id="dedc0-120">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dedc0-120">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="dedc0-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="dedc0-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-122">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="dedc0-122">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="dedc0-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="dedc0-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-124">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dedc0-124">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="dedc0-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) file \_ Traversieren (Verzeichnis)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="dedc0-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-126">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dedc0-126">Grants the right to execute a file.</span></span> <span data-ttu-id="dedc0-127">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="dedc0-127">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="dedc0-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ \_Child (Verzeichnis) löschen** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="dedc0-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-129">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="dedc0-129">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="dedc0-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="dedc0-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-131">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="dedc0-131">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="dedc0-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="dedc0-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-133">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dedc0-133">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="dedc0-134"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="dedc0-134"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-135">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="dedc0-135">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="dedc0-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="dedc0-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-137">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="dedc0-137">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="dedc0-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="dedc0-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-139">Gewährt Schreibzugriff auf die freigegebene Zugriffs Steuerungs Liste (ACL).</span><span class="sxs-lookup"><span data-stu-id="dedc0-139">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="dedc0-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="dedc0-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-141">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="dedc0-141">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="dedc0-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="dedc0-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="dedc0-143">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="dedc0-143">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dedc0-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dedc0-144">Return value</span></span>

<span data-ttu-id="dedc0-145">Gibt **true** zurück, wenn der Aufrufer über die angegebenen Berechtigungen verfügt, und **false** , wenn der Aufrufer nicht über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="dedc0-145">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedc0-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dedc0-146">Requirements</span></span>



| <span data-ttu-id="dedc0-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dedc0-147">Requirement</span></span> | <span data-ttu-id="dedc0-148">Wert</span><span class="sxs-lookup"><span data-stu-id="dedc0-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dedc0-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dedc0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="dedc0-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dedc0-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dedc0-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dedc0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="dedc0-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dedc0-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dedc0-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="dedc0-153">Namespace</span></span><br/>                | <span data-ttu-id="dedc0-154">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dedc0-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dedc0-155">Header</span><span class="sxs-lookup"><span data-stu-id="dedc0-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedc0-156"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="dedc0-156"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="dedc0-157">MOF</span><span class="sxs-lookup"><span data-stu-id="dedc0-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dedc0-158"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dedc0-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dedc0-159">DLL</span><span class="sxs-lookup"><span data-stu-id="dedc0-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dedc0-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dedc0-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedc0-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dedc0-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="dedc0-162">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dedc0-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dedc0-163">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="dedc0-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

