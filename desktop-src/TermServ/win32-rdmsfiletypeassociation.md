---
title: Win32_RDMSFileTypeAssociation-Klasse
description: Verwaltet eine Dateityp Zuordnung für eine veröffentlichte Anwendung.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSFileTypeAssociation-Klasse Remotedesktopdienste
- Win32_RDMSFileTypeAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391565"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="f3d62-105">Win32 \_ rdmsfiletypeassociation-Klasse</span><span class="sxs-lookup"><span data-stu-id="f3d62-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="f3d62-106">Verwaltet eine Dateityp Zuordnung für eine veröffentlichte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f3d62-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="f3d62-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3d62-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d62-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d62-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="f3d62-109">Member</span><span class="sxs-lookup"><span data-stu-id="f3d62-109">Members</span></span>

<span data-ttu-id="f3d62-110">Die **Win32 \_ rdmsfiletypeassociation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f3d62-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="f3d62-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3d62-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3d62-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3d62-112">Properties</span></span>

<span data-ttu-id="f3d62-113">Die **Win32 \_ rdmsfiletypeassociation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f3d62-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3d62-114">**Appalias**</span><span class="sxs-lookup"><span data-stu-id="f3d62-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3d62-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3d62-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-118">Ruft den Alias der Anwendung ab, die dem Dateityp zugeordnet ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-119">**Extname**</span><span class="sxs-lookup"><span data-stu-id="f3d62-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3d62-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3d62-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3d62-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-123">Ruft den Namen der Dateierweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="f3d62-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-124">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="f3d62-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-125">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="f3d62-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-127">Ruft den Inhalt des Symbols für den Dateityp ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="f3d62-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3d62-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-131">Ruft den Index für das Symbol für den Dateityp ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="f3d62-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3d62-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-135">Ruft den Pfad zum Symbol für den Dateityp ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-136">**Isprimaryhandler**</span><span class="sxs-lookup"><span data-stu-id="f3d62-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f3d62-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-139">Ruft einen Wert ab, der angibt, ob die Dateityp Zuordnung für den primären Handler gilt, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="f3d62-140">**True** , wenn die Dateityp Zuordnung für den primären Handler gilt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f3d62-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="f3d62-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f3d62-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-144">Gibt an, ob dieses freigegebene</span><span class="sxs-lookup"><span data-stu-id="f3d62-144">Whether this FTA is published.</span></span>

<span data-ttu-id="f3d62-145">Ruft einen Wert ab, der angibt, ob die Dateityp Zuordnung veröffentlicht wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="f3d62-146">**True** , wenn die Dateityp Zuordnung veröffentlicht wird. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="f3d62-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-147">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="f3d62-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3d62-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-149">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3d62-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-150">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3d62-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-151">Ruft den Namen des Anwendungs Pools für die Dateityp Zuordnung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f3d62-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="f3d62-152">**Progidhint**</span><span class="sxs-lookup"><span data-stu-id="f3d62-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3d62-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f3d62-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3d62-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3d62-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3d62-155">Ruft einen Hinweis ab, der Benutzern beim Öffnen der Dateierweiterung behilflich ist.</span><span class="sxs-lookup"><span data-stu-id="f3d62-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3d62-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3d62-156">Requirements</span></span>



| <span data-ttu-id="f3d62-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3d62-157">Requirement</span></span> | <span data-ttu-id="f3d62-158">Wert</span><span class="sxs-lookup"><span data-stu-id="f3d62-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d62-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3d62-159">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d62-160">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f3d62-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f3d62-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3d62-161">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d62-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3d62-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f3d62-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3d62-163">Namespace</span></span><br/>                | <span data-ttu-id="f3d62-164">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="f3d62-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f3d62-165">MOF</span><span class="sxs-lookup"><span data-stu-id="f3d62-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3d62-166"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f3d62-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3d62-167">DLL</span><span class="sxs-lookup"><span data-stu-id="f3d62-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3d62-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3d62-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f3d62-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3d62-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d62-170">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="f3d62-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

