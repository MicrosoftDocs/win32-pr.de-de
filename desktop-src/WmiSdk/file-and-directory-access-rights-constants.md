---
description: WMI-Klassen, die Dateien oder Verzeichnisse darstellen, wie z. b. Win32 \_ codecfile oder CIM \_ DataFile, enthalten eine AccessMask-Eigenschaft.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Datei-und Verzeichniszugriffs Rechte-Konstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365927"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="d8011-103">Datei-und Verzeichniszugriffs Rechte-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d8011-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="d8011-104">WMI-Klassen, die Dateien oder Verzeichnisse darstellen, wie z. b. [**Win32 \_ codecfile**](/windows/desktop/CIMWin32Prov/win32-codecfile) oder [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), enthalten eine **AccessMask** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d8011-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="d8011-105">Diese Eigenschaft enthält Biteinstellungen, mit denen die Zugriffsrechte angegeben werden, die ein Benutzer oder eine Gruppe für den Zugriff auf die Datei haben muss.</span><span class="sxs-lookup"><span data-stu-id="d8011-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="d8011-106">Weitere Informationen finden Sie unter [Datei Sicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d8011-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="d8011-107">Die Datei-oder Verzeichnis Klassen, die eine **AccessMask** -Eigenschaft enthalten, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d8011-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="d8011-108">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="d8011-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="d8011-109">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="d8011-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="d8011-110">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="d8011-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="d8011-111">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="d8011-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="d8011-112">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="d8011-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="d8011-113">[**Win32- \_ nteventlogfile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8011-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="d8011-114">**Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="d8011-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="d8011-115">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="d8011-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="d8011-116">In der folgenden Liste sind die Werte für Datei-und Verzeichnis Zugriffsrechte in der **AccessMask** -Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d8011-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="d8011-117">Diese Eigenschaft ist eine Bitmap.</span><span class="sxs-lookup"><span data-stu-id="d8011-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="d8011-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**Datei \_ Lese \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="d8011-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d8011-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-120">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d8011-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**Datei \_ Listen \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="d8011-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d8011-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-123">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d8011-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="d8011-124">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="d8011-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**Datei \_ Schreib \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="d8011-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d8011-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-127">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d8011-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**Datei \_ Hinzufügen \_**</span><span class="sxs-lookup"><span data-stu-id="d8011-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-129">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d8011-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-130">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d8011-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="d8011-131">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8011-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**Datei \_ Anfügen \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="d8011-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d8011-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-134">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="d8011-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="d8011-135">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8011-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**\_Unterverzeichnis "Datei hinzufügen" \_**</span><span class="sxs-lookup"><span data-stu-id="d8011-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-137">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d8011-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-138">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="d8011-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="d8011-139">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8011-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lese- \_ EA**</span><span class="sxs-lookup"><span data-stu-id="d8011-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-141">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d8011-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-142">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="d8011-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreib- \_ EA**</span><span class="sxs-lookup"><span data-stu-id="d8011-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-144">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d8011-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-145">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="d8011-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**Datei \_ Ausführung**</span><span class="sxs-lookup"><span data-stu-id="d8011-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-147">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d8011-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-148">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d8011-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**Datei \_ Durchlauf**</span><span class="sxs-lookup"><span data-stu-id="d8011-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-150">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d8011-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-151">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d8011-151">Grants the right to execute a file.</span></span> <span data-ttu-id="d8011-152">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="d8011-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**Datei \_ Delete \_ Child**</span><span class="sxs-lookup"><span data-stu-id="d8011-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-154">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="d8011-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-155">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="d8011-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="d8011-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-157">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="d8011-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-158">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="d8011-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ Schreib \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="d8011-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="d8011-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-161">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d8011-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-162"><span id="DELETE"></span><span id="delete"></span>**Lösch**</span><span class="sxs-lookup"><span data-stu-id="d8011-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-163">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="d8011-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-164">Gewährt das Recht, das Objekt zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d8011-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lese \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="d8011-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-166">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="d8011-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-167">Erteilt das Recht, die Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen.</span><span class="sxs-lookup"><span data-stu-id="d8011-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**\_DAC schreiben**</span><span class="sxs-lookup"><span data-stu-id="d8011-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-169">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="d8011-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-170">Erteilt das Recht, die DACL in der Objekt Sicherheits Beschreibung für das-Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d8011-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**\_Besitzer schreiben**</span><span class="sxs-lookup"><span data-stu-id="d8011-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-172">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="d8011-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-173">Erteilt das Recht, den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d8011-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8011-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisiert**</span><span class="sxs-lookup"><span data-stu-id="d8011-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8011-175">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="d8011-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="d8011-176">Gewährt das Recht, das-Objekt für die Synchronisierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8011-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="d8011-177">Dies ermöglicht einem Prozess, zu warten, bis sich das Objekt im signalisierten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="d8011-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="d8011-178">Einige Objekttypen unterstützen dieses Zugriffsrecht nicht.</span><span class="sxs-lookup"><span data-stu-id="d8011-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8011-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8011-179">Requirements</span></span>



| <span data-ttu-id="d8011-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8011-180">Requirement</span></span> | <span data-ttu-id="d8011-181">Wert</span><span class="sxs-lookup"><span data-stu-id="d8011-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8011-182">Header</span><span class="sxs-lookup"><span data-stu-id="d8011-182">Header</span></span><br/> | <dl> <span data-ttu-id="d8011-183"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8011-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8011-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8011-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8011-185">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="d8011-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="d8011-186">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d8011-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

