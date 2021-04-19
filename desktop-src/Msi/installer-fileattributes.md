---
description: Die File Attributeigenschaft des Installer-Objekts gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer. File Attribute-Eigenschaft (Windows. Storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369379"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="705b8-103">Installer. File Attribute (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="705b8-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="705b8-104">Die **File Attributeigenschaft** des [**Installer**](installer-object.md) -Objekts gibt eine Zahl zurück, die die kombinierten Dateiattribute für den angegebenen Pfad zu einer Datei oder einem Ordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="705b8-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="705b8-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="705b8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="705b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="705b8-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="705b8-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="705b8-107">Property value</span></span>

<span data-ttu-id="705b8-108">Der erforderliche Pfad zur Datei oder zum Ordner.</span><span class="sxs-lookup"><span data-stu-id="705b8-108">The required path to the file or folder.</span></span> <span data-ttu-id="705b8-109">Ein partieller Pfad nimmt das aktuelle Verzeichnis an.</span><span class="sxs-lookup"><span data-stu-id="705b8-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="705b8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="705b8-110">Remarks</span></span>

<span data-ttu-id="705b8-111">Die **File Attributeigenschaft** gibt die folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="705b8-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="705b8-112">File-Attribut</span><span class="sxs-lookup"><span data-stu-id="705b8-112">File attribute</span></span>              | <span data-ttu-id="705b8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="705b8-113">Value</span></span>      | <span data-ttu-id="705b8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="705b8-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="705b8-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="705b8-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="705b8-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="705b8-116">0x00000001</span></span> | <span data-ttu-id="705b8-117">1</span><span class="sxs-lookup"><span data-stu-id="705b8-117">1</span></span>     |
| <span data-ttu-id="705b8-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="705b8-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="705b8-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="705b8-119">0x00000002</span></span> | <span data-ttu-id="705b8-120">2</span><span class="sxs-lookup"><span data-stu-id="705b8-120">2</span></span>     |
| <span data-ttu-id="705b8-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="705b8-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="705b8-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="705b8-122">0x00000004</span></span> | <span data-ttu-id="705b8-123">4</span><span class="sxs-lookup"><span data-stu-id="705b8-123">4</span></span>     |
| <span data-ttu-id="705b8-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="705b8-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="705b8-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="705b8-125">0x00000010</span></span> | <span data-ttu-id="705b8-126">16</span><span class="sxs-lookup"><span data-stu-id="705b8-126">16</span></span>    |
| <span data-ttu-id="705b8-127">Datei \_ Attribut \_ temporär</span><span class="sxs-lookup"><span data-stu-id="705b8-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="705b8-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="705b8-128">0x00000100</span></span> | <span data-ttu-id="705b8-129">256</span><span class="sxs-lookup"><span data-stu-id="705b8-129">256</span></span>   |
| <span data-ttu-id="705b8-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="705b8-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="705b8-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="705b8-131">0x00000800</span></span> | <span data-ttu-id="705b8-132">2048</span><span class="sxs-lookup"><span data-stu-id="705b8-132">2048</span></span>  |
| <span data-ttu-id="705b8-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="705b8-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="705b8-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="705b8-134">0x00001000</span></span> | <span data-ttu-id="705b8-135">4096</span><span class="sxs-lookup"><span data-stu-id="705b8-135">4096</span></span>  |



 

<span data-ttu-id="705b8-136">Gibt – 1 zurück, wenn die Datei oder der Ordner nicht vorhanden oder nicht zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="705b8-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="705b8-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="705b8-137">Requirements</span></span>



| <span data-ttu-id="705b8-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="705b8-138">Requirement</span></span> | <span data-ttu-id="705b8-139">Wert</span><span class="sxs-lookup"><span data-stu-id="705b8-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705b8-140">Version</span><span class="sxs-lookup"><span data-stu-id="705b8-140">Version</span></span><br/> | <span data-ttu-id="705b8-141">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="705b8-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="705b8-142">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="705b8-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="705b8-143">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="705b8-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="705b8-144">Header</span><span class="sxs-lookup"><span data-stu-id="705b8-144">Header</span></span><br/>  | <dl> <span data-ttu-id="705b8-145"><dt>Windows. Storage. h</dt></span><span class="sxs-lookup"><span data-stu-id="705b8-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="705b8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="705b8-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="705b8-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="705b8-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="705b8-148">IID</span><span class="sxs-lookup"><span data-stu-id="705b8-148">IID</span></span><br/>     | <span data-ttu-id="705b8-149">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="705b8-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




