---
description: Die Klasse smtpeer-Consumer sendet eine e-Mail-Nachricht mit Simple Mail Transfer Protocol (SMTP), wenn ein Ereignis an Sie übermittelt wird.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Smtpventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218306"
---
# <a name="smtpeventconsumer-class"></a><span data-ttu-id="987c5-103">Smtpventconsumer-Klasse</span><span class="sxs-lookup"><span data-stu-id="987c5-103">SMTPEventConsumer class</span></span>

<span data-ttu-id="987c5-104">Die Klasse **smtpeer-Consumer** sendet eine e-Mail-Nachricht mit Simple Mail Transfer Protocol (SMTP), wenn ein Ereignis an Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="987c5-104">The **SMTPEventConsumer** class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="987c5-105">Ein SMTP-Server muss im Netzwerk vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="987c5-105">An SMTP server must exist on the network.</span></span> <span data-ttu-id="987c5-106">Die Klasse smtpventconsumer unterstützt keine Anlagen.</span><span class="sxs-lookup"><span data-stu-id="987c5-106">The SMTPEventConsumer class does not support attachments.</span></span> <span data-ttu-id="987c5-107">Die Codierung der e-Mail-Nachricht muss "US-ASCII" lauten.</span><span class="sxs-lookup"><span data-stu-id="987c5-107">The encoding of the email message must be US-ASCII.</span></span>

<span data-ttu-id="987c5-108">Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="987c5-108">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="987c5-109">Ein Beispiel für die Verwendung von **smtpeer-Consumer** , um einen Consumer zu erstellen, finden Sie unter [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="987c5-109">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="987c5-110">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="987c5-110">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="987c5-111">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="987c5-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="987c5-112">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="987c5-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="987c5-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="987c5-113">Syntax</span></span>

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a><span data-ttu-id="987c5-114">Member</span><span class="sxs-lookup"><span data-stu-id="987c5-114">Members</span></span>

<span data-ttu-id="987c5-115">Die Klasse **smtpventconsumer** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="987c5-115">The **SMTPEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="987c5-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="987c5-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="987c5-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="987c5-117">Properties</span></span>

<span data-ttu-id="987c5-118">Die Klasse **smtpventconsumer** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="987c5-118">The **SMTPEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="987c5-119">**Bccline**</span><span class="sxs-lookup"><span data-stu-id="987c5-119">**BccLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-122">Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer standardmäßigen Zeichen folgen Vorlage, an die die Nachricht als Blind Kopie gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="987c5-122">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a blind carbon copy.</span></span> <span data-ttu-id="987c5-123">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="987c5-123">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-124">**Ccline**</span><span class="sxs-lookup"><span data-stu-id="987c5-124">**CcLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-127">Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer standardmäßigen Zeichen folgen Vorlage, an die die Nachricht als Kopie der Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="987c5-127">A list of addresses, separated by a comma or semicolon, in the format of a standard string template to which the message is sent as a carbon copy.</span></span> <span data-ttu-id="987c5-128">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="987c5-128">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-129">**"Kreatorsid"**</span><span class="sxs-lookup"><span data-stu-id="987c5-129">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-130">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="987c5-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="987c5-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-132">Sicherheits-ID (SID), die den Benutzer, der einen Filter erstellt, eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="987c5-132">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="987c5-133">WMI speichert die SID des Benutzers, der eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) oder die Administrator-SID erstellt, je nach Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="987c5-133">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="987c5-134">Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="987c5-134">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="987c5-135">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="987c5-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="987c5-136">**Fromline**</span><span class="sxs-lookup"><span data-stu-id="987c5-136">**FromLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-139">Aus Zeile einer e-Mail-Nachricht im Format einer Standard Zeichenfolgen-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="987c5-139">From line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="987c5-140">Wenn der Wert **null** ist, wird eine from-Zeile in der Form "Winmgmt@*MachineName*" erstellt.</span><span class="sxs-lookup"><span data-stu-id="987c5-140">If **NULL**, a From line is constructed in the form of "WinMgmt@*MachineName*".</span></span>

</dd> <dt>

