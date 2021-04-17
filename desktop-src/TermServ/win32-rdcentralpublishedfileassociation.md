---
title: Win32_RDCentralPublishedFileAssociation-Klasse
description: Informationen für eine Dateierweiterung, die einer Anwendung zugeordnet ist.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFileAssociation-Klasse Remotedesktopdienste
- Win32_RDCentralPublishedFileAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478849"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="89bcd-105">Win32 \_ rdcentralpublishedfileassociation-Klasse</span><span class="sxs-lookup"><span data-stu-id="89bcd-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="89bcd-106">Informationen für eine Dateierweiterung, die einer Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="89bcd-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="89bcd-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89bcd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89bcd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89bcd-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="89bcd-109">Member</span><span class="sxs-lookup"><span data-stu-id="89bcd-109">Members</span></span>

<span data-ttu-id="89bcd-110">Die **Win32 \_ rdcentralpublishedfileassociation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="89bcd-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="89bcd-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89bcd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89bcd-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89bcd-112">Properties</span></span>

<span data-ttu-id="89bcd-113">Die **Win32 \_ rdcentralpublishedfileassociation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89bcd-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89bcd-114">**Appalias**</span><span class="sxs-lookup"><span data-stu-id="89bcd-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89bcd-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="89bcd-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89bcd-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89bcd-117">Alias der RemoteApp der Datei Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="89bcd-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="89bcd-118">**Extname**</span><span class="sxs-lookup"><span data-stu-id="89bcd-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89bcd-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="89bcd-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89bcd-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-121">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89bcd-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89bcd-122">Name der Erweiterung (z. b.. txt).</span><span class="sxs-lookup"><span data-stu-id="89bcd-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="89bcd-123">**Farmalias**</span><span class="sxs-lookup"><span data-stu-id="89bcd-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89bcd-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="89bcd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89bcd-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89bcd-126">Alias der RemoteApp-Farm der Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="89bcd-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="89bcd-127">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="89bcd-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89bcd-128">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="89bcd-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89bcd-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89bcd-130">Inhalt des Symbols für diese Datei Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="89bcd-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="89bcd-131">**Primaryhandler**</span><span class="sxs-lookup"><span data-stu-id="89bcd-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89bcd-132">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="89bcd-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="89bcd-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89bcd-134">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="89bcd-134">Reserved for future use.</span></span> <span data-ttu-id="89bcd-135">Wird immer " **true**" sein.</span><span class="sxs-lookup"><span data-stu-id="89bcd-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="89bcd-136">**Progidhint**</span><span class="sxs-lookup"><span data-stu-id="89bcd-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89bcd-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="89bcd-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89bcd-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="89bcd-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89bcd-139">Hinweise zum Öffnen von Dokumenten mit dieser Datei Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="89bcd-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89bcd-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89bcd-140">Requirements</span></span>



| <span data-ttu-id="89bcd-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89bcd-141">Requirement</span></span> | <span data-ttu-id="89bcd-142">Wert</span><span class="sxs-lookup"><span data-stu-id="89bcd-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89bcd-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89bcd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="89bcd-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="89bcd-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="89bcd-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89bcd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="89bcd-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89bcd-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="89bcd-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="89bcd-147">Namespace</span></span><br/>                | <span data-ttu-id="89bcd-148">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="89bcd-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="89bcd-149">MOF</span><span class="sxs-lookup"><span data-stu-id="89bcd-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89bcd-150"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="89bcd-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="89bcd-151">DLL</span><span class="sxs-lookup"><span data-stu-id="89bcd-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89bcd-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89bcd-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

