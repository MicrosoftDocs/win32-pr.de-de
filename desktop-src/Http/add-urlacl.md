---
title: add urlacl
description: Reserviert die angegebene URL für Benutzer und Konten ohne Administratorrechte.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Hinzufügen von urlacl http
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103961537"
---
# <a name="add-urlacl"></a><span data-ttu-id="8e885-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="8e885-104">add urlacl</span></span>

<span data-ttu-id="8e885-105">Reserviert die angegebene URL für Benutzer und Konten ohne Administratorrechte.</span><span class="sxs-lookup"><span data-stu-id="8e885-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="8e885-106">Die freigegebene Zugriffs Steuerungs Liste (DACL) kann mithilfe eines Konto namens mit den Abhör-und delegatparametern oder mithilfe einer SDDL-Zeichenfolge (Security Deskriptor Definition Language) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e885-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="8e885-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e885-107">Parameters</span></span>

<dl> <span data-ttu-id="8e885-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] Zeichenfolge**
</dt> </span><span class="sxs-lookup"><span data-stu-id="8e885-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="8e885-109">Gibt die voll qualifizierte URL an.</span><span class="sxs-lookup"><span data-stu-id="8e885-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="8e885-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user =] Zeichenfolge**
</dt> </span><span class="sxs-lookup"><span data-stu-id="8e885-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="8e885-111">Gibt den Namen des Benutzers oder der Benutzergruppe an.</span><span class="sxs-lookup"><span data-stu-id="8e885-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="8e885-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[lauschen = {Yes \| No}\]**</span><span class="sxs-lookup"><span data-stu-id="8e885-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="8e885-113">Gibt einen der folgenden Werte an:</span><span class="sxs-lookup"><span data-stu-id="8e885-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="8e885-114">Ja: ermöglicht dem Benutzer das Registrieren von URLs.</span><span class="sxs-lookup"><span data-stu-id="8e885-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="8e885-115">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8e885-115">This is the default value.</span></span>
-   <span data-ttu-id="8e885-116">Nein: verweigert dem Benutzer das Registrieren von URLs.</span><span class="sxs-lookup"><span data-stu-id="8e885-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="8e885-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegat = {Yes \| No}\]**</span><span class="sxs-lookup"><span data-stu-id="8e885-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="8e885-118">Gibt einen der folgenden Werte an:</span><span class="sxs-lookup"><span data-stu-id="8e885-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="8e885-119">Ja: ermöglicht dem Benutzer das Delegieren von URLs.</span><span class="sxs-lookup"><span data-stu-id="8e885-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="8e885-120">Nein: verweigert dem Benutzer die Delegierung von URLs.</span><span class="sxs-lookup"><span data-stu-id="8e885-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="8e885-121">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8e885-121">This is the default value.</span></span>

<span data-ttu-id="8e885-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] Zeichenfolge**
</dt> </span><span class="sxs-lookup"><span data-stu-id="8e885-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="8e885-123">Gibt die SDDL-Zeichenfolge an, die die DACL beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8e885-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8e885-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e885-124">Examples</span></span>

* <span data-ttu-id="8e885-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="8e885-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="8e885-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="8e885-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="8e885-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="8e885-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="8e885-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8e885-128">See Also</span></span>

* [<span data-ttu-id="8e885-129">Netsh http-Befehle</span><span class="sxs-lookup"><span data-stu-id="8e885-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 