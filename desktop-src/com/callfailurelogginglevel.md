---
title: CallFailureLoggingLevel
description: Legt die Ausführlichkeit von Ereignisprotokoll Einträgen zu fehlgeschlagenen Aufrufen von-Komponenten fest.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- CallFailureLoggingLevel-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855887"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="b16c3-104">CallFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="b16c3-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="b16c3-105">Legt die Ausführlichkeit von Ereignisprotokoll Einträgen zu fehlgeschlagenen Aufrufen von-Komponenten fest.</span><span class="sxs-lookup"><span data-stu-id="b16c3-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b16c3-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="b16c3-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="b16c3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b16c3-107">Remarks</span></span>

<span data-ttu-id="b16c3-108">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="b16c3-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="b16c3-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b16c3-109">Value</span></span> | <span data-ttu-id="b16c3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b16c3-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b16c3-111">1</span><span class="sxs-lookup"><span data-stu-id="b16c3-111">1</span></span>     | <span data-ttu-id="b16c3-112">Fehler während eines Aufrufes im com-Server Prozess immer protokollieren.</span><span class="sxs-lookup"><span data-stu-id="b16c3-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="b16c3-113">2</span><span class="sxs-lookup"><span data-stu-id="b16c3-113">2</span></span>     | <span data-ttu-id="b16c3-114">Fehler während eines Aufrufes im com-Server Prozess nie protokollieren.</span><span class="sxs-lookup"><span data-stu-id="b16c3-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="b16c3-115">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="b16c3-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b16c3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b16c3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b16c3-117">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b16c3-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




