---
title: Fileassociations-Methode der Win32_TSApplicationFileExtensions-Klasse
description: Scannt die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Fileassociations-Methode Remotedesktopdienste
- Fileassociations-Methode Remotedesktopdienste, Win32_TSApplicationFileExtensions-Klasse
- Win32_TSApplicationFileExtensions-Klasse Remotedesktopdienste, fileassociations-Methode
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340005"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="f17cc-106">Filezuzuordnungen-Methode der Win32-Klasse "-Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="f17cc-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="f17cc-107">Scannt die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f17cc-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="f17cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f17cc-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="f17cc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f17cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f17cc-110">*Apppath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f17cc-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f17cc-111">Gibt den Pfad zur Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="f17cc-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="f17cc-112">*Dateizuordnungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f17cc-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f17cc-113">Nach erfolgreichem Abschluss enthält die Dateizuordnungen für diese Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f17cc-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f17cc-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f17cc-114">Requirements</span></span>



| <span data-ttu-id="f17cc-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f17cc-115">Requirement</span></span> | <span data-ttu-id="f17cc-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f17cc-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f17cc-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f17cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f17cc-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f17cc-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f17cc-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f17cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f17cc-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f17cc-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="f17cc-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="f17cc-121">Namespace</span></span><br/>                | <span data-ttu-id="f17cc-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f17cc-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f17cc-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f17cc-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f17cc-124"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f17cc-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f17cc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f17cc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f17cc-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17cc-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f17cc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f17cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f17cc-128">**Win32- \_ applicationfileextensions**</span><span class="sxs-lookup"><span data-stu-id="f17cc-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="f17cc-129">**Win32 \_ rdfileassociation**</span><span class="sxs-lookup"><span data-stu-id="f17cc-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





