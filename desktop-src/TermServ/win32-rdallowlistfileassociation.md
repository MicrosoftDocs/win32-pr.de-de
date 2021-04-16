---
title: Win32_RDAllowListFileAssociation-Klasse
description: Beschreibt eine veröffentlichte Dateityp Zuordnung zu einer RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Win32_RDAllowListFileAssociation-Klasse Remotedesktopdienste
- Win32_RDAllowListFileAssociation Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476698"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="4d69a-105">Win32 \_ rdallowlistfileassociation-Klasse</span><span class="sxs-lookup"><span data-stu-id="4d69a-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="4d69a-106">Beschreibt eine veröffentlichte Dateityp Zuordnung zu einer RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="4d69a-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="4d69a-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d69a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d69a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d69a-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="4d69a-109">Member</span><span class="sxs-lookup"><span data-stu-id="4d69a-109">Members</span></span>

<span data-ttu-id="4d69a-110">Die **Win32 \_ rdallowlistfileassociation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d69a-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="4d69a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d69a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d69a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4d69a-112">Properties</span></span>

<span data-ttu-id="4d69a-113">Die **Win32 \_ rdallowlistfileassociation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4d69a-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d69a-114">**Appalias**</span><span class="sxs-lookup"><span data-stu-id="4d69a-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4d69a-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-117">Alias der RemoteApp, die der Erweiterung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4d69a-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-118">**Extname**</span><span class="sxs-lookup"><span data-stu-id="4d69a-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4d69a-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-121">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="4d69a-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-122">Name der Erweiterung, z. b. ". txt".</span><span class="sxs-lookup"><span data-stu-id="4d69a-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="4d69a-123">**Progidhint**</span><span class="sxs-lookup"><span data-stu-id="4d69a-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d69a-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4d69a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d69a-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4d69a-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4d69a-126">Hinweis zum Öffnen von Dokumenten mit dieser Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="4d69a-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d69a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d69a-127">Requirements</span></span>



| <span data-ttu-id="4d69a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d69a-128">Requirement</span></span> | <span data-ttu-id="4d69a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="4d69a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d69a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d69a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4d69a-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d69a-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4d69a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d69a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4d69a-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d69a-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="4d69a-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d69a-134">Namespace</span></span><br/>                | <span data-ttu-id="4d69a-135">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4d69a-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4d69a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="4d69a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d69a-137"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4d69a-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="4d69a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4d69a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d69a-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d69a-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





