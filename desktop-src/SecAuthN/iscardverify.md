---
description: Bietet Dienste zum Festlegen von Code für die Überprüfung von CHV (Karteninhaber) und zum Überprüfen des Benutzers.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Iscardverify-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757015"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="6370d-103">Iscardverify-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6370d-103">ISCardVerify interface</span></span>

<span data-ttu-id="6370d-104">\[Die **iscardverify** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="6370d-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6370d-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6370d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6370d-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6370d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6370d-107">Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6370d-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="6370d-108">Die **iscardverify** -Schnittstelle bietet Dienste zum Festlegen von Code für die Überprüfung von CHV (Karteninhaber) und zum Überprüfen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="6370d-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="6370d-109">Die **iscardverify** -Klasse ist für Anwendungen definiert, die anwendungsspezifische CHV-Richtlinien implementieren, und die über ein detailliertes Wissen zur internen Implementierung der Smartcard verfügen.</span><span class="sxs-lookup"><span data-stu-id="6370d-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="6370d-110">Im folgenden finden Sie eine typische Verwendung der **iscardverify** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6370d-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="6370d-111">Im folgenden Verfahren wird **iscardverify** verwendet, um den CHV-Code zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6370d-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="6370d-112">**So ändern Sie den CHV-Code einer Smartcard**</span><span class="sxs-lookup"><span data-stu-id="6370d-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="6370d-113">Erstellen Sie eine **iscardverify** -Schnittstelle (über die entsprechende [**iscardmanage**](iscardmanage.md) -Schnittstellen Methode).</span><span class="sxs-lookup"><span data-stu-id="6370d-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="6370d-114">Nennen Sie die [**ChangeCode**](iscardverify-changecode.md) -Methode, und stellen Sie neuen Code bereit, um anzugeben, ob es sich um eine lokale oder globale Methode handelt und ob Sie aktiviert oder deaktiviert</span><span class="sxs-lookup"><span data-stu-id="6370d-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="6370d-115">Geben Sie die **iscardverify** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="6370d-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="6370d-116">Member</span><span class="sxs-lookup"><span data-stu-id="6370d-116">Members</span></span>

<span data-ttu-id="6370d-117">Die **iscardverify** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6370d-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6370d-118">**Iscardverify** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6370d-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="6370d-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="6370d-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6370d-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="6370d-120">Methods</span></span>

<span data-ttu-id="6370d-121">Die **iscardverify** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6370d-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="6370d-122">Methode</span><span class="sxs-lookup"><span data-stu-id="6370d-122">Method</span></span>                                                        | <span data-ttu-id="6370d-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6370d-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6370d-124">**ChangeCode**</span><span class="sxs-lookup"><span data-stu-id="6370d-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="6370d-125">Ändert den aktuellen CHV-Code.</span><span class="sxs-lookup"><span data-stu-id="6370d-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="6370d-126">**Resetsecuritystate**</span><span class="sxs-lookup"><span data-stu-id="6370d-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="6370d-127">Setzt den [*Sicherheitskontext*](../secgloss/s-gly.md) der Smartcard zurück.</span><span class="sxs-lookup"><span data-stu-id="6370d-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="6370d-128">[**Blockierung**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6370d-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="6370d-129">Aktiviert den [*Sicherheitskontext*](../secgloss/s-gly.md)erneut.</span><span class="sxs-lookup"><span data-stu-id="6370d-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="6370d-130">**Weisen**</span><span class="sxs-lookup"><span data-stu-id="6370d-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="6370d-131">Authentifiziert den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="6370d-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="6370d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6370d-132">Requirements</span></span>



| <span data-ttu-id="6370d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6370d-133">Requirement</span></span> | <span data-ttu-id="6370d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6370d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6370d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6370d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6370d-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6370d-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6370d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6370d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6370d-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6370d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6370d-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6370d-139">End of client support</span></span><br/>    | <span data-ttu-id="6370d-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6370d-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6370d-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6370d-141">End of server support</span></span><br/>    | <span data-ttu-id="6370d-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6370d-142">Windows Server 2003</span></span><br/>                       |



 

 
