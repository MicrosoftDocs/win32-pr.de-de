---
description: Wenn eine Anwendung die Anmelde Informations Verwaltungs-API verwendet, um Anmelde Informationen einzugeben, wird erwartet, dass der Benutzer die Informationen eingibt, die vom Betriebssystem oder von der Anwendung überprüft werden können.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Benutzernamen Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349591"
---
# <a name="user-name-formats"></a><span data-ttu-id="1ff32-103">Benutzernamen Formate</span><span class="sxs-lookup"><span data-stu-id="1ff32-103">User Name Formats</span></span>

<span data-ttu-id="1ff32-104">Wenn eine Anwendung die Anmelde Informations Verwaltungs-API verwendet, um Anmelde Informationen einzugeben, wird erwartet, dass der Benutzer die Informationen eingibt, die vom Betriebssystem oder von der Anwendung überprüft werden können.</span><span class="sxs-lookup"><span data-stu-id="1ff32-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="1ff32-105">Der Benutzer kann Informationen zu Domänen Anmelde Informationen in einem der folgenden Formate angeben:</span><span class="sxs-lookup"><span data-stu-id="1ff32-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="1ff32-106">Benutzerprinzipalname</span><span class="sxs-lookup"><span data-stu-id="1ff32-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="1ff32-107">Anmelde Name auf der gleichen Ebene</span><span class="sxs-lookup"><span data-stu-id="1ff32-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="1ff32-108">Benutzerprinzipalname</span><span class="sxs-lookup"><span data-stu-id="1ff32-108">User Principal Name</span></span>

<span data-ttu-id="1ff32-109">Das UPN-Format ( [*User Principal Name, Benutzer Prinzipal Name*](../secgloss/u-gly.md) ) wird verwendet, um einen Internet Namen anzugeben, z <b>UserName@Example.Microsoft.com</b> . b..</span><span class="sxs-lookup"><span data-stu-id="1ff32-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="1ff32-110">In der folgenden Tabelle werden die Teile eines UPN zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="1ff32-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="1ff32-111">Teil</span><span class="sxs-lookup"><span data-stu-id="1ff32-111">Part</span></span>                                                        | <span data-ttu-id="1ff32-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1ff32-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1ff32-113">Der Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="1ff32-113">User account name.</span></span> <span data-ttu-id="1ff32-114">Wird auch als Anmelde Name bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ff32-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="1ff32-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="1ff32-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="1ff32-116">Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="1ff32-116">Separator.</span></span> <span data-ttu-id="1ff32-117">Ein Zeichenliteral, das at-Zeichen (@).</span><span class="sxs-lookup"><span data-stu-id="1ff32-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="1ff32-118">UPN-Suffix.</span><span class="sxs-lookup"><span data-stu-id="1ff32-118">UPN suffix.</span></span> <span data-ttu-id="1ff32-119">Wird auch als Domänen Name bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ff32-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="1ff32-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="1ff32-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="1ff32-121">Ein UPN kann implizit oder explizit definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ff32-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="1ff32-122">Ein impliziter UPN hat die Form <b>UserName@DNSDomainName.com</b> .</span><span class="sxs-lookup"><span data-stu-id="1ff32-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="1ff32-123">Ein impliziter UPN ist immer mit dem Benutzerkonto verknüpft, auch wenn kein expliziter UPN definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1ff32-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="1ff32-124">Ein expliziter UPN weist das Format auf, wobei die Namen-und suffixzeichenfolgen <i><b>Name@Suffix</b></i> explizit vom Administrator definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1ff32-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="1ff32-125">Anmelde Name Down-Level</span><span class="sxs-lookup"><span data-stu-id="1ff32-125">Down-Level Logon Name</span></span>

<span data-ttu-id="1ff32-126">Das Format der untergeordneten Anmelde Namen wird verwendet, um eine Domäne und ein Benutzerkonto in dieser Domäne anzugeben, z. b. <i><b>Domäne \\ Benutzername</b></i>.</span><span class="sxs-lookup"><span data-stu-id="1ff32-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="1ff32-127">In der folgenden Tabelle werden die Teile eines untergeordneten Anmelde namens zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="1ff32-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="1ff32-128">Teil</span><span class="sxs-lookup"><span data-stu-id="1ff32-128">Part</span></span>                                                           | <span data-ttu-id="1ff32-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1ff32-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="1ff32-130">NetBIOS-Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="1ff32-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="1ff32-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="1ff32-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="1ff32-132">Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="1ff32-132">Separator.</span></span> <span data-ttu-id="1ff32-133">Ein Zeichenliterals, der umgekehrte Schrägstrich ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="1ff32-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="1ff32-134">Der Name des Benutzerkontos.</span><span class="sxs-lookup"><span data-stu-id="1ff32-134">User account name.</span></span> <span data-ttu-id="1ff32-135">Wird auch als Anmelde Name bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1ff32-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="1ff32-136">*UserName*</span><span class="sxs-lookup"><span data-stu-id="1ff32-136">*UserName*</span></span><br/> |



 

 

 
