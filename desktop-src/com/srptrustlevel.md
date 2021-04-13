---
title: SRPTrustLevel
description: Legt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) für Anwendungen fest.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- SRPTrustLevel Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388146"
---
# <a name="srptrustlevel"></a><span data-ttu-id="75c5e-104">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="75c5e-104">SRPTrustLevel</span></span>

<span data-ttu-id="75c5e-105">Legt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) für Anwendungen fest.</span><span class="sxs-lookup"><span data-stu-id="75c5e-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="75c5e-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="75c5e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="75c5e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75c5e-107">Remarks</span></span>

<span data-ttu-id="75c5e-108">Dies ist ein **reg \_ DWORD** -Wert, der ab Windows XP verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="75c5e-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="75c5e-109">Wert</span><span class="sxs-lookup"><span data-stu-id="75c5e-109">Value</span></span>                                 | <span data-ttu-id="75c5e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75c5e-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75c5e-111">0x0 (sicherere \_ levelid nicht \_ zulässig)</span><span class="sxs-lookup"><span data-stu-id="75c5e-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="75c5e-112">Der Zugriff auf und sicherheitsrelevante Benutzerberechtigungen ist für die Anwendung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="75c5e-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="75c5e-113">0x40000 (sichere \_ levelid \_ fullytrusted)</span><span class="sxs-lookup"><span data-stu-id="75c5e-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="75c5e-114">Die Anwendung hat uneingeschränkten Zugriff auf die Berechtigungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="75c5e-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="75c5e-115">Wenn der **SRPTrustLevel** -Wert nicht vorhanden ist, wird der Standardwert von sicherere \_ levelid nicht \_ zulässig verwendet.</span><span class="sxs-lookup"><span data-stu-id="75c5e-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="75c5e-116">Wenn **SRPTrustLevel** den falschen Typ oder außerhalb des zulässigen Bereichs hat, gibt com den Fehler COMAdmin \_ E \_ saferinvalid zurück.</span><span class="sxs-lookup"><span data-stu-id="75c5e-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="75c5e-117">Wenn die Aktivierung einer beliebigen Sortierung aufgrund von SRP-Vertrauensstellungs Überprüfungen fehlschlägt, gibt com den Fehler Co \_ E \_ activationfailed zurück.</span><span class="sxs-lookup"><span data-stu-id="75c5e-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75c5e-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="75c5e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75c5e-119">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="75c5e-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="75c5e-120">**Srpactivateasactivatorchecks**</span><span class="sxs-lookup"><span data-stu-id="75c5e-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="75c5e-121">**Srprunningobjectchecks**</span><span class="sxs-lookup"><span data-stu-id="75c5e-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 




