---
title: Win32_RDFileAssociation-Klasse
description: Stellt eine Dateityp Zuordnung für eine RemoteApp dar.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Win32_RDFileAssociation-Klasse Remotedesktopdienste
- Win32_RDFileAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949741"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="6edaa-105">Win32 \_ rdfileassociation-Klasse</span><span class="sxs-lookup"><span data-stu-id="6edaa-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="6edaa-106">Stellt eine Dateityp Zuordnung für eine RemoteApp dar.</span><span class="sxs-lookup"><span data-stu-id="6edaa-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="6edaa-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6edaa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edaa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6edaa-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="6edaa-109">Member</span><span class="sxs-lookup"><span data-stu-id="6edaa-109">Members</span></span>

<span data-ttu-id="6edaa-110">Die **Win32 \_ rdfileassociation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6edaa-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="6edaa-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6edaa-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6edaa-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6edaa-112">Properties</span></span>

<span data-ttu-id="6edaa-113">Die **Win32 \_ rdfileassociation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6edaa-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6edaa-114">**Extname**</span><span class="sxs-lookup"><span data-stu-id="6edaa-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6edaa-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6edaa-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-117">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="6edaa-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6edaa-118">Der Name der Dateinamenerweiterung, z. b. txt.</span><span class="sxs-lookup"><span data-stu-id="6edaa-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="6edaa-119">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="6edaa-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6edaa-120">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="6edaa-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6edaa-122">Der Inhalt des Symbols für diese Datei Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6edaa-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="6edaa-123">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="6edaa-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6edaa-124">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6edaa-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6edaa-126">Der Index des Symbols in der Datei.</span><span class="sxs-lookup"><span data-stu-id="6edaa-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="6edaa-127">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="6edaa-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6edaa-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6edaa-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6edaa-130">Der Dateipfad zum Symbol für diese Datei Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="6edaa-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="6edaa-131">**Primaryhandler**</span><span class="sxs-lookup"><span data-stu-id="6edaa-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6edaa-132">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6edaa-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6edaa-134">Gibt an, ob diese Zuordnung für einen primären Handler gilt.</span><span class="sxs-lookup"><span data-stu-id="6edaa-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="6edaa-135">**Progidhint**</span><span class="sxs-lookup"><span data-stu-id="6edaa-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6edaa-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6edaa-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6edaa-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6edaa-138">Der Hinweis, dass Dokumente mit dieser Datei Zuordnung geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="6edaa-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6edaa-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6edaa-139">Requirements</span></span>



| <span data-ttu-id="6edaa-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6edaa-140">Requirement</span></span> | <span data-ttu-id="6edaa-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6edaa-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6edaa-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6edaa-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6edaa-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6edaa-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6edaa-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6edaa-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6edaa-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6edaa-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="6edaa-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="6edaa-146">Namespace</span></span><br/>                | <span data-ttu-id="6edaa-147">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6edaa-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6edaa-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6edaa-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6edaa-149"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6edaa-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6edaa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6edaa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6edaa-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6edaa-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





