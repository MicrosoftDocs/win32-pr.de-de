---
description: Bestimmt, ob der Benutzer über alle erforderlichen Berechtigungen verfügt, die im Berechtigungs Parameter für das Win32-Auslagerungs \_ Datei-Objekt, das Verzeichnis und die Freigabe angegeben sind, in der sich die Auslagerungs Datei befindet, wenn sich die Datei oder das Verzeichnis auf einer Freigabe befinden.
ms.assetid: 1c417ac2-6968-4faf-b596-8df9308f8647
ms.tgt_platform: multiple
title: Geteffectiveberechtigungs Methode der Win32_PageFile-Klasse (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3b9985d18e93f3a3dbcc8f65484bf3fd72284fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958308"
---
# <a name="geteffectivepermission-method-of-the-win32_pagefile-class"></a><span data-ttu-id="dd117-103">Geteffectiveberechtigungs Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd117-103">GetEffectivePermission method of the Win32\_PageFile class</span></span>

<span data-ttu-id="dd117-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode [**geteffectiveberechtigungs**](geteffectivepermission-method-in-class-win32-shortcutfile.md) Methode bestimmt, ob der Benutzer über alle erforderlichen Berechtigungen verfügt, die im *Berechtigungs* Parameter für das Win32-Auslagerungs [**\_ Datei**](win32-pagefile.md) Objekt, das Verzeichnis und die Freigabe angegeben sind, in der sich die Auslagerungs Datei befindet, wenn sich die Datei oder das Verzeichnis auf einer Freigabe befinden.</span><span class="sxs-lookup"><span data-stu-id="dd117-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter identified for the [**Win32\_PageFile**](win32-pagefile.md) object, directory, and share where the paging file is located, if the file or directory are on a share.</span></span>

<span data-ttu-id="dd117-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd117-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dd117-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dd117-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd117-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd117-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="dd117-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd117-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd117-109">*Berechtigungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dd117-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd117-110">Bitmap der Berechtigungen, über die der Aufrufer eine Anfrage erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="dd117-110">Bitmap of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="dd117-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ \_Datei \_ Listen \_ Verzeichnis (Verzeichnis) lesen** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="dd117-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-112">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="dd117-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="dd117-113">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="dd117-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="dd117-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Datei zum \_ Hinzufügen von Daten schreiben (Datei) Datei \_ Hinzufügen \_ (Verzeichnis)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="dd117-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-115">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dd117-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="dd117-116">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd117-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="dd117-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Datei \_ Anfügen von \_ Daten (Datei) \_ \_ Unterverzeichnis (Verzeichnis) hinzufügen** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="dd117-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-118">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="dd117-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="dd117-119">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd117-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="dd117-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="dd117-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-121">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="dd117-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="dd117-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="dd117-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-123">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dd117-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="dd117-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Datei \_ Execute (File) file \_ Traversieren (Verzeichnis)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="dd117-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-125">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dd117-125">Grants the right to execute a file.</span></span> <span data-ttu-id="dd117-126">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="dd117-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="dd117-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ \_Child (Verzeichnis) löschen** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="dd117-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-128">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="dd117-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="dd117-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="dd117-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-130">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="dd117-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="dd117-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="dd117-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-132">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="dd117-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="dd117-133"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="dd117-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-134">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="dd117-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="dd117-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="dd117-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-136">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="dd117-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="dd117-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="dd117-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-138">Gewährt Schreibzugriff auf die freigegebene Zugriffs Steuerungs Liste (DACL).</span><span class="sxs-lookup"><span data-stu-id="dd117-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="dd117-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="dd117-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-140">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="dd117-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="dd117-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="dd117-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="dd117-142">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="dd117-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd117-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dd117-143">Return value</span></span>

<span data-ttu-id="dd117-144">Gibt **true** zurück, wenn der Aufrufer über die angegebenen Berechtigungen verfügt, und **false** , wenn der Aufrufer nicht über die angegebenen Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="dd117-144">Returns **True** if the caller has the specified permissions, and **false** if the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd117-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd117-145">Requirements</span></span>



| <span data-ttu-id="dd117-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd117-146">Requirement</span></span> | <span data-ttu-id="dd117-147">Wert</span><span class="sxs-lookup"><span data-stu-id="dd117-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd117-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd117-148">Minimum supported client</span></span><br/> | <span data-ttu-id="dd117-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd117-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd117-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd117-150">Minimum supported server</span></span><br/> | <span data-ttu-id="dd117-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd117-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd117-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd117-152">Namespace</span></span><br/>                | <span data-ttu-id="dd117-153">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dd117-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd117-154">Header</span><span class="sxs-lookup"><span data-stu-id="dd117-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd117-155"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd117-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="dd117-156">MOF</span><span class="sxs-lookup"><span data-stu-id="dd117-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd117-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd117-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd117-158">DLL</span><span class="sxs-lookup"><span data-stu-id="dd117-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd117-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd117-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd117-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd117-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd117-161">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd117-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dd117-162">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="dd117-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

