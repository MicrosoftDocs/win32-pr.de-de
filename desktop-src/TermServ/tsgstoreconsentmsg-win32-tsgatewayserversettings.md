---
title: Zgstoreconsentmsg-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktualisiert die Zustimmungs Nachricht für den Gatewayserver.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- Zgstoreconsentmsg-Methode Remotedesktopdienste
- Methode Remotedesktopdienste der Methode "zgstoreconsentmsg", Win32_TSGatewayServerSettings Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, Methode "zgstoreconsentmsg"
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477091"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="6ec5e-106">Zgstoreconsentmsg-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="6ec5e-106">TSGStoreConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="6ec5e-107">Aktualisiert die Zustimmungs Nachricht für den Gatewayserver.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-107">Updates the consent message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec5e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ec5e-108">Syntax</span></span>


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a><span data-ttu-id="6ec5e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec5e-110">GS-Verbindungs *Text* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ec5e-110">*TSGConMsgText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec5e-111">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6ec5e-111">Type: **string**</span></span>

<span data-ttu-id="6ec5e-112">Der Zustimmungs Meldungs Text.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-112">The consent message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec5e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ec5e-113">Return value</span></span>

<span data-ttu-id="6ec5e-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ec5e-114">Type: **uint32**</span></span>

<span data-ttu-id="6ec5e-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6ec5e-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6ec5e-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6ec5e-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec5e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ec5e-118">Remarks</span></span>

<span data-ttu-id="6ec5e-119">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6ec5e-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6ec5e-121">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6ec5e-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ec5e-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6ec5e-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6ec5e-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec5e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ec5e-124">Requirements</span></span>



| <span data-ttu-id="6ec5e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ec5e-125">Requirement</span></span> | <span data-ttu-id="6ec5e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6ec5e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec5e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ec5e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec5e-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6ec5e-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6ec5e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ec5e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec5e-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ec5e-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="6ec5e-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ec5e-131">Namespace</span></span><br/>                | <span data-ttu-id="6ec5e-132">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6ec5e-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6ec5e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6ec5e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ec5e-134"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5e-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ec5e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec5e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec5e-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec5e-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6ec5e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ec5e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec5e-138">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="6ec5e-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

