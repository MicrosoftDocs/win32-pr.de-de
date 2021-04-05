---
title: EmailAction-Objekt
description: Skript Objekt, das eine Aktion darstellt, die eine e-Mail-Nachricht sendet.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Emailaction-Objekt Taskplaner
- Emailaction-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a339a1549b76f61499b7192a48edc7c1b86a6c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859186"
---
# <a name="emailaction-object"></a><span data-ttu-id="08986-105">EmailAction-Objekt</span><span class="sxs-lookup"><span data-stu-id="08986-105">EmailAction object</span></span>

<span data-ttu-id="08986-106">\[Dieses Objekt wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="08986-106">\[This object is no longer supported.</span></span> <span data-ttu-id="08986-107">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.\]</span><span class="sxs-lookup"><span data-stu-id="08986-107">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="08986-108">Skript Objekt, das eine Aktion darstellt, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="08986-108">Scripting object that represents an action that sends an email message.</span></span>

## <a name="members"></a><span data-ttu-id="08986-109">Member</span><span class="sxs-lookup"><span data-stu-id="08986-109">Members</span></span>

<span data-ttu-id="08986-110">Das **emailaction** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="08986-110">The **EmailAction** object has these types of members:</span></span>

-   [<span data-ttu-id="08986-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08986-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08986-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08986-112">Properties</span></span>

<span data-ttu-id="08986-113">Das **emailaction** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="08986-113">The **EmailAction** object has these properties.</span></span>



| <span data-ttu-id="08986-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08986-114">Property</span></span>                                                    | <span data-ttu-id="08986-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="08986-115">Access type</span></span>           | <span data-ttu-id="08986-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08986-116">Description</span></span>                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08986-117">**Attachments**</span><span class="sxs-lookup"><span data-stu-id="08986-117">**Attachments**</span></span>](emailaction-attachments.md)<br/>   | <span data-ttu-id="08986-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-118">Read/write</span></span><br/> | <span data-ttu-id="08986-119">Ruft ein Array von Anlagen ab, das mit der e-Mail gesendet wird, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="08986-119">Gets or sets an array of attachments that is sent with the email message.</span></span><br/>                      |
| [<span data-ttu-id="08986-120">**Bcc**</span><span class="sxs-lookup"><span data-stu-id="08986-120">**Bcc**</span></span>](emailaction-bcc.md)<br/>                   | <span data-ttu-id="08986-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-121">Read/write</span></span><br/> | <span data-ttu-id="08986-122">Dient zum Abrufen oder Festlegen der e-Mail-Adressen, die Sie in der e-Mail-Nachricht für Bcc angeben möchten</span><span class="sxs-lookup"><span data-stu-id="08986-122">Gets or sets the email address or addresses that you want to Bcc in the email message.</span></span><br/>         |
| [<span data-ttu-id="08986-123">**Text**</span><span class="sxs-lookup"><span data-stu-id="08986-123">**Body**</span></span>](emailaction-body.md)<br/>                 | <span data-ttu-id="08986-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-124">Read/write</span></span><br/> | <span data-ttu-id="08986-125">Ruft den Textkörper der e-Mail ab, der die e-Mail enthält, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="08986-125">Gets or sets the body of the email that contains the email message.</span></span><br/>                            |
| [<span data-ttu-id="08986-126">**125**</span><span class="sxs-lookup"><span data-stu-id="08986-126">**Cc**</span></span>](emailaction-cc.md)<br/>                     | <span data-ttu-id="08986-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-127">Read/write</span></span><br/> | <span data-ttu-id="08986-128">Dient zum Abrufen oder Festlegen der e-Mail-Adressen, die Sie in der e-Mail-Nachricht CC CC angeben möchten</span><span class="sxs-lookup"><span data-stu-id="08986-128">Gets or sets the email address or addresses that you want to Cc in the email message.</span></span><br/>          |
| [<span data-ttu-id="08986-129">**From**</span><span class="sxs-lookup"><span data-stu-id="08986-129">**From**</span></span>](emailaction-from.md)<br/>                 | <span data-ttu-id="08986-130">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-130">Read/write</span></span><br/> | <span data-ttu-id="08986-131">Ruft die e-Mail-Adresse ab, von der Sie die e-Mail senden möchten, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="08986-131">Gets or sets the email address that you want to send the email from.</span></span><br/>                           |
| [<span data-ttu-id="08986-132">**Headerfields**</span><span class="sxs-lookup"><span data-stu-id="08986-132">**HeaderFields**</span></span>](emailaction-headerfields.md)<br/> | <span data-ttu-id="08986-133">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-133">Read/write</span></span><br/> | <span data-ttu-id="08986-134">Ruft die Header Informationen in der e-Mail ab, die Sie senden möchten, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="08986-134">Gets or sets the header information in the email that you want to send.</span></span><br/>                        |
| [<span data-ttu-id="08986-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="08986-135">**Id**</span></span>](action-id.md)<br/>                          | <span data-ttu-id="08986-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-136">Read/write</span></span><br/> | <span data-ttu-id="08986-137">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="08986-137">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="08986-138">Ruft den Bezeichner der Aktion ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="08986-138">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="08986-139">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="08986-139">**ReplyTo**</span></span>](emailaction-replyto.md)<br/>           | <span data-ttu-id="08986-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-140">Read/write</span></span><br/> | <span data-ttu-id="08986-141">Ruft die e-Mail-Adresse ab, der Sie antworten möchten, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="08986-141">Gets or sets the email address that you want to reply to.</span></span><br/>                                      |
| [<span data-ttu-id="08986-142">**Servers**</span><span class="sxs-lookup"><span data-stu-id="08986-142">**Server**</span></span>](emailaction-server.md)<br/>             | <span data-ttu-id="08986-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-143">Read/write</span></span><br/> | <span data-ttu-id="08986-144">Ruft den Namen des Servers ab, der zum Senden von e-Mails verwendet wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="08986-144">Gets or sets the name of the server that you use to send email from.</span></span><br/>                           |
| [<span data-ttu-id="08986-145">**Subject**</span><span class="sxs-lookup"><span data-stu-id="08986-145">**Subject**</span></span>](emailaction-subject.md)<br/>           | <span data-ttu-id="08986-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-146">Read/write</span></span><br/> | <span data-ttu-id="08986-147">Ruft den Betreff der e-Mail-Nachricht ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="08986-147">Gets or sets the subject of the email message.</span></span><br/>                                                 |
| [<span data-ttu-id="08986-148">**An**</span><span class="sxs-lookup"><span data-stu-id="08986-148">**To**</span></span>](emailaction-to.md)<br/>                     | <span data-ttu-id="08986-149">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="08986-149">Read/write</span></span><br/> | <span data-ttu-id="08986-150">Ruft die e-Mail-Adresse oder Adressen ab, an die die e-Mail gesendet werden soll, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="08986-150">Gets or sets the email address or addresses that you want to send the email to.</span></span><br/>                |
| [<span data-ttu-id="08986-151">**type**</span><span class="sxs-lookup"><span data-stu-id="08986-151">**Type**</span></span>](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | <span data-ttu-id="08986-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="08986-152">Read-only</span></span><br/>  | <span data-ttu-id="08986-153">Wird vom [**Aktions**](action.md) Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="08986-153">Inherited from [**Action**](action.md) object.</span></span> <span data-ttu-id="08986-154">Ruft den Typ der Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="08986-154">Gets the type of the action.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="08986-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08986-155">Remarks</span></span>

<span data-ttu-id="08986-156">Die e-Mail-Aktion muss einen gültigen Wert für die Eigenschaften " [**Server**](emailaction-server.md)", " [**from**](emailaction-from.md)" und " [**to**](emailaction-to.md) " und " [**CC**](emailaction-cc.md) " aufweisen, damit die Aufgabe ordnungsgemäß registriert und ausgeführt</span><span class="sxs-lookup"><span data-stu-id="08986-156">The email action must have a valid value for the [**Server**](emailaction-server.md), [**From**](emailaction-from.md), and [**To**](emailaction-to.md) or [**Cc**](emailaction-cc.md) properties for the task to register and run correctly.</span></span>

<span data-ttu-id="08986-157">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird eine e-Mail-Aktion mithilfe des [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) -Elements des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="08986-157">When reading or writing your own XML for a task, an email action is specified using the [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="08986-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08986-158">Examples</span></span>

<span data-ttu-id="08986-159">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [Event-auslöserbeispiel (Skripterstellung)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08986-159">For more information and example code for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="08986-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08986-160">Requirements</span></span>



| <span data-ttu-id="08986-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08986-161">Requirement</span></span> | <span data-ttu-id="08986-162">Wert</span><span class="sxs-lookup"><span data-stu-id="08986-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08986-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08986-163">Minimum supported client</span></span><br/> | <span data-ttu-id="08986-164">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08986-164">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="08986-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08986-165">Minimum supported server</span></span><br/> | <span data-ttu-id="08986-166">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08986-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08986-167">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="08986-167">End of client support</span></span><br/>    | <span data-ttu-id="08986-168">Windows 7</span><span class="sxs-lookup"><span data-stu-id="08986-168">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="08986-169">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="08986-169">End of server support</span></span><br/>    | <span data-ttu-id="08986-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08986-170">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="08986-171">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="08986-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="08986-172"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08986-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08986-173">DLL</span><span class="sxs-lookup"><span data-stu-id="08986-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08986-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08986-174"><dt>Taskschd.dll</dt></span></span> </dl> |



 

