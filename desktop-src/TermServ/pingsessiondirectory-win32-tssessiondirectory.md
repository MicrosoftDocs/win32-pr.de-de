---
title: Pingsessiondirectory-Methode der Win32_TSSessionDirectory-Klasse
description: Überprüft, ob der Remotedesktopverbindung Broker-Server (RD-Verbindungsbroker) verfügbar ist.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Pingsessiondirectory-Methode Remotedesktopdienste
- Pingsessiondirectory-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, pingsessiondirectory-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518041"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="6baef-106">Pingsessiondirectory-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="6baef-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="6baef-107">Überprüft, ob der Remotedesktopverbindung Broker-Server (RD-Verbindungsbroker) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6baef-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="6baef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6baef-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="6baef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6baef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6baef-110">*Servername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6baef-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6baef-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6baef-111">Type: **string**</span></span>

<span data-ttu-id="6baef-112">Der Name des RD-Verbindungsbroker Servers.</span><span class="sxs-lookup"><span data-stu-id="6baef-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6baef-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6baef-113">Return value</span></span>

<span data-ttu-id="6baef-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6baef-114">Type: **uint32**</span></span>

<span data-ttu-id="6baef-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6baef-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6baef-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6baef-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="6baef-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6baef-117">Remarks</span></span>

<span data-ttu-id="6baef-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="6baef-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6baef-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="6baef-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6baef-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6baef-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6baef-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6baef-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6baef-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6baef-122">Requirements</span></span>



| <span data-ttu-id="6baef-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6baef-123">Requirement</span></span> | <span data-ttu-id="6baef-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6baef-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6baef-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6baef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6baef-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6baef-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6baef-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6baef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6baef-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6baef-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6baef-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6baef-129">Namespace</span></span><br/>                | <span data-ttu-id="6baef-130">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6baef-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6baef-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6baef-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6baef-132"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6baef-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6baef-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6baef-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6baef-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6baef-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6baef-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6baef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6baef-136">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="6baef-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

