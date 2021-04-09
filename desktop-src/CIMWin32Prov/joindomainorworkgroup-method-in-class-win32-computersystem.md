---
description: Fügt ein Computersystem einer Domäne oder Arbeitsgruppe hinzu.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: JoinDomainOrWorkgroup-Methode der Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861527"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="e3b22-103">JoinDomainOrWorkgroup-Methode der Win32 \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="e3b22-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="e3b22-104">Die **JoinDomainOrWorkgroup** -Methode verbindet ein Computersystem mit einer Domäne oder Arbeitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e3b22-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="e3b22-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3b22-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e3b22-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e3b22-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b22-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3b22-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="e3b22-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3b22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b22-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3b22-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-110">Gibt die Domäne oder Arbeitsgruppe an, der beigetreten werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3b22-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="e3b22-111">Darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e3b22-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-112">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3b22-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-113">Wenn der Parameter *username* einen Kontonamen angibt, muss der *Password* -Parameter auf das Kennwort verweisen, das beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3b22-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="e3b22-114">Andernfalls muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e3b22-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-115">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3b22-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-116">Ein Zeiger auf eine Konstante mit **null** endende Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3b22-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="e3b22-117">Sie müssen einen Domänen-NetBIOS-Namen und ein Benutzerkonto angeben, z. b. Domänen \\ Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e3b22-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="e3b22-118">Wenn dieser Parameter **null** ist, werden die Aufruferinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3b22-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="e3b22-119">Sie können auch den Benutzer Prinzipal Namen (User Principal Name, upped) im Formular verwenden user@domain .</span><span class="sxs-lookup"><span data-stu-id="e3b22-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-120">*AccountOU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3b22-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-121">Gibt den Zeiger auf eine Konstante mit **null** endenden Zeichenfolge an, die den [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) -Format Namen der Organisationseinheit (OU) für das Computer Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="e3b22-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="e3b22-122">Wenn Sie diesen Parameter angeben, muss die Zeichenfolge einen vollständigen Pfad enthalten. andernfalls muss der *Akzent* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e3b22-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="e3b22-123">Beispiel: "ou = testOU; DC = Domäne; DC = Domäne; DC = com "</span><span class="sxs-lookup"><span data-stu-id="e3b22-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-124">"F"- *Optionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3b22-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-125">Ein Satz von Bitflags, die die joinoptionen definieren.</span><span class="sxs-lookup"><span data-stu-id="e3b22-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="e3b22-126"> (0)</span><span class="sxs-lookup"><span data-stu-id="e3b22-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-127">Standard.</span><span class="sxs-lookup"><span data-stu-id="e3b22-127">Default.</span></span> <span data-ttu-id="e3b22-128">Keine Join-Optionen.</span><span class="sxs-lookup"><span data-stu-id="e3b22-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="e3b22-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**Netsetup \_ Beitreten zur \_ Domäne** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e3b22-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-130">Fügt den Computer einer Domäne hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3b22-130">Joins the computer to a domain.</span></span> <span data-ttu-id="e3b22-131">Wenn dieser Wert nicht angegeben wird, wird der Computer mit einer Arbeitsgruppe verbunden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="e3b22-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**Netsetup \_ Acct \_ Erstellen** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e3b22-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-133">Erstellt das Konto für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="e3b22-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="e3b22-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**Netsetup \_ WIN9X- \_ Upgrade** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e3b22-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-135">Der Joinvorgang tritt im Rahmen eines Upgrades auf.</span><span class="sxs-lookup"><span data-stu-id="e3b22-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="e3b22-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**Netsetup \_ Domänen \_ Beitritt, \_ Wenn \_** verknüpft (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e3b22-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-137">Ermöglicht das beitreten zu einer neuen Domäne, auch wenn der Computer bereits einer Domäne hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3b22-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="e3b22-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**Netsetup \_ \_Nicht sicher beitreten** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="e3b22-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-139">Führt einen unsicheren Beitritt durch.</span><span class="sxs-lookup"><span data-stu-id="e3b22-139">Performs an unsecured join.</span></span>

<span data-ttu-id="e3b22-140">Diese Option fordert einen Domänen Beitritt zu einem vorab erstellten Konto ohne Authentifizierung mit Domänen Benutzer-Anmelde Informationen an.</span><span class="sxs-lookup"><span data-stu-id="e3b22-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="e3b22-141">Diese Option kann in Verbindung mit der Option **netsetup \_ Machine \_ pwd- \_ weitergegeben** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="e3b22-142">In diesem Fall ist *Password* das Kennwort des vorab erstellten Computer Kontos.</span><span class="sxs-lookup"><span data-stu-id="e3b22-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="e3b22-143">Vor Windows Vista mit SP1 und Windows Server 2008 wurde ein unsicherer Join nicht beim Domänen Controller authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="e3b22-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="e3b22-144">Die gesamte Kommunikation wurde mithilfe einer NULL-Sitzung (nicht authentifiziert) durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="e3b22-145">Ab Windows Vista mit SP1 und Windows Server 2008 werden der Computer Konto Name und das Kennwort verwendet, um sich beim Domänen Controller zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="e3b22-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="e3b22-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**Netsetup \_ Computer- \_ pwd \_ übergeben** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="e3b22-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-147">Gibt an, dass der Kenn *Wort* Parameter anstelle eines Benutzer Kennworts ein Kennwort für das lokale Computer Konto angibt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="e3b22-148">Dieses Flag ist nur für unsichere Joins gültig, die Sie angeben müssen, indem Sie auch das unsecure-Flag "netsetup Join" festlegen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e3b22-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="e3b22-149">Wenn Sie dieses Flag festlegen, wird das Computer Kennwort nach erfolgreicher Verbindungs Ausführung auf den Wert des *Kennworts* festgelegt, wenn es sich bei diesem Wert um ein gültiges Computer Kennwort handelt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="e3b22-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**Netsetup \_ \_SPN- \_ Satz zurücksetzen** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="e3b22-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-151">Gibt an, dass der Dienst Prinzipal Name (SPN) und die DNSHostName-Eigenschaften des Computer Objekts zu diesem Zeitpunkt nicht aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3b22-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="e3b22-152">Diese Eigenschaften werden in der Regel während des Join-Vorgangs aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e3b22-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="e3b22-153">Stattdessen sollten diese Eigenschaften bei einem nachfolgenden Rückruf der [**Rename**](rename-method-in-class-win32-computersystem.md) -Methode aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="e3b22-154">Diese Eigenschaften werden während des Umbenennungs Vorgangs immer aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e3b22-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="e3b22-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**Netsetup \_ \_DC- \_ Konto beitreten** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="e3b22-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-156">Erlauben Sie den Domänen Beitritt, wenn ein vorhandenes Konto ein Domänen Controller ist.</span><span class="sxs-lookup"><span data-stu-id="e3b22-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-157">Dieses Flag wird unter Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="e3b22-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**Netsetup \_ Mehrdeutiger \_ DC** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="e3b22-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-159">Versuchen Sie beim Beitreten zur Domäne nicht, den bevorzugten Domänen Controller in der Registrierung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e3b22-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-160">Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="e3b22-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**Netsetup \_ Kein \_ Netlogon- \_ Cache** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="e3b22-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-162">Wenn Sie der Domäne beitreten, erstellen Sie den Netlogon-Cache nicht.</span><span class="sxs-lookup"><span data-stu-id="e3b22-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-163">Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="e3b22-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**Netsetup \_ Nicht \_ Steuerungs \_ Dienste** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="e3b22-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-165">Wenn Sie der Domäne beitreten, erzwingen Sie nicht, dass der Netlogon-Dienst startet.</span><span class="sxs-lookup"><span data-stu-id="e3b22-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-166">Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="e3b22-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**Netsetup \_ \_Computer \_ Namen festlegen** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="e3b22-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-168">Wenn Sie die Domäne nur für den Offline Beitritt beitreten, legen Sie den Hostnamen des Ziel Computers und den NetBIOS-Namen fest.</span><span class="sxs-lookup"><span data-stu-id="e3b22-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-169">Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="e3b22-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**Netsetup \_ \_SPN- \_ Satz erzwingen** (0x00010000 bis)</span><span class="sxs-lookup"><span data-stu-id="e3b22-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-171">Überschreiben Sie beim Beitreten zur Domäne andere Einstellungen während des Domänen Beitritts, und legen Sie den Dienst Prinzipal Namen (SPN) fest.</span><span class="sxs-lookup"><span data-stu-id="e3b22-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-172">Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="e3b22-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**Netsetup \_ Keine \_ Acct- \_ Wiederverwendung** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="e3b22-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-174">Verwenden Sie beim Beitreten zur Domäne kein vorhandenes Konto.</span><span class="sxs-lookup"><span data-stu-id="e3b22-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="e3b22-175">Dieses Flag wird unter Windows 7, Windows Server 2008 R2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="e3b22-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**Netsetup \_ \_Nicht unterstützte \_ Flags ignorieren** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="e3b22-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="e3b22-177">Wenn dieses Bit festgelegt ist, werden unbekannte Flags von der **JoinDomainOrWorkgroup** -Funktion ignoriert, und [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) verhält sich so, als ob die Flags nicht festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b22-178">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3b22-178">Return value</span></span>

<span data-ttu-id="e3b22-179">Gibt einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurück, der einen der folgenden numerischen Werte enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="e3b22-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="e3b22-180">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="e3b22-180">Any other number indicates an error.</span></span> <span data-ttu-id="e3b22-181">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e3b22-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="e3b22-182">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="e3b22-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-183">0</span><span class="sxs-lookup"><span data-stu-id="e3b22-183">0</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-184">**5**</span><span class="sxs-lookup"><span data-stu-id="e3b22-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-185">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="e3b22-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-186">**87**</span><span class="sxs-lookup"><span data-stu-id="e3b22-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-187">„Der Parameter ist falsch.“</span><span class="sxs-lookup"><span data-stu-id="e3b22-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-188">**110**</span><span class="sxs-lookup"><span data-stu-id="e3b22-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-189">Das System kann das angegebene Objekt nicht öffnen.</span><span class="sxs-lookup"><span data-stu-id="e3b22-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="e3b22-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-191">Das Kennwort kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="e3b22-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-193">Anmeldefehler: Unbekannter Benutzername oder ungültiges Kennwort.</span><span class="sxs-lookup"><span data-stu-id="e3b22-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="e3b22-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-195">Die angegebene Domäne ist entweder nicht vorhanden, oder es konnte keine Verbindung mit ihr hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="e3b22-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-197">Das Konto ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e3b22-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="e3b22-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-199">Der Computer ist bereits der Domäne beigetreten.</span><span class="sxs-lookup"><span data-stu-id="e3b22-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="e3b22-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-201">Der Computer ist zurzeit keiner Domäne beigetreten.</span><span class="sxs-lookup"><span data-stu-id="e3b22-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-202">**WBEM \_ E- \_ verschlüsselte \_ Verbindung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e3b22-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="e3b22-203">0x80041087</span></span>

<span data-ttu-id="e3b22-204">Das *Kennwort* und der *Benutzername* sind angegeben, aber die Authentifizierungs Ebene entspricht nicht der **RPC-C- \_ \_ authn- \_ Ebene \_ Pkt \_ Privacy**</span><span class="sxs-lookup"><span data-stu-id="e3b22-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="e3b22-205">Für Visual Basic wird **wbemErrEncryptedConnectionRequired** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3b22-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="e3b22-206">**Andere**</span><span class="sxs-lookup"><span data-stu-id="e3b22-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e3b22-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="e3b22-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3b22-208">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3b22-208">Remarks</span></span>

<span data-ttu-id="e3b22-209">Wenn Sie einen Computer von einer Domäne in eine Arbeitsgruppe verschieben, müssen Sie den Computer aus der Domäne entfernen (mit einem Aufruf von [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)), bevor Sie diese Methode aufrufen, um einer Arbeitsgruppe beizutreten (mit einem Aufruf von **JoinDomainOrWorkgroup**).</span><span class="sxs-lookup"><span data-stu-id="e3b22-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="e3b22-210">Starten Sie nach dem Aufrufen dieser Methode den betroffenen Computer neu, um die Änderungen zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="e3b22-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="e3b22-211">Der *Benutzername* und das *Kennwort* können **null** bleiben.</span><span class="sxs-lookup"><span data-stu-id="e3b22-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="e3b22-212">Allerdings muss die Authentifizierung der Verbindung mit WMI in den Skripts "6" oder " **wbemauthenticationlevelpktprivacy** " in Visual Basic und anderen Sprachen erfolgen, die die [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) Bibliothek verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e3b22-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="e3b22-213">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="e3b22-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="e3b22-214">Legen Sie in C++ die Authentifizierung auf **RPC- \_ C- \_ authn- \_ Ebene \_ Pkt \_ Privacy** entweder in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), für den gesamten Prozess oder in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)für eine Verbindung mit dem [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) -Proxy fest.</span><span class="sxs-lookup"><span data-stu-id="e3b22-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="e3b22-215">Weitere Informationen finden Sie unter [Festlegen der Authentifizierung mit C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) und [Festlegen der Sicherheit für IWbemServices und andere](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies)Proxys.</span><span class="sxs-lookup"><span data-stu-id="e3b22-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="e3b22-216">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3b22-216">Examples</span></span>

