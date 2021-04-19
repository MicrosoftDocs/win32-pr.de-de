---
description: Die msilockpermissionsex-Tabelle kann verwendet werden, um Dienste, Dateien, Registrierungsschlüssel und erstellte Ordner zu sichern.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Msilockpermissionsex-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373273"
---
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="06ae8-103">Msilockpermissionsex-Tabelle</span><span class="sxs-lookup"><span data-stu-id="06ae8-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="06ae8-104">Die msilockpermissionsex-Tabelle kann verwendet werden, um Dienste, Dateien, Registrierungsschlüssel und erstellte Ordner zu sichern.</span><span class="sxs-lookup"><span data-stu-id="06ae8-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="06ae8-105">Ein Paket sollte nicht sowohl die msilockpermissionsex-Tabelle als auch die [lockberechtigungs Tabelle](lockpermissions-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="06ae8-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="06ae8-106">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06ae8-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="06ae8-107">Diese Tabelle wird für Pakete empfohlen, die für die Installation mit Windows Installer 5,0 oder höher vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="06ae8-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="06ae8-108">Die msilockpermissionsex-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="06ae8-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="06ae8-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="06ae8-109">Column</span></span>               | <span data-ttu-id="06ae8-110">Typ</span><span class="sxs-lookup"><span data-stu-id="06ae8-110">Type</span></span>                                       | <span data-ttu-id="06ae8-111">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="06ae8-111">Key</span></span> | <span data-ttu-id="06ae8-112">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="06ae8-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="06ae8-113">Msilockpermissionsex</span><span class="sxs-lookup"><span data-stu-id="06ae8-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="06ae8-114">Text</span><span class="sxs-lookup"><span data-stu-id="06ae8-114">Text</span></span>](text.md)                           | <span data-ttu-id="06ae8-115">J</span><span class="sxs-lookup"><span data-stu-id="06ae8-115">Y</span></span>   | <span data-ttu-id="06ae8-116">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-116">N</span></span>        |
| <span data-ttu-id="06ae8-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="06ae8-117">LockObject</span></span>           | [<span data-ttu-id="06ae8-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="06ae8-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="06ae8-119">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-119">N</span></span>   | <span data-ttu-id="06ae8-120">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-120">N</span></span>        |
| <span data-ttu-id="06ae8-121">Tabelle</span><span class="sxs-lookup"><span data-stu-id="06ae8-121">Table</span></span>                | [<span data-ttu-id="06ae8-122">Text</span><span class="sxs-lookup"><span data-stu-id="06ae8-122">Text</span></span>](text.md)                           | <span data-ttu-id="06ae8-123">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-123">N</span></span>   | <span data-ttu-id="06ae8-124">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-124">N</span></span>        |
| <span data-ttu-id="06ae8-125">Sddltext</span><span class="sxs-lookup"><span data-stu-id="06ae8-125">SDDLText</span></span>             | [<span data-ttu-id="06ae8-126">Formattedsddltext</span><span class="sxs-lookup"><span data-stu-id="06ae8-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="06ae8-127">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-127">N</span></span>   | <span data-ttu-id="06ae8-128">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-128">N</span></span>        |
| <span data-ttu-id="06ae8-129">Bedingung</span><span class="sxs-lookup"><span data-stu-id="06ae8-129">Condition</span></span>            | [<span data-ttu-id="06ae8-130">Condition</span><span class="sxs-lookup"><span data-stu-id="06ae8-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="06ae8-131">N</span><span class="sxs-lookup"><span data-stu-id="06ae8-131">N</span></span>   | <span data-ttu-id="06ae8-132">J</span><span class="sxs-lookup"><span data-stu-id="06ae8-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="06ae8-133">Spalten</span><span class="sxs-lookup"><span data-stu-id="06ae8-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="06ae8-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>Msilockpermissionsex</span><span class="sxs-lookup"><span data-stu-id="06ae8-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="06ae8-135">Dies ist der Primärschlüssel dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="06ae8-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="06ae8-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="06ae8-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="06ae8-137">In dieser Spalte und in der Tabellenspalte werden die Datei, das Verzeichnis, der Registrierungsschlüssel oder der Dienst angegeben, der gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06ae8-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="06ae8-138">Die LockObject-Spalte ist ein Fremdschlüssel, der auf den Primärschlüssel der Tabelle verweist, die in der Tabellenspalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="06ae8-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="06ae8-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Glaub</span><span class="sxs-lookup"><span data-stu-id="06ae8-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="06ae8-140">In dieser Spalte und der Spalte lockobject werden die Datei, das Verzeichnis, der Registrierungsschlüssel oder der Dienst angegeben, der gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06ae8-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="06ae8-141">Geben Sie in der Spalte Tabelle den Eintrag File, Registry, kreatefolder oder ServiceInstall ein, um ein lockobject anzugeben, das in der [Dateitabelle](file-table.md), in der [Registrierungs Tabelle](registry-table.md), in der [Tabelle](createfolder-table.md)mit den Tabellen oder in der Tabelle " [ServiceInstall](serviceinstall-table.md)" aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="06ae8-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="06ae8-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>Sddltext</span><span class="sxs-lookup"><span data-stu-id="06ae8-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="06ae8-143">Geben Sie die SDDL-Zeichenfolge ein, um die Berechtigungen für das ausgewählte Objekt anzugeben.</span><span class="sxs-lookup"><span data-stu-id="06ae8-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="06ae8-144">Die SDDL muss im Format der [Sicherheits Deskriptor-Zeichenfolge](../secauthz/security-descriptor-string-format.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06ae8-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="06ae8-145">Dies unterstützt keine privaten oder öffentlichen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="06ae8-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="06ae8-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="06ae8-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="06ae8-147">Diese Spalte enthält einen bedingten Ausdruck, der verwendet wird, um zu bestimmen, ob die angegebene Berechtigung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="06ae8-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="06ae8-148">Wenn die Bedingung zu **false** ausgewertet wird, wird die Berechtigung nicht angewendet.</span><span class="sxs-lookup"><span data-stu-id="06ae8-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="06ae8-149">Wenn die Bedingung als **true** ausgewertet wird, wird die Berechtigung angewendet.</span><span class="sxs-lookup"><span data-stu-id="06ae8-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06ae8-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06ae8-150">Remarks</span></span>

<span data-ttu-id="06ae8-151">Weitere Informationen zum Sichern von Diensten, Dateien, Registrierungs Schlüsseln und erstellten Ordnern finden Sie unter [Sichern von Ressourcen](securing-resources-.md).</span><span class="sxs-lookup"><span data-stu-id="06ae8-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="06ae8-152">Verwenden Sie die msilockpermissionsex-Tabelle, um Objekte für ein Benutzerkonto zu sichern, das während der Installation erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="06ae8-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="06ae8-153">Das Benutzerkonto muss bereits vorhanden sein, wenn das Objekt durch die Installation gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="06ae8-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="06ae8-154">Erstellen Sie das Benutzerkonto, bevor Sie die zu sichernden Dateien, Registrierungsschlüssel, Ordner oder Dienste installieren.</span><span class="sxs-lookup"><span data-stu-id="06ae8-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="06ae8-155">Wenn ein lockobject-und Tabellen Paar in dieser Tabelle über mehr als einen Bedingungs Ausdruck verfügt, der als true ausgewertet wird, schlägt die Installation fehl, und Windows Installer gibt eine Fehlermeldung 1942 zurück.</span><span class="sxs-lookup"><span data-stu-id="06ae8-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="06ae8-156">Wenn die [formattedsddltext](formattedsddltext.md) -Zeichenfolge im sddltext-Feld nicht in eine gültige SDDL-Zeichenfolge aufgelöst werden kann, schlägt die Installation fehl, und Windows Installer gibt eine Fehlermeldung 1943 zurück.</span><span class="sxs-lookup"><span data-stu-id="06ae8-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="06ae8-157">Wenn der Benutzer nicht über ausreichende Berechtigungen verfügt, um die vom sddltext-Feld angegebene Sicherheits Beschreibung für eine Datei oder einen Ordner festzulegen, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1926 zurück.</span><span class="sxs-lookup"><span data-stu-id="06ae8-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="06ae8-158">Wenn der Benutzer nicht über ausreichende Berechtigungen zum Festlegen der Sicherheits Beschreibung verfügt, die im Feld sddltext eines Registrierungsschlüssels angegeben ist, tritt bei der Installation ein Fehler auf, und Windows Installer gibt die Fehlermeldung 1401 zurück.</span><span class="sxs-lookup"><span data-stu-id="06ae8-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="06ae8-159">Wenn der Benutzer nicht über ausreichende Berechtigungen zum Festlegen der vom sddltext-Feld für einen Dienst angegebenen Sicherheits Beschreibung verfügt, schlägt die Installation fehl, und Windows Installer gibt die Fehlermeldung 1944 zurück.</span><span class="sxs-lookup"><span data-stu-id="06ae8-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="06ae8-160">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="06ae8-160">Validation</span></span>

<dl>

[<span data-ttu-id="06ae8-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="06ae8-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="06ae8-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="06ae8-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="06ae8-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="06ae8-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
