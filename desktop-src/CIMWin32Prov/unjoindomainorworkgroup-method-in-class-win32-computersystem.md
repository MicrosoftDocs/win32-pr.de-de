---
description: Entfernt ein Computersystem aus einer Domäne oder Arbeitsgruppe.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: UnjoinDomainOrWorkgroup-Methode der Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861600"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="58e42-103">UnjoinDomainOrWorkgroup-Methode der Win32 \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="58e42-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="58e42-104">Mit der **UnjoinDomainOrWorkgroup** -Methode wird ein Computersystem aus einer Domäne oder Arbeitsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="58e42-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="58e42-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="58e42-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="58e42-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="58e42-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="58e42-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e42-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="58e42-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="58e42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e42-109">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e42-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e42-110">Wenn der Parameter *username* einen Kontonamen angibt, muss der *Password* -Parameter auf das Kennwort verweisen, das beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58e42-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="58e42-111">Andernfalls muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="58e42-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="58e42-112">Das *Kennwort* muss bei der Verbindung mit winmgmt oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) auf dem [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Zeiger eine hohe Authentifizierungs Ebene und nicht weniger als die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene** verwenden.</span><span class="sxs-lookup"><span data-stu-id="58e42-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="58e42-113">Wenn es sich um ein lokales in WinMgmt handelt, ist dies kein Problem.</span><span class="sxs-lookup"><span data-stu-id="58e42-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="58e42-114">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e42-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e42-115">Ein Zeiger auf eine Konstante mit NULL endende Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58e42-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="58e42-116">Sie müssen ein Domänen-und Benutzerkonto angeben, z. b. "Domänen \\ Benutzer" oder " user@domain ".</span><span class="sxs-lookup"><span data-stu-id="58e42-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="58e42-117">Wenn dieser Parameter **null** ist, wird der Aufruferkontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="58e42-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="58e42-118">Der *Benutzername* muss beim Herstellen einer Verbindung mit winmgmt oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) auf dem [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Zeiger eine hohe Authentifizierungs Ebene und nicht weniger als die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene** verwenden.</span><span class="sxs-lookup"><span data-stu-id="58e42-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="58e42-119">Wenn es sich um ein lokales in WinMgmt handelt, ist dies kein Problem.</span><span class="sxs-lookup"><span data-stu-id="58e42-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="58e42-120">*FUnjoinOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58e42-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58e42-121">Ein Satz von Bitflags, die die Optionen für den entfernen definieren.</span><span class="sxs-lookup"><span data-stu-id="58e42-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="58e42-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="58e42-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="58e42-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="58e42-123">Default.</span></span> <span data-ttu-id="58e42-124">Keine Optionen.</span><span class="sxs-lookup"><span data-stu-id="58e42-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="58e42-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**Netsetup \_ \_Löschen** (4)</span><span class="sxs-lookup"><span data-stu-id="58e42-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="58e42-126">Deaktivieren Sie das Active Directory Konto nach dem Vorgang zum nicht beitreten, aber löschen Sie das Konto nicht.</span><span class="sxs-lookup"><span data-stu-id="58e42-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e42-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58e42-127">Return value</span></span>

<span data-ttu-id="58e42-128">Die **UnjoinDomainOrWorkgroup** -Methode gibt bei Erfolg 0 (null) zurück oder wenn keine Optionen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="58e42-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="58e42-129">Jeder andere Wert gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="58e42-129">Any other value indicates an error.</span></span> <span data-ttu-id="58e42-130">Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="58e42-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="58e42-131">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="58e42-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="58e42-132">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="58e42-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58e42-133">**Sonstige** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="58e42-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="58e42-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58e42-134">Remarks</span></span>

<span data-ttu-id="58e42-135">Starten Sie nach dem Aufrufen dieser Methode den betroffenen Computer neu, um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="58e42-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="58e42-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58e42-136">Examples</span></span>

<span data-ttu-id="58e42-137">[Die Verknüpfung eines Computers aus einer Domäne entfernen](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) Im VBScript-Beispiel wird der lokale Computer aus der aktuellen Domäne entfernt, und das Computer Konto wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="58e42-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="58e42-138">Das Beispiel zum [Entfernen eines Computers aus einer Domäne mithilfe eines vbskripts](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) entfernt die Verknüpfung eines angegebenen Computers zu einer Domäne.</span><span class="sxs-lookup"><span data-stu-id="58e42-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="58e42-139">.</span><span class="sxs-lookup"><span data-stu-id="58e42-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e42-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58e42-140">Requirements</span></span>



| <span data-ttu-id="58e42-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58e42-141">Requirement</span></span> | <span data-ttu-id="58e42-142">Wert</span><span class="sxs-lookup"><span data-stu-id="58e42-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e42-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58e42-143">Minimum supported client</span></span><br/> | <span data-ttu-id="58e42-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58e42-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58e42-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58e42-145">Minimum supported server</span></span><br/> | <span data-ttu-id="58e42-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58e42-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58e42-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="58e42-147">Namespace</span></span><br/>                | <span data-ttu-id="58e42-148">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58e42-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58e42-149">MOF</span><span class="sxs-lookup"><span data-stu-id="58e42-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58e42-150"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58e42-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58e42-151">DLL</span><span class="sxs-lookup"><span data-stu-id="58e42-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e42-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e42-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e42-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58e42-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e42-154">**Win32- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="58e42-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="58e42-155">**JoinDomainOrWorkgroup-Methode**</span><span class="sxs-lookup"><span data-stu-id="58e42-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

