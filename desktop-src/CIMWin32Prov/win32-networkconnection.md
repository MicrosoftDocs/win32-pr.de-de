---
description: Stellt eine aktive Netzwerkverbindung in einer Windows-basierten Umgebung dar.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Win32_NetworkConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748912"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="e2a03-103">Win32 \_ Network Connection-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2a03-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="e2a03-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md)von **Win32 \_ NetworkConnection** stellt eine aktive Netzwerkverbindung in einer Windows-basierten Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="e2a03-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="e2a03-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2a03-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e2a03-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e2a03-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a03-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="e2a03-108">Member</span><span class="sxs-lookup"><span data-stu-id="e2a03-108">Members</span></span>

<span data-ttu-id="e2a03-109">Die **Win32- \_ Network Connection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e2a03-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="e2a03-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2a03-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2a03-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e2a03-111">Properties</span></span>

<span data-ttu-id="e2a03-112">Die **Win32 \_ Network Connection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2a03-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2a03-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="e2a03-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2a03-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-116">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e2a03-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-117">Liste der Zugriffsrechte für die Datei oder das Verzeichnis, die der Benutzer oder die Gruppe hat, in deren Namen die Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e2a03-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="e2a03-118">Auf FAT-Volumes wird stattdessen der **vollständige \_ Zugriffs** Wert zurückgegeben, der angibt, dass für das Objekt keine Sicherheit festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2a03-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="e2a03-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Datei \_ Lesen von \_ Daten (Datei) oder Datei \_ Listen \_ Verzeichnis (Verzeichnis)** (1)</span><span class="sxs-lookup"><span data-stu-id="e2a03-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-120">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="e2a03-121">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="e2a03-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="e2a03-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Datei \_ Schreiben von \_ Daten (Datei) oder Datei \_ Hinzufügen \_ (Verzeichnis)** (2)</span><span class="sxs-lookup"><span data-stu-id="e2a03-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-123">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e2a03-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="e2a03-124">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="e2a03-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Datei \_ Anfügen von \_ Daten (Datei) oder \_ \_ Unterverzeichnis "Datei hinzufügen** " (4)</span><span class="sxs-lookup"><span data-stu-id="e2a03-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-126">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="e2a03-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="e2a03-127">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="e2a03-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Datei \_ Lesen von \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="e2a03-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-129">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="e2a03-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="e2a03-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Datei \_ Schreiben von \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="e2a03-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-131">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e2a03-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="e2a03-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Datei \_ Execute (File) oder file \_ Traversieren (Verzeichnis)** (32)</span><span class="sxs-lookup"><span data-stu-id="e2a03-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-133">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-133">Grants the right to execute a file.</span></span> <span data-ttu-id="e2a03-134">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="e2a03-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="e2a03-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Datei \_ Untergeordnetes Element \_ (Verzeichnis) löschen** (64)</span><span class="sxs-lookup"><span data-stu-id="e2a03-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-136">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="e2a03-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="e2a03-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Datei \_ Lese \_ Attribute** (128)</span><span class="sxs-lookup"><span data-stu-id="e2a03-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-138">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="e2a03-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Datei \_ \_Attribute schreiben** (256)</span><span class="sxs-lookup"><span data-stu-id="e2a03-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-140">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e2a03-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="e2a03-141"><span id="DELETE"></span><span id="delete"></span>**Löschen** (65536)</span><span class="sxs-lookup"><span data-stu-id="e2a03-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-142">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="e2a03-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="e2a03-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lesen Sie \_ Steuer** Element (131072)</span><span class="sxs-lookup"><span data-stu-id="e2a03-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-144">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="e2a03-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="e2a03-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Schreiben \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="e2a03-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-146">Gewährt Schreibzugriff auf die freigegebene Zugriffs Steuerungs Liste (DACL).</span><span class="sxs-lookup"><span data-stu-id="e2a03-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="e2a03-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Schreiben \_ Besitzer** (524288)</span><span class="sxs-lookup"><span data-stu-id="e2a03-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-148">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="e2a03-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="e2a03-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Synchronisieren** (1048576)</span><span class="sxs-lookup"><span data-stu-id="e2a03-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="e2a03-150">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e2a03-151">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e2a03-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-154">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e2a03-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-155">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2a03-155">A short textual description of the object.</span></span>

