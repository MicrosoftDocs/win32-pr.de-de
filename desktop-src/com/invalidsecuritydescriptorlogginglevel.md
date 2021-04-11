---
title: Invalidsecuritydescriptor LoggingLevel
description: Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen über ungültige Sicherheits Deskriptoren für die Start-und Zugriffsberechtigungen der Komponente fest.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Invalidsecuritydescriptor LoggingLevel-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309180"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="4dcb9-104">Invalidsecuritydescriptor LoggingLevel</span><span class="sxs-lookup"><span data-stu-id="4dcb9-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="4dcb9-105">Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen über ungültige Sicherheits Deskriptoren für die Start-und Zugriffsberechtigungen der Komponente fest.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4dcb9-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="4dcb9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="4dcb9-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dcb9-107">Remarks</span></span>

<span data-ttu-id="4dcb9-108">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="4dcb9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="4dcb9-109">Value</span></span> | <span data-ttu-id="4dcb9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dcb9-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dcb9-111">1</span><span class="sxs-lookup"><span data-stu-id="4dcb9-111">1</span></span>     | <span data-ttu-id="4dcb9-112">Fehler immer protokollieren, wenn com einen ungültigen Sicherheits Deskriptor findet.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="4dcb9-113">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="4dcb9-114">2</span><span class="sxs-lookup"><span data-stu-id="4dcb9-114">2</span></span>     | <span data-ttu-id="4dcb9-115">Fehler werden nie protokolliert, wenn com einen ungültigen Sicherheits Deskriptor findet.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="4dcb9-116">Es wird nicht empfohlen, die Ereignisprotokollierung zu deaktivieren, da dadurch die Diagnose von Problemen erschwert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="4dcb9-117">Wenn Sie die Sicherheits Deskriptoren für die Start-und Zugriffsberechtigung (häufig als ACLs bezeichnet) direkt festlegen, ist es möglich, eine Sicherheits Beschreibung zu erstellen, deren Bedeutung nicht eindeutig interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="4dcb9-118">COM führt einen Ereignisprotokoll Eintrag aus, wenn ein solcher Ungültiger Sicherheits Deskriptor auftritt.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="4dcb9-119">Beachten Sie, dass [**activationfailurelogginglevel**](activationfailurelogginglevel.md) und [**CallFailureLoggingLevel**](callfailurelogginglevel.md) keine Kontrolle über die Protokollierung ungültiger Sicherheits deskriptorfehler haben.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="4dcb9-120">Verwenden Sie **invalidsecuritydescriptor LoggingLevel** , um die vollständige Kontrolle über diese Funktionalität zu haben.</span><span class="sxs-lookup"><span data-stu-id="4dcb9-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dcb9-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4dcb9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dcb9-122">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="4dcb9-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




