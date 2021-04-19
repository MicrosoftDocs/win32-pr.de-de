---
title: Umgebungs variables-Methode der Win32_TSExpandEnvironmentVariables-Klasse
description: Erweitert System definierte Umgebungsvariablen. | Umgebungs variables-Methode der Win32_TSExpandEnvironmentVariables-Klasse
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Umgebungs variables-Methode Remotedesktopdienste
- Umgebungs variables-Methode Remotedesktopdienste, Win32_TSExpandEnvironmentVariables-Klasse
- Win32_TSExpandEnvironmentVariables-Klasse Remotedesktopdienste, Umgebungs variables-Methode
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355129"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="72e3a-107">Umgebungs variables-Methode der Win32- \_ Klasse "tsexpandumgebungsvariables"</span><span class="sxs-lookup"><span data-stu-id="72e3a-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="72e3a-108">Erweitert System definierte Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="72e3a-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e3a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e3a-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="72e3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72e3a-111">*OriginalString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72e3a-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72e3a-112">Eine Zeichenfolge, die die Umgebungsvariablen enthält, die erweitert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72e3a-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="72e3a-113">*Expandecodstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72e3a-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72e3a-114">Eine Zeichenfolge, in der die Umgebungsvariablen erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="72e3a-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72e3a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72e3a-115">Remarks</span></span>

<span data-ttu-id="72e3a-116">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="72e3a-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="72e3a-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="72e3a-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="72e3a-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="72e3a-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="72e3a-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72e3a-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="72e3a-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="72e3a-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="72e3a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72e3a-121">Requirements</span></span>



| <span data-ttu-id="72e3a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72e3a-122">Requirement</span></span> | <span data-ttu-id="72e3a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="72e3a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72e3a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72e3a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72e3a-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="72e3a-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="72e3a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72e3a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72e3a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e3a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72e3a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="72e3a-128">Namespace</span></span><br/>                | <span data-ttu-id="72e3a-129">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="72e3a-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="72e3a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="72e3a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72e3a-131"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="72e3a-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="72e3a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="72e3a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72e3a-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72e3a-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e3a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72e3a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e3a-135">**Win32 \_ tsexpandumgebungs variables**</span><span class="sxs-lookup"><span data-stu-id="72e3a-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