<span data-ttu-id="987c5-141">**Headerfields**</span><span class="sxs-lookup"><span data-stu-id="987c5-141">**HeaderFields**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-142">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="987c5-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="987c5-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-144">Ein Array von Header Feldern, die ohne Interpretation in eine e-Mail-Nachricht eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="987c5-144">Array of header fields that are inserted into an email message without interpretation.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-145">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="987c5-145">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-148">Der Name des Computers, an den Windows-Verwaltungsinstrumentation (WMI) Ereignisse sendet.</span><span class="sxs-lookup"><span data-stu-id="987c5-148">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="987c5-149">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="987c5-149">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="987c5-150">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="987c5-150">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="987c5-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-153">Maximale Warteschlange für einen bestimmten Consumer in Bytes.</span><span class="sxs-lookup"><span data-stu-id="987c5-153">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="987c5-154">Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="987c5-154">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="987c5-155">**Meldung**</span><span class="sxs-lookup"><span data-stu-id="987c5-155">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-158">Standard mäßige Zeichen folgen Vorlage, die den Textkörper einer e-Mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="987c5-158">Standard string template that contains the body of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-159">**Name**</span><span class="sxs-lookup"><span data-stu-id="987c5-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="987c5-162">Qualifizierer: [ **Schlüssel**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="987c5-162">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="987c5-163">Eindeutiger Bezeichner für den Ereignisconsumer.</span><span class="sxs-lookup"><span data-stu-id="987c5-163">Unique identifier for the event consumer.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-164">**Replytoline**</span><span class="sxs-lookup"><span data-stu-id="987c5-164">**ReplyToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-167">Antwort an Zeile einer e-Mail-Nachricht im Format einer Standard Zeichenfolgen-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="987c5-167">Reply-to line of an email message in the format of a standard string template.</span></span> <span data-ttu-id="987c5-168">Wenn der Wert **null** ist, wird keine Antwort an Zeile verwendet.</span><span class="sxs-lookup"><span data-stu-id="987c5-168">If **NULL**, no Reply-to line is used.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-169">**SMTPServer**</span><span class="sxs-lookup"><span data-stu-id="987c5-169">**SMTPServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-172">Der Name des SMTP-Servers, über den eine e-Mail gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="987c5-172">Name of the SMTP server through which an email is sent.</span></span> <span data-ttu-id="987c5-173">Zulässige Namen sind eine IP-Adresse oder ein DNS-oder NetBIOS-Name.</span><span class="sxs-lookup"><span data-stu-id="987c5-173">Permissible names are an IP address, or a DNS or NetBIOS name.</span></span> <span data-ttu-id="987c5-174">Diese Eigenschaft darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="987c5-174">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-175">**Subject**</span><span class="sxs-lookup"><span data-stu-id="987c5-175">**Subject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-178">Standard Zeichen folgen Vorlage, die den Betreff einer e-Mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="987c5-178">Standard string template that contains the subject of an email message.</span></span>

</dd> <dt>

<span data-ttu-id="987c5-179">**Unter Toline**</span><span class="sxs-lookup"><span data-stu-id="987c5-179">**ToLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987c5-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="987c5-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="987c5-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="987c5-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="987c5-182">Eine Liste von Adressen, getrennt durch ein Komma oder Semikolon, im Format einer standardmäßigen Zeichen folgen Vorlage, die angibt, wohin die Nachricht gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="987c5-182">A list of addresses, separated by a comma or semicolon, in the format of a standard string template that identifies where the message is to be sent.</span></span> <span data-ttu-id="987c5-183">Weitere Informationen finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="987c5-183">For more information, see the Remarks section of this topic.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="987c5-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="987c5-184">Remarks</span></span>

<span data-ttu-id="987c5-185">Die Klasse smtpeer-Consumer wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="987c5-185">The SMTPEventConsumer class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="987c5-186">Einige der Eigenschaften **Toline**, **ccline** oder **bccline** können **null** sein, Sie können jedoch nicht alle **null** sein.</span><span class="sxs-lookup"><span data-stu-id="987c5-186">Some of the **ToLine**, **CcLine**, or **BccLine** properties can be **NULL**, but they cannot all be **NULL**.</span></span>

<span data-ttu-id="987c5-187">Der Empfang eines Fehlerrückgabe Codes vom SMTP-Dienst wird als Fehler betrachtet.</span><span class="sxs-lookup"><span data-stu-id="987c5-187">Receiving an error return code from the SMTP service is considered a failure.</span></span>

## <a name="examples"></a><span data-ttu-id="987c5-188">Beispiele</span><span class="sxs-lookup"><span data-stu-id="987c5-188">Examples</span></span>

<span data-ttu-id="987c5-189">Ein Beispiel für die Verwendung von **smtpeer-Consumer** , um einen Consumer zu erstellen, finden Sie unter [Senden von e-Mails auf der Grundlage eines Ereignisses](sending-e-mail-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="987c5-189">For an example of using **SMTPEventConsumer** to create a consumer, see [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md).</span></span> <span data-ttu-id="987c5-190">Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.</span><span class="sxs-lookup"><span data-stu-id="987c5-190">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="987c5-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="987c5-191">Requirements</span></span>



| <span data-ttu-id="987c5-192">Anforderung</span><span class="sxs-lookup"><span data-stu-id="987c5-192">Requirement</span></span> | <span data-ttu-id="987c5-193">Wert</span><span class="sxs-lookup"><span data-stu-id="987c5-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="987c5-194">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="987c5-194">Minimum supported client</span></span><br/> | <span data-ttu-id="987c5-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987c5-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="987c5-196">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="987c5-196">Minimum supported server</span></span><br/> | <span data-ttu-id="987c5-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="987c5-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="987c5-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="987c5-198">Namespace</span></span><br/>                | <span data-ttu-id="987c5-199">Stamm \\ Abonnement</span><span class="sxs-lookup"><span data-stu-id="987c5-199">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="987c5-200">MOF</span><span class="sxs-lookup"><span data-stu-id="987c5-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="987c5-201"><dt>Smtpcons. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="987c5-201"><dt>Smtpcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="987c5-202">DLL</span><span class="sxs-lookup"><span data-stu-id="987c5-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="987c5-203"><dt>Smtpcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="987c5-203"><dt>Smtpcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987c5-204">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="987c5-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987c5-205">**\_\_Eventconsumer**</span><span class="sxs-lookup"><span data-stu-id="987c5-205">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="987c5-206">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="987c5-206">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="987c5-207">Senden von e-Mails auf der Grundlage eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="987c5-207">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="987c5-208">Erstellen eines logischen Consumers</span><span class="sxs-lookup"><span data-stu-id="987c5-208">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="987c5-209">Empfangen von Ereignissen zu allen Zeitpunkten</span><span class="sxs-lookup"><span data-stu-id="987c5-209">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 




