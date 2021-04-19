---
description: Die extractpatchxmldata-Methode des Installer-Objekts extrahiert Informationen aus einem Patch als XML-Zeichenfolge. Anhand dieser Informationen kann ermittelt werden, ob der Patch auf ein Zielsystem angewendet wird. Diese Methode ruft msiextractpatchxmldata auf.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Installer. extractpatchxmldata-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367444"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="640fe-105">Installer. extractpatchxmldata-Methode</span><span class="sxs-lookup"><span data-stu-id="640fe-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="640fe-106">Die **extractpatchxmldata** -Methode des [**Installer**](installer-object.md) -Objekts extrahiert Informationen aus einem Patch als XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="640fe-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="640fe-107">Anhand dieser Informationen kann ermittelt werden, ob der Patch auf ein Zielsystem angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="640fe-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="640fe-108">Diese Methode ruft [**msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)auf.</span><span class="sxs-lookup"><span data-stu-id="640fe-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="640fe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="640fe-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="640fe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="640fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640fe-111">*Patchpfad*</span><span class="sxs-lookup"><span data-stu-id="640fe-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="640fe-112">Vollständiger Pfad zum Patch, von dem die anwendbarkeits Informationen extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="640fe-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640fe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="640fe-113">Return value</span></span>

<span data-ttu-id="640fe-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="640fe-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="640fe-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="640fe-115">Requirements</span></span>



| <span data-ttu-id="640fe-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="640fe-116">Requirement</span></span> | <span data-ttu-id="640fe-117">Wert</span><span class="sxs-lookup"><span data-stu-id="640fe-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640fe-118">Version</span><span class="sxs-lookup"><span data-stu-id="640fe-118">Version</span></span><br/> | <span data-ttu-id="640fe-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="640fe-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="640fe-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="640fe-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="640fe-121">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="640fe-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="640fe-122">DLL</span><span class="sxs-lookup"><span data-stu-id="640fe-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="640fe-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="640fe-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="640fe-124">IID</span><span class="sxs-lookup"><span data-stu-id="640fe-124">IID</span></span><br/>     | <span data-ttu-id="640fe-125">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="640fe-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="640fe-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="640fe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640fe-127">**Msiextractpatchxmldata**</span><span class="sxs-lookup"><span data-stu-id="640fe-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="640fe-128">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="640fe-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