<span data-ttu-id="e2a03-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-157">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="e2a03-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-160">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *lpcomment*")</span><span class="sxs-lookup"><span data-stu-id="e2a03-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-161">Vom Netzwerkanbieter bereitgestellter Kommentar.</span><span class="sxs-lookup"><span data-stu-id="e2a03-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="e2a03-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-165">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (20), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Network Management Structures \| [**use \_ Info \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ Status**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-166">Aktueller Status der Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="e2a03-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="e2a03-167">**Verbunden** ("verbunden")</span><span class="sxs-lookup"><span data-stu-id="e2a03-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2a03-168">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="e2a03-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e2a03-169">**Angeh** alten ("angehalten")</span><span class="sxs-lookup"><span data-stu-id="e2a03-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="e2a03-170">**Getrennt** ("getrennt")</span><span class="sxs-lookup"><span data-stu-id="e2a03-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="e2a03-171">**Verbindung** wird hergestellt ("Verbindung wird hergestellt")</span><span class="sxs-lookup"><span data-stu-id="e2a03-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="e2a03-172">**Verbindung wird wieder hergestellt** ("Verbindung wird wieder hergestellt")</span><span class="sxs-lookup"><span data-stu-id="e2a03-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2a03-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="e2a03-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-176">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwscope**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-177">Persistenztyp der Verbindung, die zum Herstellen einer Verbindung mit dem Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2a03-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="e2a03-178">**Aktuelle Verbindung** ("aktuelle Verbindung")</span><span class="sxs-lookup"><span data-stu-id="e2a03-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="e2a03-179">**Persistente Verbindung** ("persistente Verbindung")</span><span class="sxs-lookup"><span data-stu-id="e2a03-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2a03-180">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2a03-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-183">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e2a03-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-184">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e2a03-184">A textual description of the object.</span></span>

<span data-ttu-id="e2a03-185">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-186">**Display Type**</span><span class="sxs-lookup"><span data-stu-id="e2a03-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-189">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwdisplaytype**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-190">Das Netzwerk Objekt sollte auf einer Benutzeroberfläche für das Netzwerk durchsuchen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e2a03-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="e2a03-191">**Domäne** ("Domäne")</span><span class="sxs-lookup"><span data-stu-id="e2a03-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="e2a03-192">**Generisch** ("generisch")</span><span class="sxs-lookup"><span data-stu-id="e2a03-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="e2a03-193">**Server** ("Server")</span><span class="sxs-lookup"><span data-stu-id="e2a03-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="e2a03-194">**Freigabe** ("freigeben")</span><span class="sxs-lookup"><span data-stu-id="e2a03-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2a03-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e2a03-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-196">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2a03-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-198">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="e2a03-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-199">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e2a03-199">Indicates when the object was installed.</span></span> <span data-ttu-id="e2a03-200">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2a03-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e2a03-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-202">**LocalName**</span><span class="sxs-lookup"><span data-stu-id="e2a03-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-205">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lplocalname**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-206">Lokaler Name des verbundenen Netzwerkgeräts.</span><span class="sxs-lookup"><span data-stu-id="e2a03-206">Local name of the connected network device.</span></span>

<span data-ttu-id="e2a03-207">Beispiel: "c: \\ Public"</span><span class="sxs-lookup"><span data-stu-id="e2a03-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-208">**Name**</span><span class="sxs-lookup"><span data-stu-id="e2a03-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-211">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span><span class="sxs-lookup"><span data-stu-id="e2a03-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-212">Der Name der aktuellen Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="e2a03-212">Name of the current network connection.</span></span> <span data-ttu-id="e2a03-213">Dabei handelt es sich um die Kombination der Werte in **Remotename** und **localname**.</span><span class="sxs-lookup"><span data-stu-id="e2a03-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="e2a03-214">Beispiel: " \\ \\ ntrelease (c: \\ Public)"</span><span class="sxs-lookup"><span data-stu-id="e2a03-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-215">**Persistent**</span><span class="sxs-lookup"><span data-stu-id="e2a03-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-216">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e2a03-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-218">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Functions \| [**wnettenumschlag**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span><span class="sxs-lookup"><span data-stu-id="e2a03-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-219">Die Verbindung wird vom Betriebssystem bei der nächsten Anmeldung automatisch wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="e2a03-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-223">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpprovider**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-224">Der Name des Anbieters, der Besitzer der Ressource ist.</span><span class="sxs-lookup"><span data-stu-id="e2a03-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="e2a03-225">Diese Eigenschaft kann **null** sein, wenn der Anbieter Name unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e2a03-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-226">**Remote Name**</span><span class="sxs-lookup"><span data-stu-id="e2a03-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-229">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpremutename**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-230">Der Name der Remote Netzwerkressource für eine Netzwerkressource.</span><span class="sxs-lookup"><span data-stu-id="e2a03-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="e2a03-231">Bei einer aktuellen oder permanenten Verbindung enthält **Remotename** den Netzwerknamen, der dem Namen des Werts in der **localname** -Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e2a03-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="e2a03-232">Der Name in **Remotename** muss den Benennungs Konventionen des Netzwerk Anbieters entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="e2a03-233">Beispiel: " \\ \\ ntrelease"</span><span class="sxs-lookup"><span data-stu-id="e2a03-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-234">**RemotePath**</span><span class="sxs-lookup"><span data-stu-id="e2a03-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-235">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-237">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **lpremutename**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-238">Vollständiger Pfad zur Netzwerkressource.</span><span class="sxs-lookup"><span data-stu-id="e2a03-238">Full path to the network resource.</span></span>

<span data-ttu-id="e2a03-239">Beispiel: " \\ \\ infosrv1 \\ Public"</span><span class="sxs-lookup"><span data-stu-id="e2a03-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="e2a03-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="e2a03-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-243">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Structures \| [**nettresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **dwType**")</span><span class="sxs-lookup"><span data-stu-id="e2a03-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-244">Der Typ der Ressource, die aufgelistet oder mit der eine Verbindung hergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="e2a03-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="e2a03-245">Daten **Träger ("** Datenträger")</span><span class="sxs-lookup"><span data-stu-id="e2a03-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="e2a03-246">**Print** ("Print")</span><span class="sxs-lookup"><span data-stu-id="e2a03-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="e2a03-247">**Any** ("beliebig")</span><span class="sxs-lookup"><span data-stu-id="e2a03-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2a03-248">**Status**</span><span class="sxs-lookup"><span data-stu-id="e2a03-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-251">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e2a03-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-252">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="e2a03-253">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e2a03-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e2a03-254">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2a03-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e2a03-255">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="e2a03-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e2a03-256">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2a03-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e2a03-257">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e2a03-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e2a03-258">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="e2a03-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e2a03-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e2a03-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e2a03-260">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="e2a03-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e2a03-261">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e2a03-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e2a03-262">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="e2a03-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e2a03-263">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="e2a03-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e2a03-264">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="e2a03-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e2a03-265">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e2a03-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e2a03-266">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="e2a03-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e2a03-267">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="e2a03-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e2a03-268">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="e2a03-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e2a03-269">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="e2a03-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e2a03-270">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="e2a03-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e2a03-271">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="e2a03-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e2a03-272">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="e2a03-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e2a03-273">**UserName**</span><span class="sxs-lookup"><span data-stu-id="e2a03-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2a03-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e2a03-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e2a03-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2a03-276">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Networking Functions \| [**wnetgetuser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span><span class="sxs-lookup"><span data-stu-id="e2a03-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="e2a03-277">Der Benutzername oder der Standardbenutzer Name, der verwendet wird, um eine Netzwerkverbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="e2a03-278">Beispiel: "System"</span><span class="sxs-lookup"><span data-stu-id="e2a03-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2a03-279">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2a03-279">Remarks</span></span>

<span data-ttu-id="e2a03-280">Die **Win32- \_ Network Connection** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e2a03-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e2a03-281">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2a03-281">Examples</span></span>

<span data-ttu-id="e2a03-282">Im folgenden VBScript-Codebeispiel werden Informationen über die lokale Netzwerkverbindung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="e2a03-283">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2a03-283">Requirements</span></span>



| <span data-ttu-id="e2a03-284">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2a03-284">Requirement</span></span> | <span data-ttu-id="e2a03-285">Wert</span><span class="sxs-lookup"><span data-stu-id="e2a03-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a03-286">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2a03-286">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a03-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2a03-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2a03-288">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2a03-288">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a03-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2a03-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2a03-290">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2a03-290">Namespace</span></span><br/>                | <span data-ttu-id="e2a03-291">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e2a03-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2a03-292">MOF</span><span class="sxs-lookup"><span data-stu-id="e2a03-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2a03-293"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e2a03-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2a03-294">DLL</span><span class="sxs-lookup"><span data-stu-id="e2a03-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2a03-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2a03-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a03-296">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a03-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a03-297">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="e2a03-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="e2a03-298">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="e2a03-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
