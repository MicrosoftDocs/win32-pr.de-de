---
description: Die Methode "flehash" des Installerobjekts nimmt den Pfad zu einer Datei an und gibt einen 128-Bit-Hash dieser Datei zurück. Die Datei Hash Informationen werden als Datensatz-Objekt zurückgegeben. Der gesamte 128-Bit-Dateihash wird als 4 32-Bit-IntegerData-Eigenschafts Felder zurückgegeben.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer. flehash-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364790"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="359d9-105">Installer. flehash-Methode</span><span class="sxs-lookup"><span data-stu-id="359d9-105">Installer.FileHash method</span></span>

<span data-ttu-id="359d9-106">Die Methode " **flehash** " des [**Installerobjekts**](installer-object.md) nimmt den Pfad zu einer Datei an und gibt einen 128-Bit-Hash dieser Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="359d9-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="359d9-107">Die Datei Hash Informationen werden als Datensatz- [**Objekt**](record-object.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="359d9-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="359d9-108">Der gesamte 128-Bit-Dateihash wird als 4 32-Bit- [**IntegerData**](record-integerdata.md) -Eigenschafts Felder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="359d9-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="359d9-109">Die Werte, die im [**Datensatz-Objekt**](record-object.md) zurückgegeben werden, entsprechen den vier Feldern der [**msigetatashinfo**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) -Struktur, die von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="359d9-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="359d9-110">Die Nummerierung von vier Feldern ist 1-basiert in der [msimelehash-Tabelle](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="359d9-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="359d9-111">Feld 1 entspricht der HashPart1-Spalte.</span><span class="sxs-lookup"><span data-stu-id="359d9-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="359d9-112">Feld 2 entspricht der HashPart2-Spalte.</span><span class="sxs-lookup"><span data-stu-id="359d9-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="359d9-113">Field 3 entspricht der HashPart3-Spalte.</span><span class="sxs-lookup"><span data-stu-id="359d9-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="359d9-114">Field 4 entspricht der HashPart4-Spalte.</span><span class="sxs-lookup"><span data-stu-id="359d9-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="359d9-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="359d9-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="359d9-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="359d9-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="359d9-117">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="359d9-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="359d9-118">Der Pfad zu der Datei, für die ein Hashwert erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="359d9-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="359d9-119">*Optionen*</span><span class="sxs-lookup"><span data-stu-id="359d9-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="359d9-120">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="359d9-120">Reserved for future use.</span></span>

<span data-ttu-id="359d9-121">Der Wert dieses Parameters muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="359d9-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="359d9-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="359d9-122">Return value</span></span>

<span data-ttu-id="359d9-123">Bei erfolgreicher Ausführung gibt diese Methode ein [**Daten Satz Objekt**](record-object.md) zurück, das den Hash der Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="359d9-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="359d9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="359d9-124">Requirements</span></span>



| <span data-ttu-id="359d9-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="359d9-125">Requirement</span></span> | <span data-ttu-id="359d9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="359d9-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="359d9-127">Version</span><span class="sxs-lookup"><span data-stu-id="359d9-127">Version</span></span><br/> | <span data-ttu-id="359d9-128">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="359d9-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="359d9-129">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="359d9-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="359d9-130">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="359d9-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="359d9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="359d9-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="359d9-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="359d9-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="359d9-133">IID</span><span class="sxs-lookup"><span data-stu-id="359d9-133">IID</span></span><br/>     | <span data-ttu-id="359d9-134">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="359d9-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="359d9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="359d9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359d9-136">Standardmäßige Datei Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="359d9-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="359d9-137">Verwalten von Dateigrößen und-Versionen</span><span class="sxs-lookup"><span data-stu-id="359d9-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="359d9-138">Msiflehash-Tabelle</span><span class="sxs-lookup"><span data-stu-id="359d9-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="359d9-139">**Msigetflehash**</span><span class="sxs-lookup"><span data-stu-id="359d9-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




