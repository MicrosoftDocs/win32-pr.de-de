---
title: komplexer sendemailtype-Typ
description: Definiert den Aktionstyp, der verwendet wird, um anzugeben, dass eine e-Mail gesendet wird, wenn eine Aufgabe ausgeführt wird. Dieser Typ definiert alle Elemente, die zum Modellieren der e-Mail-Nachricht verwendet werden.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- komplexer sendemailtype-Typ Taskplaner
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341040"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="a1e9a-105">komplexer sendemailtype-Typ</span><span class="sxs-lookup"><span data-stu-id="a1e9a-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="a1e9a-106">Definiert den Aktionstyp, der verwendet wird, um anzugeben, dass eine e-Mail gesendet wird, wenn eine Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="a1e9a-107">Dieser Typ definiert alle Elemente, die zum Modellieren der e-Mail-Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a1e9a-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a1e9a-108">Child elements</span></span>



| <span data-ttu-id="a1e9a-109">Element</span><span class="sxs-lookup"><span data-stu-id="a1e9a-109">Element</span></span>                                                                        | <span data-ttu-id="a1e9a-110">type</span><span class="sxs-lookup"><span data-stu-id="a1e9a-110">Type</span></span>                                                                         | <span data-ttu-id="a1e9a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1e9a-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1e9a-112">**Attachments**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="a1e9a-113">**attachmentstype**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="a1e9a-114">Gibt eine Liste der Anlagen in der e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="a1e9a-115">**Bcc**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="a1e9a-116">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-116">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-117">Gibt die e-Mail-Adressen an, die in der Bcc-Zeile einer e-Mail verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="a1e9a-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="a1e9a-119">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-119">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-120">Gibt den Text im Textkörper der e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="a1e9a-121">**125**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="a1e9a-122">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-122">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-123">Gibt die e-Mail-Adressen an, die in der CC-Zeile einer e-Mail verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="a1e9a-124">**From**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="a1e9a-125">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-125">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-126">Gibt die e-Mail-Adresse des Absenders an.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="a1e9a-127">**Headerfields**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="a1e9a-128">**headerfieldstype**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="a1e9a-129">Gibt die Header Felder und deren Werte an, die im Header der e-Mail-Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="a1e9a-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="a1e9a-131">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-131">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-132">Gibt die e-Mail-Adressen an, auf die in der e-Mail geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="a1e9a-133">**Servers**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="a1e9a-134">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="a1e9a-135">Gibt den e-Mail-Server an, mit dem die e-Mail gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="a1e9a-136">**Subject**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="a1e9a-137">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-137">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-138">Gibt den Betreff der e-Mail-Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="a1e9a-139">**An**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="a1e9a-140">**string**</span><span class="sxs-lookup"><span data-stu-id="a1e9a-140">**string**</span></span>                                                                   | <span data-ttu-id="a1e9a-141">Gibt die e-Mail-Adressen an, an die die e-Mail gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="a1e9a-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="a1e9a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1e9a-142">Requirements</span></span>



| <span data-ttu-id="a1e9a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1e9a-143">Requirement</span></span> | <span data-ttu-id="a1e9a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="a1e9a-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a1e9a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1e9a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e9a-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1e9a-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1e9a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1e9a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e9a-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1e9a-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





