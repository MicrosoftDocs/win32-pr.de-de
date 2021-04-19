---
description: Die sourcelistaddsource-Methode fügt eine Netzwerk-oder URL-Quelle hinzu. Akzeptiert SourcePath, Type und Index als Parameter. Diese Methode ruft msisourcelistaddsourceex auf.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Patch. sourcelistaddsource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369664"
---
# <a name="patchsourcelistaddsource-method"></a><span data-ttu-id="2d615-105">Patch. sourcelistaddsource-Methode</span><span class="sxs-lookup"><span data-stu-id="2d615-105">Patch.SourceListAddSource method</span></span>

<span data-ttu-id="2d615-106">Die **sourcelistaddsource** -Methode fügt eine Netzwerk-oder URL-Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d615-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="2d615-107">Akzeptiert *SourcePath*, *Type* und *Index* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="2d615-107">Accepts *SourcePath*, *Type* and *Index* as parameters.</span></span> <span data-ttu-id="2d615-108">Diese Methode ruft [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)auf.</span><span class="sxs-lookup"><span data-stu-id="2d615-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d615-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d615-109">Syntax</span></span>


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="2d615-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d615-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d615-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="2d615-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="2d615-112">Typ der hinzu zufügenden Quelle: msisourcetype \_ Network oder msisourcetype \_ URL.</span><span class="sxs-lookup"><span data-stu-id="2d615-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="2d615-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="2d615-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="2d615-114">Der Pfad zur hinzu zufügenden Quelle.</span><span class="sxs-lookup"><span data-stu-id="2d615-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="2d615-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="2d615-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="2d615-116">Wenn **sourcelistaddsource** mit einer neuen Quelle und einem auf 0 festgelegten *Index* aufgerufen wird, fügt das Installationsprogramm die Quelle am Ende der Quell Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d615-116">If **SourceListAddSource** is called with a new source and *Index* set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="2d615-117">Wenn diese Funktion mit einer bereits in der Quell Liste vorhandenen Quelle aufgerufen wird und der *Index* auf 0 festgelegt ist, behält das Installationsprogramm den vorhandenen Index der Quelle bei.</span><span class="sxs-lookup"><span data-stu-id="2d615-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="2d615-118">Wenn die Funktion mit einer vorhandenen Quelle in der Quell Liste aufgerufen wird und der *Index* auf einen Wert ungleich 0 (null) festgelegt ist, wird die Quelle aus der aktuellen Position in der Liste entfernt und an der durch *Index* angegebenen Position eingefügt, bevor eine Quelle vorhanden ist, die an dieser Position bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2d615-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="2d615-119">Wenn die Funktion mit einer neuen Quelle aufgerufen wird und der *Index* auf einen Wert ungleich 0 (null) festgelegt ist, wird die Quelle an der durch *Index* angegebenen Position eingefügt, bevor eine Quelle vorhanden ist, die an dieser Position bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2d615-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="2d615-120">Der Indexwert für alle Quellen in der Liste nach dem durch *Index* angegebenen Index wird aktualisiert, um sicherzustellen, dass eindeutige Indexwerte und die vorhandene Reihenfolge sicher unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="2d615-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the preexisting order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="2d615-121">Wenn *Index* größer als die Anzahl der Quellen in der Liste ist, wird die Quelle am Ende der Liste mit einem Indexwert eingefügt, der größer als jede vorhandene Quelle ist.</span><span class="sxs-lookup"><span data-stu-id="2d615-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d615-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d615-122">Return value</span></span>

<span data-ttu-id="2d615-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2d615-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d615-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d615-124">Requirements</span></span>



| <span data-ttu-id="2d615-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d615-125">Requirement</span></span> | <span data-ttu-id="2d615-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2d615-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d615-127">Version</span><span class="sxs-lookup"><span data-stu-id="2d615-127">Version</span></span><br/> | <span data-ttu-id="2d615-128">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2d615-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2d615-129">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2d615-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2d615-130">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2d615-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="2d615-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2d615-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d615-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d615-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="2d615-133">IID</span><span class="sxs-lookup"><span data-stu-id="2d615-133">IID</span></span><br/>     | <span data-ttu-id="2d615-134">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2d615-134">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="2d615-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d615-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d615-136">**Patch**</span><span class="sxs-lookup"><span data-stu-id="2d615-136">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="2d615-137">**Msisourcelistaddsourceex**</span><span class="sxs-lookup"><span data-stu-id="2d615-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="2d615-138">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d615-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




