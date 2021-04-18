---
title: Die Methode "stexportpath" der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert den Verzeichnispfad, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "stexportpath"
- Methode Remotedesktopdienste der Methode "Win32_RDMSDeploymentSettings"
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, Methode "abtexportpath"
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340581"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="a6af7-106">Die Methode "stexportpath" der Win32- \_ Klasse "rdmsdeploymentsettings"</span><span class="sxs-lookup"><span data-stu-id="a6af7-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="a6af7-107">Aktualisiert den Verzeichnispfad, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a6af7-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6af7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6af7-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="a6af7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6af7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6af7-110">*Directoriypath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6af7-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6af7-111">Der neue Verzeichnispfad.</span><span class="sxs-lookup"><span data-stu-id="a6af7-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6af7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6af7-112">Return value</span></span>

<span data-ttu-id="a6af7-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6af7-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6af7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6af7-114">Requirements</span></span>



| <span data-ttu-id="a6af7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6af7-115">Requirement</span></span> | <span data-ttu-id="a6af7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a6af7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6af7-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6af7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a6af7-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a6af7-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a6af7-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6af7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a6af7-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6af7-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a6af7-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6af7-121">Namespace</span></span><br/>                | <span data-ttu-id="a6af7-122">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="a6af7-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a6af7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a6af7-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6af7-124"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a6af7-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6af7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a6af7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6af7-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6af7-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a6af7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6af7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6af7-128">**Win32 \_ rdmsdeploymentsettings**</span><span class="sxs-lookup"><span data-stu-id="a6af7-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





