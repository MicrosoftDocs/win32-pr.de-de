---
description: Die sourcelistaddsource-Methode fügt eine Netzwerk-oder URL-Quelle hinzu. Akzeptiert SourcePath, Type und Index als Parameter. Diese Methode ruft msisourcelistaddsourceex auf.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Product. sourcelistaddsource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e0cfda9b8eab0e7dd00afd15eb701a6e7decf2ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372316"
---
# <a name="productsourcelistaddsource-method"></a><span data-ttu-id="56706-105">Product. sourcelistaddsource-Methode</span><span class="sxs-lookup"><span data-stu-id="56706-105">Product.SourceListAddSource method</span></span>

<span data-ttu-id="56706-106">Die **sourcelistaddsource** -Methode fügt eine Netzwerk-oder URL-Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="56706-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="56706-107">Akzeptiert *SourcePath*,*Type* und *Index* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="56706-107">Accepts *SourcePath*,*Type*, and *Index* as parameters.</span></span> <span data-ttu-id="56706-108">Diese Methode ruft [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)auf.</span><span class="sxs-lookup"><span data-stu-id="56706-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="56706-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="56706-109">Syntax</span></span>


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="56706-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="56706-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56706-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="56706-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="56706-112">Typ der hinzu zufügenden Quelle: msisourcetype \_ Network oder msisourcetype \_ URL.</span><span class="sxs-lookup"><span data-stu-id="56706-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="56706-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="56706-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="56706-114">Der Pfad zur hinzu zufügenden Quelle.</span><span class="sxs-lookup"><span data-stu-id="56706-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="56706-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="56706-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="56706-116">Wenn **sourcelistaddsource** mit einer neuen Quelle aufgerufen wird und *Index* auf 0 festgelegt ist, fügt das Installationsprogramm die Quelle am Ende der Quell Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="56706-116">If **SourceListAddSource** is called with a new source and *Index* is set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="56706-117">Wenn diese Funktion mit einer bereits in der Quell Liste vorhandenen Quelle aufgerufen wird und der *Index* auf 0 festgelegt ist, behält das Installationsprogramm den vorhandenen Index der Quelle bei.</span><span class="sxs-lookup"><span data-stu-id="56706-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="56706-118">Wenn die Funktion mit einer vorhandenen Quelle in der Quell Liste aufgerufen wird und der *Index* auf einen Wert ungleich 0 (null) festgelegt ist, wird die Quelle aus der aktuellen Position in der Liste entfernt und an der durch *Index* angegebenen Position eingefügt, bevor eine Quelle vorhanden ist, die an dieser Position bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="56706-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="56706-119">Wenn die Funktion mit einer neuen Quelle aufgerufen wird und der *Index* auf einen Wert ungleich 0 (null) festgelegt ist, wird die Quelle an der durch *Index* angegebenen Position eingefügt, bevor eine Quelle vorhanden ist, die an dieser Position bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="56706-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="56706-120">Der Indexwert für alle Quellen in der Liste nach dem durch *Index* angegebenen Index wird aktualisiert, um sicherzustellen, dass eindeutige Indexwerte und die bereits vorhandene Reihenfolge unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="56706-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the pre-existing order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="56706-121">Wenn *Index* größer als die Anzahl der Quellen in der Liste ist, wird die Quelle am Ende der Liste mit einem Indexwert eingefügt, der größer als jede vorhandene Quelle ist.</span><span class="sxs-lookup"><span data-stu-id="56706-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56706-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56706-122">Return value</span></span>

<span data-ttu-id="56706-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="56706-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56706-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56706-124">Requirements</span></span>



| <span data-ttu-id="56706-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56706-125">Requirement</span></span> | <span data-ttu-id="56706-126">Wert</span><span class="sxs-lookup"><span data-stu-id="56706-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56706-127">Version</span><span class="sxs-lookup"><span data-stu-id="56706-127">Version</span></span><br/> | <span data-ttu-id="56706-128">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="56706-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="56706-129">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56706-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="56706-130">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="56706-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="56706-131">DLL</span><span class="sxs-lookup"><span data-stu-id="56706-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="56706-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56706-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="56706-133">IID</span><span class="sxs-lookup"><span data-stu-id="56706-133">IID</span></span><br/>     | <span data-ttu-id="56706-134">IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="56706-134">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="56706-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56706-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56706-136">**Product**</span><span class="sxs-lookup"><span data-stu-id="56706-136">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="56706-137">**Msisourcelistaddsourceex**</span><span class="sxs-lookup"><span data-stu-id="56706-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="56706-138">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56706-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