<span data-ttu-id="e3b22-217">Im Beispiel [Hinzufügen eines Computers zu einer Domäne in](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell wird ein Computer einer Domäne hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="e3b22-218">Im folgenden VBScript-Codebeispiel wird ein Computer mit einer Domäne verbunden und das Konto des Computers in Active Directory erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3b22-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="e3b22-219">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3b22-219">Requirements</span></span>



| <span data-ttu-id="e3b22-220">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3b22-220">Requirement</span></span> | <span data-ttu-id="e3b22-221">Wert</span><span class="sxs-lookup"><span data-stu-id="e3b22-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b22-222">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3b22-222">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b22-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3b22-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3b22-224">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3b22-224">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b22-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3b22-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3b22-226">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3b22-226">Namespace</span></span><br/>                | <span data-ttu-id="e3b22-227">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e3b22-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3b22-228">MOF</span><span class="sxs-lookup"><span data-stu-id="e3b22-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3b22-229"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e3b22-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3b22-230">DLL</span><span class="sxs-lookup"><span data-stu-id="e3b22-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3b22-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b22-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b22-232">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3b22-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b22-233">**Win32- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="e3b22-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="e3b22-234">**UnjoinDomainOrWorkgroup-Methode**</span><span class="sxs-lookup"><span data-stu-id="e3b22-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

