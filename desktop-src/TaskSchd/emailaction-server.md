---
title: Emailaction. Server-Eigenschaft
description: Bei der Skripterstellung wird der Name des SMTP-Servers abgerufen oder festgelegt, den Sie zum Senden von e-Mail verwenden.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Taskplaner der Server Eigenschaft
- Server Eigenschaft Taskplaner, emailaction-Objekt
- Emailaction-Objekt Taskplaner, Server Eigenschaft
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340768"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="afc1a-106">Emailaction. Server-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="afc1a-106">EmailAction.Server property</span></span>

<span data-ttu-id="afc1a-107">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="afc1a-107">\[This object is no longer supported.</span></span> <span data-ttu-id="afc1a-108">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="afc1a-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="afc1a-109">Bei der Skripterstellung wird der Name des SMTP-Servers abgerufen oder festgelegt, den Sie zum Senden von e-Mail verwenden.</span><span class="sxs-lookup"><span data-stu-id="afc1a-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="afc1a-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="afc1a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc1a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="afc1a-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="afc1a-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="afc1a-112">Property value</span></span>

<span data-ttu-id="afc1a-113">Der Name des Servers, der zum Senden von e-Mails verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="afc1a-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc1a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc1a-114">Remarks</span></span>

<span data-ttu-id="afc1a-115">Stellen Sie sicher, dass der SMTP-Server, der die e-Mail sendet, korrekt eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="afc1a-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="afc1a-116">E-Mail wird mithilfe der NTLM-Authentifizierung für Windows-SMTP-Server gesendet. Dies bedeutet, dass die zum Ausführen der Aufgabe verwendeten Sicherheits Anmelde Informationen auch über Berechtigungen auf dem SMTP-Server verfügen müssen, um eine e-Mail zu senden.</span><span class="sxs-lookup"><span data-stu-id="afc1a-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="afc1a-117">Wenn es sich beim SMTP-Server um einen nicht auf Windows basierenden Server handelt, wird die e-Mail gesendet, wenn der Server den anonymen Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="afc1a-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="afc1a-118">Weitere Informationen zum Einrichten des SMTP-Servers finden Sie unter [SMTP-Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true). Weitere Informationen zum Verwalten von SMTP-Servereinstellungen finden Sie unter [SMTP-Verwaltung](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="afc1a-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="afc1a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc1a-119">Requirements</span></span>



| <span data-ttu-id="afc1a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc1a-120">Requirement</span></span> | <span data-ttu-id="afc1a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="afc1a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc1a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="afc1a-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc1a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="afc1a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="afc1a-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc1a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afc1a-126">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="afc1a-126">End of client support</span></span><br/>    | <span data-ttu-id="afc1a-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="afc1a-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="afc1a-128">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="afc1a-128">End of server support</span></span><br/>    | <span data-ttu-id="afc1a-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afc1a-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="afc1a-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="afc1a-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="afc1a-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="afc1a-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="afc1a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="afc1a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc1a-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc1a-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc1a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afc1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc1a-135">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="afc1a-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="afc1a-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="afc1a-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

