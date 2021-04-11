---
title: SendEmail (actionGroup)-Element
description: Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- SendEmail-Element Taskplaner
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956920"
---
# <a name="sendemail-actiongroup-element"></a><span data-ttu-id="f54b3-104">SendEmail (actionGroup)-Element</span><span class="sxs-lookup"><span data-stu-id="f54b3-104">SendEmail (actionGroup) Element</span></span>

<span data-ttu-id="f54b3-105">Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="f54b3-105">Represents an action that sends an email message.</span></span>

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

<span data-ttu-id="f54b3-106">Das **SendEmail** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="f54b3-106">The **SendEmail** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f54b3-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="f54b3-107">Parent element</span></span>



| <span data-ttu-id="f54b3-108">Element</span><span class="sxs-lookup"><span data-stu-id="f54b3-108">Element</span></span>                                                         | <span data-ttu-id="f54b3-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="f54b3-109">Derived from</span></span>                                                       | <span data-ttu-id="f54b3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f54b3-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f54b3-111">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="f54b3-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="f54b3-112">**Aktions sType**</span><span class="sxs-lookup"><span data-stu-id="f54b3-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="f54b3-113">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f54b3-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f54b3-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f54b3-114">Child elements</span></span>



| <span data-ttu-id="f54b3-115">Element</span><span class="sxs-lookup"><span data-stu-id="f54b3-115">Element</span></span>                                                                        | <span data-ttu-id="f54b3-116">type</span><span class="sxs-lookup"><span data-stu-id="f54b3-116">Type</span></span>                                                                         | <span data-ttu-id="f54b3-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f54b3-117">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f54b3-118">**Attachments**</span><span class="sxs-lookup"><span data-stu-id="f54b3-118">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="f54b3-119">**attachmentstype**</span><span class="sxs-lookup"><span data-stu-id="f54b3-119">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="f54b3-120">Gibt eine Liste der Anlagen in der e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f54b3-120">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="f54b3-121">**Bcc**</span><span class="sxs-lookup"><span data-stu-id="f54b3-121">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="f54b3-122">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-122">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-123">Gibt die e-Mail-Adressen an, die in der Bcc-Zeile einer e-Mail verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f54b3-123">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="f54b3-124">**Text**</span><span class="sxs-lookup"><span data-stu-id="f54b3-124">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="f54b3-125">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-125">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-126">Gibt den Text im Textkörper der e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f54b3-126">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="f54b3-127">**125**</span><span class="sxs-lookup"><span data-stu-id="f54b3-127">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="f54b3-128">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-128">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-129">Gibt die e-Mail-Adressen an, die in der CC-Zeile einer e-Mail verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f54b3-129">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="f54b3-130">**From**</span><span class="sxs-lookup"><span data-stu-id="f54b3-130">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="f54b3-131">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-131">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-132">Gibt die e-Mail-Adresse des Absenders an.</span><span class="sxs-lookup"><span data-stu-id="f54b3-132">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="f54b3-133">**Headerfields**</span><span class="sxs-lookup"><span data-stu-id="f54b3-133">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="f54b3-134">**headerfieldstype**</span><span class="sxs-lookup"><span data-stu-id="f54b3-134">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="f54b3-135">Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f54b3-135">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="f54b3-136">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="f54b3-136">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="f54b3-137">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-137">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-138">Gibt die e-Mail-Adressen an, auf die in der e-Mail geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="f54b3-138">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="f54b3-139">**Servers**</span><span class="sxs-lookup"><span data-stu-id="f54b3-139">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="f54b3-140">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="f54b3-140">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="f54b3-141">Gibt den e-Mail-Server an, mit dem die e-Mail gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f54b3-141">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="f54b3-142">**Subject**</span><span class="sxs-lookup"><span data-stu-id="f54b3-142">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="f54b3-143">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-143">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-144">Gibt den Betreff der e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="f54b3-144">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="f54b3-145">**An**</span><span class="sxs-lookup"><span data-stu-id="f54b3-145">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="f54b3-146">**string**</span><span class="sxs-lookup"><span data-stu-id="f54b3-146">**string**</span></span>                                                                   | <span data-ttu-id="f54b3-147">Gibt die e-Mail-Adressen an, an die die e-Mail gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f54b3-147">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="f54b3-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f54b3-148">Remarks</span></span>

<span data-ttu-id="f54b3-149">Informationen zur C++-Entwicklung finden Sie unter der [**iemailaction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f54b3-149">For C++ development, see the [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) interface.</span></span>

<span data-ttu-id="f54b3-150">Informationen zur Skript Entwicklung finden Sie unter dem [**emailaction**](emailaction.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="f54b3-150">For script development, see the [**EmailAction**](emailaction.md) object.</span></span>

<span data-ttu-id="f54b3-151">**Windows 8 und Windows Server 2012:** Dieses Element wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="f54b3-151">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="f54b3-152">Verwenden Sie "IExecAction" mit dem PowerShell-Cmdlet " [**Send-Mail Message**](/powershell/module/microsoft.powershell.utility/send-mailmessage) " als Problem Umgehung.</span><span class="sxs-lookup"><span data-stu-id="f54b3-152">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.</span></span>

## <a name="examples"></a><span data-ttu-id="f54b3-153">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f54b3-153">Examples</span></span>

<span data-ttu-id="f54b3-154">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine e-Mail-Aktion angibt, finden Sie unter [Event triggerbeispiel (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f54b3-154">For a complete example of the XML for a task that specifies an email action, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f54b3-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f54b3-155">Requirements</span></span>



| <span data-ttu-id="f54b3-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f54b3-156">Requirement</span></span> | <span data-ttu-id="f54b3-157">Wert</span><span class="sxs-lookup"><span data-stu-id="f54b3-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f54b3-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f54b3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f54b3-159">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f54b3-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f54b3-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f54b3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f54b3-161">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f54b3-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f54b3-162">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f54b3-162">End of client support</span></span><br/>    | <span data-ttu-id="f54b3-163">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f54b3-163">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="f54b3-164">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f54b3-164">End of server support</span></span><br/>    | <span data-ttu-id="f54b3-165">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f54b3-165">Windows Server 2008 R2</span></span><br/>                    |



 

