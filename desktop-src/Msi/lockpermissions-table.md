---
description: Wird verwendet, um einzelne Teile einer Anwendung in einer gesperrten Umgebung zu sichern. Sie kann mit der Installation von Dateien, Registrierungs Schlüsseln und erstellten Ordnern verwendet werden.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Lockberechtigungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350208"
---
# <a name="lockpermissions-table"></a><span data-ttu-id="216a8-104">Lockberechtigungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="216a8-104">LockPermissions Table</span></span>

<span data-ttu-id="216a8-105">Die lockberechtigungs-Tabelle wird verwendet, um einzelne Teile einer Anwendung in einer gesperrten Umgebung zu sichern.</span><span class="sxs-lookup"><span data-stu-id="216a8-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="216a8-106">Sie kann mit der Installation von Dateien, Registrierungs Schlüsseln und erstellten Ordnern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="216a8-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="216a8-107">Ein Paket, das für die Installation in Windows Server 2008 R2 oder Windows 7 vorgesehen ist, sollte die Tabelle " [msilockpermissionsex](msilockpermissionsex-table.md) " anstelle der Tabelle "lockberechtigungs Tabelle" verwenden.</span><span class="sxs-lookup"><span data-stu-id="216a8-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="216a8-108">In Windows Installer Versionen vor Windows Installer 5,0 wird die Tabelle "msilockpermissionsex" ignoriert.</span><span class="sxs-lookup"><span data-stu-id="216a8-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="216a8-109">Windows Installer 5,0 kann ein-Paket installieren, das die lockberechtigungs-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="216a8-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="216a8-110">Ab Windows Installer 5,0 tritt bei der Installation eines Pakets, das sowohl die msilockpermissionsex-Tabelle als auch die lockberechtigungs Tabelle enthält, ein Fehler auf, und die Fehlermeldung 1941 wird Windows Installer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="216a8-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="216a8-111">Die lockberechtigungs-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="216a8-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="216a8-112">Spalte</span><span class="sxs-lookup"><span data-stu-id="216a8-112">Column</span></span>     | <span data-ttu-id="216a8-113">Typ</span><span class="sxs-lookup"><span data-stu-id="216a8-113">Type</span></span>                               | <span data-ttu-id="216a8-114">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="216a8-114">Key</span></span> | <span data-ttu-id="216a8-115">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="216a8-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="216a8-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="216a8-116">LockObject</span></span> | [<span data-ttu-id="216a8-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="216a8-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="216a8-118">J</span><span class="sxs-lookup"><span data-stu-id="216a8-118">Y</span></span>   | <span data-ttu-id="216a8-119">N</span><span class="sxs-lookup"><span data-stu-id="216a8-119">N</span></span>        |
| <span data-ttu-id="216a8-120">Tabelle</span><span class="sxs-lookup"><span data-stu-id="216a8-120">Table</span></span>      | [<span data-ttu-id="216a8-121">Text</span><span class="sxs-lookup"><span data-stu-id="216a8-121">Text</span></span>](text.md)                   | <span data-ttu-id="216a8-122">J</span><span class="sxs-lookup"><span data-stu-id="216a8-122">Y</span></span>   | <span data-ttu-id="216a8-123">N</span><span class="sxs-lookup"><span data-stu-id="216a8-123">N</span></span>        |
| <span data-ttu-id="216a8-124">Domain</span><span class="sxs-lookup"><span data-stu-id="216a8-124">Domain</span></span>     | [<span data-ttu-id="216a8-125">Großformatige</span><span class="sxs-lookup"><span data-stu-id="216a8-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="216a8-126">J</span><span class="sxs-lookup"><span data-stu-id="216a8-126">Y</span></span>   | <span data-ttu-id="216a8-127">J</span><span class="sxs-lookup"><span data-stu-id="216a8-127">Y</span></span>        |
| <span data-ttu-id="216a8-128">Benutzer</span><span class="sxs-lookup"><span data-stu-id="216a8-128">User</span></span>       | [<span data-ttu-id="216a8-129">Großformatige</span><span class="sxs-lookup"><span data-stu-id="216a8-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="216a8-130">J</span><span class="sxs-lookup"><span data-stu-id="216a8-130">Y</span></span>   | <span data-ttu-id="216a8-131">N</span><span class="sxs-lookup"><span data-stu-id="216a8-131">N</span></span>        |
| <span data-ttu-id="216a8-132">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="216a8-132">Permission</span></span> | [<span data-ttu-id="216a8-133">Doubleiteger</span><span class="sxs-lookup"><span data-stu-id="216a8-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="216a8-134">N</span><span class="sxs-lookup"><span data-stu-id="216a8-134">N</span></span>   | <span data-ttu-id="216a8-135">J</span><span class="sxs-lookup"><span data-stu-id="216a8-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="216a8-136">Spalten</span><span class="sxs-lookup"><span data-stu-id="216a8-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="216a8-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="216a8-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="216a8-138">In dieser Spalte und der Tabellenspalte werden die Datei, das Verzeichnis oder der Registrierungsschlüssel angegeben, die gesichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="216a8-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="216a8-139">Die LockObject-Spalte ist ein Fremdschlüssel, der auf den Primärschlüssel der Tabelle verweist, die in der Tabellenspalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="216a8-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="216a8-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="216a8-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="216a8-141">In dieser Spalte und der Spalte lockobject wird die Datei, das Verzeichnis oder der Registrierungsschlüssel angegeben, die gesichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="216a8-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="216a8-142">Geben Sie in der Spalte Tabelle den Eintrag File, Registry oder Up Folder ein, um ein lockobject anzugeben, das in der [Dateitabelle](file-table.md), der [Registrierungs Tabelle](registry-table.md)oder der [Tabelle](createfolder-table.md)"Tabelle" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="216a8-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="216a8-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>-</span><span class="sxs-lookup"><span data-stu-id="216a8-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="216a8-144">Die Spalte, die die Domäne des Benutzers identifiziert, für den Berechtigungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="216a8-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="216a8-145">Dies ist der Name eines eigenständigen Computers oder eines Domänen Namens.</span><span class="sxs-lookup"><span data-stu-id="216a8-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="216a8-146">Der Spaltendatentyp ist [formatiert](formatted.md), und Sie können die Zeichenfolge \[ % UserDomain \] in diesem Feld verwenden, um den Wert der User Domain-Umgebungsvariablen für die aktuelle Domäne zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="216a8-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="216a8-147">Zum erhalten einer anderen Domäne müssen [benutzerdefinierte Aktionen](custom-actions.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="216a8-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="216a8-148">Weitere Informationen finden Sie in der benutzerdefinierten Aktionstabelle.</span><span class="sxs-lookup"><span data-stu-id="216a8-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="216a8-149"><span id="User"></span><span id="user"></span><span id="USER"></span>Bedienungs</span><span class="sxs-lookup"><span data-stu-id="216a8-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="216a8-150">Die Spalte, die den lokalisierten Namen des Benutzers identifiziert, für den Berechtigungen festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="216a8-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="216a8-151">Dieser Name muss sich auf dem Computer oder in der Domäne befinden.</span><span class="sxs-lookup"><span data-stu-id="216a8-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="216a8-152">Die Installation schlägt fehl, wenn der Computer oder der Domänen Controller die Kombination aus Domäne und Benutzer nicht erkennt oder wenn die Sicherheits-ID (SID) des Benutzers nicht abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="216a8-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="216a8-153">Es können mehrere Benutzer für ein einzelnes lockobject angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="216a8-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="216a8-154">Die allgemeinen Benutzernamen "jeder" und "Administratoren" können in englischer Sprache eingegeben werden und werden bekannten SIDs zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="216a8-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="216a8-155">"LocalSystem" erhält Vollzugriff in allen Sicherheits Deskriptoren, die über die lockberechtigungtabelle erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="216a8-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="216a8-156">Sie können den aktuellen Benutzer mit der Eigenschaft " [**Computername**](computername.md)", der Eigenschaft " [**LogonUser**](logonuser.md) " oder der [**username**](username.md) -Eigenschaft in diesem Feld erhalten.</span><span class="sxs-lookup"><span data-stu-id="216a8-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="216a8-157">Eine benutzerdefinierte Aktion ist erforderlich, um den lokalisierten Namen eines beliebigen Benutzers oder einer Gruppe einzugeben.</span><span class="sxs-lookup"><span data-stu-id="216a8-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="216a8-158">Sie können mehrere Datensätze mit identischen lockobject-und Table-Einträgen (aber unterschiedlichen Benutzer Einträgen) verwenden, um Zugriffs Steuerungs Listen für mehrere Benutzer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="216a8-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="216a8-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Berechtigung</span><span class="sxs-lookup"><span data-stu-id="216a8-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="216a8-160">Die Spalte, die die ganzzahlige Beschreibung der System Privilegien identifiziert.</span><span class="sxs-lookup"><span data-stu-id="216a8-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="216a8-161">Im folgenden finden Sie die am häufigsten verwendeten Werte (eine komplette Liste ist in "Winnt. h" vorhanden).</span><span class="sxs-lookup"><span data-stu-id="216a8-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="216a8-162">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="216a8-162">Privilege</span></span>                                                              | <span data-ttu-id="216a8-163">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="216a8-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="216a8-164">generisch \_ alle</span><span class="sxs-lookup"><span data-stu-id="216a8-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="216a8-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="216a8-165">0X10000000</span></span><br/> <span data-ttu-id="216a8-166">268435456</span><span class="sxs-lookup"><span data-stu-id="216a8-166">268435456</span></span><br/>     | <span data-ttu-id="216a8-167">Lese-, Schreib-und Ausführungs Zugriff</span><span class="sxs-lookup"><span data-stu-id="216a8-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="216a8-168">generisch \_ Ausführen</span><span class="sxs-lookup"><span data-stu-id="216a8-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="216a8-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="216a8-169">0X20000000</span></span><br/> <span data-ttu-id="216a8-170">536870912</span><span class="sxs-lookup"><span data-stu-id="216a8-170">536870912</span></span><br/> | <span data-ttu-id="216a8-171">Zugriff ausführen</span><span class="sxs-lookup"><span data-stu-id="216a8-171">Execute access</span></span>                  |
| <span data-ttu-id="216a8-172">generischer \_ Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="216a8-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="216a8-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="216a8-173">0X40000000</span></span><br/> <span data-ttu-id="216a8-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="216a8-174">1073741824</span></span><br/>  | <span data-ttu-id="216a8-175">Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="216a8-175">Write access</span></span>                    |



 

<span data-ttu-id="216a8-176">Sie können \_ in der Berechtigungs Spalte keinen generischen Lesevorgang angeben.</span><span class="sxs-lookup"><span data-stu-id="216a8-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="216a8-177">Der Versuch, dies zu tun, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="216a8-177">Attempting to do so will fail.</span></span> <span data-ttu-id="216a8-178">Stattdessen müssen Sie einen Wert angeben, z. b \_ . den Schlüssel Lesevorgang oder den \_ allgemeinen Datei Lesevorgang \_ .</span><span class="sxs-lookup"><span data-stu-id="216a8-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="216a8-179">In diese Spalte eingegebene NULL ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="216a8-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="216a8-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="216a8-180">Remarks</span></span>

<span data-ttu-id="216a8-181">Die Informationen in dieser Tabelle werden in den Aktionen [InstallFiles](installfiles-action.md), [schreiteregistryvalues](writeregistryvalues-action.md)und [kreatefolders](createfolders-action.md) in [*Sequenz Tabellen*](s-gly.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="216a8-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="216a8-182">Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="216a8-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="216a8-183">Die Berechtigung kann nur für Benutzer festgelegt werden, die bereits auf dem Computer oder in der Domäne vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="216a8-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="216a8-184">Der Versuch, Berechtigungen für einen unbekannten Benutzer festzulegen, bewirkt, dass die Installation fehlschlägt, auch wenn dieses Benutzerkonto während der Installation durch eine verzögerte benutzerdefinierte Aktion erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="216a8-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="216a8-185">Es wird empfohlen, dass die lokale Gruppe des Systemadministrators in allen Zugriffs Steuerungs Listen (Access Control Lists, ACL) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="216a8-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="216a8-186">Dadurch wird sichergestellt, dass der Systemadministrator auf Objekte zugreifen und Sie verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="216a8-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="216a8-187">Alle Dateien, Registrierungsschlüssel oder Verzeichnisse, die in der Tabelle lockberechtigungs Tabelle aufgeführt sind, erhalten eine explizite Sicherheits Beschreibung, unabhängig davon, ob ein vorhandenes Objekt ersetzt wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="216a8-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="216a8-188">Der Windows Installer versucht, die Sicherheit von Objekten beizubehalten, die bereits im System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="216a8-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="216a8-189">Wenn ein Objekt nicht in der Tabelle lockberechtigungs Tabelle aufgeführt ist und ein vorhandenes Objekt ersetzt, ruft der Austausch die Sicherheitseinstellungen des Objekts ab, das es ersetzt.</span><span class="sxs-lookup"><span data-stu-id="216a8-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="216a8-190">Wenn ein Objekt nicht in der Tabelle lockberechtigungs Tabelle aufgeführt ist und kein vorhandenes Objekt ersetzt, empfängt es keine explizite Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="216a8-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="216a8-191">Der Zugriff auf das neue Objekt basiert auf den Attributen des übergeordneten Objekts bzw. des Container Objekts.</span><span class="sxs-lookup"><span data-stu-id="216a8-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="216a8-192">Wenn ein Objekt nicht in der Tabelle aufgeführt ist und ein Objekt ohne explizite Sicherheits Beschreibung ersetzt, basiert der Zugriff auf das neue Objekt auf den Attributen des übergeordneten Objekts bzw. des Container Objekts.</span><span class="sxs-lookup"><span data-stu-id="216a8-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="216a8-193">Der Windows Installer legt die [**UserSID**](usersid.md) -Eigenschaft auf die Sicherheits-ID (SID) oder den Benutzer fest, der die Installation durchführt.</span><span class="sxs-lookup"><span data-stu-id="216a8-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="216a8-194">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="216a8-194">Validation</span></span>

<dl>

[<span data-ttu-id="216a8-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="216a8-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="216a8-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="216a8-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="216a8-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="216a8-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="216a8-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="216a8-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




