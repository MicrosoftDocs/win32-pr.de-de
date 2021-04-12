---
title: Win32_RemoteAppChangeEvent-Klasse
description: Stellt eine Änderung an Windows Server 2008 R2 RemoteApp-Einstellungen auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) dar.
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Win32_RemoteAppChangeEvent-Klasse Remotedesktopdienste
- Win32_RemoteAppChangeEvent Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103676"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="034ff-105">Win32 \_ remoteappchangeevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="034ff-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="034ff-106">Stellt eine Änderung an Windows Server 2008 R2 RemoteApp-Einstellungen auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) dar.</span><span class="sxs-lookup"><span data-stu-id="034ff-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="034ff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="034ff-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="034ff-108">Member</span><span class="sxs-lookup"><span data-stu-id="034ff-108">Members</span></span>

<span data-ttu-id="034ff-109">Die **Win32 \_ remoteappchangeevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="034ff-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="034ff-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="034ff-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="034ff-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="034ff-111">Properties</span></span>

<span data-ttu-id="034ff-112">Die **Win32 \_ remoteappchangeevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="034ff-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="034ff-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="034ff-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="034ff-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="034ff-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="034ff-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="034ff-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="034ff-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="034ff-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="034ff-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="034ff-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="034ff-118">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="034ff-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="034ff-119">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="034ff-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="034ff-120">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="034ff-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="034ff-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="034ff-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="034ff-122">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="034ff-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="034ff-123">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="034ff-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="034ff-124">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="034ff-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="034ff-125">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.</span><span class="sxs-lookup"><span data-stu-id="034ff-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="034ff-126">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="034ff-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="034ff-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="034ff-127">Remarks</span></span>

<span data-ttu-id="034ff-128">Zum Herstellen einer Verbindung mit dem \\ Namespace "root cimv2 \\ TerminalServices" muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="034ff-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="034ff-129">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="034ff-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="034ff-130">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="034ff-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="034ff-131">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="034ff-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="034ff-132">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="034ff-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="034ff-133">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="034ff-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="034ff-134">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="034ff-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="034ff-135">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="034ff-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="034ff-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="034ff-136">Requirements</span></span>



| <span data-ttu-id="034ff-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="034ff-137">Requirement</span></span> | <span data-ttu-id="034ff-138">Wert</span><span class="sxs-lookup"><span data-stu-id="034ff-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="034ff-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="034ff-139">Minimum supported client</span></span><br/> | <span data-ttu-id="034ff-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="034ff-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="034ff-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="034ff-141">Minimum supported server</span></span><br/> | <span data-ttu-id="034ff-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="034ff-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="034ff-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="034ff-143">Namespace</span></span><br/>                | <span data-ttu-id="034ff-144">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="034ff-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="034ff-145">MOF</span><span class="sxs-lookup"><span data-stu-id="034ff-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="034ff-146"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="034ff-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="034ff-147">DLL</span><span class="sxs-lookup"><span data-stu-id="034ff-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="034ff-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="034ff-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

