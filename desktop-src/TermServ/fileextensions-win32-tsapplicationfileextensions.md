---
title: FileExtensions-Methode der Win32_TSApplicationFileExtensions-Klasse
description: Stellt eine Liste der Dateinamen Erweiterungen bereit, die von einer Anwendung behandelt werden.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- FileExtensions-Methode Remotedesktopdienste
- File Extensions-Methode Remotedesktopdienste, Win32_TSApplicationFileExtensions-Klasse
- Win32_TSApplicationFileExtensions-Klasse Remotedesktopdienste, FileExtensions-Methode
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957066"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="ea180-106">FileExtensions-Methode der Win32- \_ Klasse "tyapplicationfileextensions"</span><span class="sxs-lookup"><span data-stu-id="ea180-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="ea180-107">Stellt eine Liste der Dateinamen Erweiterungen bereit, die von einer Anwendung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ea180-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea180-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea180-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="ea180-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea180-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea180-110">*Apppath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea180-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea180-111">Pfad der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ea180-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="ea180-112">*Erweiterungen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ea180-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea180-113">Die Dateinamen Erweiterungen, die von der Anwendung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ea180-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea180-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea180-114">Remarks</span></span>

<span data-ttu-id="ea180-115">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ea180-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ea180-116">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ea180-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ea180-117">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ea180-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ea180-118">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea180-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ea180-119">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ea180-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea180-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea180-120">Requirements</span></span>



| <span data-ttu-id="ea180-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea180-121">Requirement</span></span> | <span data-ttu-id="ea180-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ea180-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea180-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea180-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea180-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea180-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ea180-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea180-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea180-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea180-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea180-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea180-127">Namespace</span></span><br/>                | <span data-ttu-id="ea180-128">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ea180-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ea180-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ea180-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea180-130"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ea180-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="ea180-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ea180-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea180-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea180-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea180-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea180-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea180-134">**Win32- \_ applicationfileextensions**</span><span class="sxs-lookup"><span data-stu-id="ea180-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

