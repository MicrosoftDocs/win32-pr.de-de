---
title: Die Methode "szessiondirectoryexposeserverip" der Win32_TSSessionDirectory-Klasse
description: Legt die sessiondirectoriyexposeserverip-Eigenschaft fest.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "" der Methode "" der Methode "*"
- Methode Remotedesktopdienste der Methode "" der Klasse "Win32_TSSessionDirectory"
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, Methode "" der Methode ""
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949732"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="c1dd8-106">Die Methode "tssessiondirectoryexposeserverip" der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="c1dd8-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="c1dd8-107">Legt die **sessiondirectoriyexposeserverip-** Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1dd8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1dd8-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="c1dd8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1dd8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1dd8-110">*Sessiondirectoriyexposeserverip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1dd8-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1dd8-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-111">Type: **uint32**</span></span>

<span data-ttu-id="c1dd8-112">Flag zum Deaktivieren oder Aktivieren der **sessiondirectoriyexposeserverip-** Eigenschaft, die das Abrufen der IP-Adresse für das Sitzungs Verzeichnis zulässt oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c1dd8-113"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c1dd8-114">Deaktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c1dd8-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c1dd8-116">Aktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1dd8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1dd8-117">Return value</span></span>

<span data-ttu-id="c1dd8-118">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-118">Type: **uint32**</span></span>

<span data-ttu-id="c1dd8-119">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c1dd8-120">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dd8-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="c1dd8-121">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1dd8-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1dd8-122">Remarks</span></span>

<span data-ttu-id="c1dd8-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c1dd8-124">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c1dd8-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1dd8-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c1dd8-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c1dd8-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dd8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1dd8-127">Requirements</span></span>



| <span data-ttu-id="c1dd8-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1dd8-128">Requirement</span></span> | <span data-ttu-id="c1dd8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c1dd8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dd8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1dd8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c1dd8-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1dd8-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c1dd8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1dd8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c1dd8-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1dd8-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1dd8-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1dd8-134">Namespace</span></span><br/>                | <span data-ttu-id="c1dd8-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c1dd8-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c1dd8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c1dd8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1dd8-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c1dd8-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1dd8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c1dd8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1dd8-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1dd8-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1dd8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1dd8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1dd8-141">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="c1dd8-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

