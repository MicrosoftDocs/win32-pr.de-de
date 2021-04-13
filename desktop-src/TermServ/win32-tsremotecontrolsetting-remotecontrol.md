---
title: Remotecontrol-Methode der Win32_TSRemoteControlSetting-Klasse
description: Die Methode "levelofcontrol" wird von der remotecontrol-Methode festgelegt.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Remotecontrol-Methode Remotedesktopdienste
- Remotecontrol-Methode Remotedesktopdienste, Win32_TSRemoteControlSetting-Klasse
- Win32_TSRemoteControlSetting-Klasse Remotedesktopdienste, remotecontrol-Methode
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340628"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="7b4d5-106">Remotecontrol-Methode der Win32- \_ Klasse "zremotecontrolsetting"</span><span class="sxs-lookup"><span data-stu-id="7b4d5-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="7b4d5-107">Die Methode " **levelofcontrol** " wird von der **remotecontrol** -Methode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4d5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b4d5-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="7b4d5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b4d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4d5-110">*Levelofcontrol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4d5-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4d5-111">Neuer Wert für die **levelofcontrol** -Eigenschaft, die angibt, ob die Sitzung nur vom Remote Benutzer angezeigt wird oder über Tastatur und Maus angezeigt und gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="7b4d5-112">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="7b4d5-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="7b4d5-113">Die folgenden Werte werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="7b4d5-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** (0)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7b4d5-115">Die Remote Steuerung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="7b4d5-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7b4d5-117">Der Benutzer der Remote Steuerung hat die vollständige Kontrolle über die Sitzung des Benutzers mit der Berechtigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="7b4d5-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7b4d5-119">Der Benutzer der Remote Steuerung hat die vollständige Kontrolle über die Sitzung des Benutzers. die Berechtigung des Benutzers ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="7b4d5-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b4d5-121">Der Benutzer der Remote Steuerung kann die Sitzung Remote mit der Berechtigung des Benutzers anzeigen. der Remote Benutzer kann die Sitzung nicht aktiv steuern.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="7b4d5-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b4d5-123">Der Benutzer der Remote Steuerung kann die Sitzung Remote anzeigen, aber die Sitzung nicht aktiv steuern. die Berechtigung des Benutzers ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4d5-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b4d5-124">Return value</span></span>

<span data-ttu-id="7b4d5-125">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7b4d5-126">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4d5-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7b4d5-127">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4d5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b4d5-128">Remarks</span></span>

<span data-ttu-id="7b4d5-129">Vollständige Kontrolle über eine Sitzung bedeutet, dass der Remote Benutzer die Sitzung des Benutzers mit Tastatur und Maus aktiv steuern kann.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="7b4d5-130">Wenn ein Benutzer versucht, eine Remote Steuerungs Verbindung herzustellen, zeigt das System eine Meldung an den Remote Client an und fordert die Berechtigung an, die Remote Sitzung entweder in der Remote Sitzung anzuzeigen oder aktiv zu nehmen.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="7b4d5-131">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7b4d5-132">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7b4d5-133">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b4d5-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7b4d5-134">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7b4d5-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4d5-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b4d5-135">Requirements</span></span>



| <span data-ttu-id="7b4d5-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b4d5-136">Requirement</span></span> | <span data-ttu-id="7b4d5-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7b4d5-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4d5-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4d5-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b4d5-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b4d5-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b4d5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4d5-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b4d5-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b4d5-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b4d5-142">Namespace</span></span><br/>                | <span data-ttu-id="7b4d5-143">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7b4d5-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7b4d5-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7b4d5-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b4d5-145"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7b4d5-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b4d5-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4d5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b4d5-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4d5-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4d5-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b4d5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4d5-149">**Win32-"t- \_ remotecontrolsetting"**</span><span class="sxs-lookup"><span data-stu-id="7b4d5-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 

