---
description: Die iscardauth-Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines Smartcard-Dienstanbieters befolgt werden kann. Die iscardauth-Schnittstelle kann verwendet werden, um von einer Smartcard unterstützte Authentifizierungsdienste verfügbar zu machen.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Iscardauth-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484723"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="b5e76-103">Iscardauth-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b5e76-103">ISCardAuth interface</span></span>

<span data-ttu-id="b5e76-104">\[Die **iscardauth** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b5e76-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b5e76-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b5e76-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5e76-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b5e76-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b5e76-107">Die **iscardauth** -Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b5e76-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="b5e76-108">Die **iscardauth** -Schnittstelle kann verwendet werden, um von einer Smartcard unterstützte Authentifizierungsdienste verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b5e76-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="b5e76-109">Zu diesen Diensten gehören die Anwendungs Authentifizierung, die Smartcard-Authentifizierung und die Benutzerauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="b5e76-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="b5e76-110">Das folgende Beispiel zeigt eine typische Verwendung der **iscardauth** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5e76-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="b5e76-111">**So verwenden Sie iscardauth**</span><span class="sxs-lookup"><span data-stu-id="b5e76-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="b5e76-112">Erstellen Sie eine **iscardauth** -Schnittstelle (über die entsprechende [**iscardmanage**](iscardmanage.md) -Schnittstellen Methode).</span><span class="sxs-lookup"><span data-stu-id="b5e76-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="b5e76-113">Aufrufen der entsprechenden **iscardauth** -Methode (app-Authentifizierung, [**getchallenge**](iscardauth-getchallenge.md), [**ICC \_**](iscardauth-icc-auth.md)-Authentifizierung oder [**Benutzer \_**](iscardauth-user-auth.md)Authentifizierung).[**\_**](iscardauth-app-auth.md)</span><span class="sxs-lookup"><span data-stu-id="b5e76-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="b5e76-114">Geben Sie die **iscardauth** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="b5e76-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="b5e76-115">Member</span><span class="sxs-lookup"><span data-stu-id="b5e76-115">Members</span></span>

<span data-ttu-id="b5e76-116">Die **iscardauth** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5e76-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b5e76-117">**Iscardauth** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b5e76-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="b5e76-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="b5e76-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b5e76-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="b5e76-119">Methods</span></span>

<span data-ttu-id="b5e76-120">Die **iscardauth** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b5e76-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="b5e76-121">Methode</span><span class="sxs-lookup"><span data-stu-id="b5e76-121">Method</span></span>                                          | <span data-ttu-id="b5e76-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5e76-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5e76-123">**APP \_ -Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="b5e76-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="b5e76-124">Ermöglicht es der Anwendung, sich mit einem Challenge/Signature-Protokoll zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e76-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="b5e76-125">**Getchallenge**</span><span class="sxs-lookup"><span data-stu-id="b5e76-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="b5e76-126">Gibt eine Herausforderung von der Smartcard zurück.</span><span class="sxs-lookup"><span data-stu-id="b5e76-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="b5e76-127">**ICC \_ -Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="b5e76-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="b5e76-128">Ermöglicht es einer Anwendung, die Smartcard zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e76-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="b5e76-129">**Benutzer \_ Authentifizierung**</span><span class="sxs-lookup"><span data-stu-id="b5e76-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="b5e76-130">Ermöglicht den Zugriff auf Benutzer Authentifizierungsdienste.</span><span class="sxs-lookup"><span data-stu-id="b5e76-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="b5e76-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5e76-131">Requirements</span></span>



| <span data-ttu-id="b5e76-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5e76-132">Requirement</span></span> | <span data-ttu-id="b5e76-133">Wert</span><span class="sxs-lookup"><span data-stu-id="b5e76-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5e76-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5e76-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e76-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5e76-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b5e76-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5e76-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e76-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5e76-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b5e76-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b5e76-138">End of client support</span></span><br/>    | <span data-ttu-id="b5e76-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5e76-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b5e76-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b5e76-140">End of server support</span></span><br/>    | <span data-ttu-id="b5e76-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5e76-141">Windows Server 2003</span></span><br/>                       |



 

 
