---
title: Delete-Methode der Win32_TSAccount-Klasse
description: Die Delete-Methode löscht den angegebenen Benutzer, die Gruppe oder das Computer Konto.
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- Delete-Methode Remotedesktopdienste
- Delete-Methode Remotedesktopdienste, Win32_TSAccount-Klasse
- Win32_TSAccount-Klasse Remotedesktopdienste, DELETE-Methode
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ab76ad1200fc872a3a105e74533460104d806
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392160"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="57ae1-106">Delete-Methode der Win32- \_ Klasse "zaccount"</span><span class="sxs-lookup"><span data-stu-id="57ae1-106">Delete method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="57ae1-107">Die **Delete** -Methode löscht den angegebenen Benutzer, die Gruppe oder das Computer Konto.</span><span class="sxs-lookup"><span data-stu-id="57ae1-107">The **Delete** method deletes the specified user, group, or computer account.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ae1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ae1-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="57ae1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="57ae1-109">Parameters</span></span>

<span data-ttu-id="57ae1-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="57ae1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57ae1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57ae1-111">Return value</span></span>

<span data-ttu-id="57ae1-112">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="57ae1-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="57ae1-113">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="57ae1-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ae1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57ae1-114">Remarks</span></span>

<span data-ttu-id="57ae1-115">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="57ae1-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="57ae1-116">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="57ae1-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="57ae1-117">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="57ae1-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="57ae1-118">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="57ae1-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="57ae1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57ae1-119">Requirements</span></span>



| <span data-ttu-id="57ae1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57ae1-120">Requirement</span></span> | <span data-ttu-id="57ae1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="57ae1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57ae1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57ae1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57ae1-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ae1-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57ae1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57ae1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57ae1-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ae1-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57ae1-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="57ae1-126">Namespace</span></span><br/>                | <span data-ttu-id="57ae1-127">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="57ae1-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="57ae1-128">MOF</span><span class="sxs-lookup"><span data-stu-id="57ae1-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57ae1-129"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="57ae1-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="57ae1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="57ae1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ae1-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ae1-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ae1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57ae1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ae1-133">**Win32- \_ Konto**</span><span class="sxs-lookup"><span data-stu-id="57ae1-133">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

