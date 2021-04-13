---
title: Activationfailurelogginglevel
description: Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen zu fehlgeschlagenen Anforderungen für das Starten und Aktivieren von Komponenten fest.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Registrierungs Wert "activationfailurelogginglevel" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388752"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="5c999-104">Activationfailurelogginglevel</span><span class="sxs-lookup"><span data-stu-id="5c999-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="5c999-105">Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen zu fehlgeschlagenen Anforderungen für das Starten und Aktivieren von Komponenten fest.</span><span class="sxs-lookup"><span data-stu-id="5c999-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5c999-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="5c999-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="5c999-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c999-107">Remarks</span></span>

<span data-ttu-id="5c999-108">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="5c999-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="5c999-109">Wert</span><span class="sxs-lookup"><span data-stu-id="5c999-109">Value</span></span> | <span data-ttu-id="5c999-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c999-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c999-111">0</span><span class="sxs-lookup"><span data-stu-id="5c999-111">0</span></span>     | <span data-ttu-id="5c999-112">Verwenden der freigegebenen Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="5c999-112">Use discretionary logging.</span></span> <span data-ttu-id="5c999-113">Standardmäßig protokollieren Sie Fehler, Clients können dieses Verhalten jedoch außer Kraft setzen, indem Sie \_ \_ \_ in [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)das CLSCTX No Failure Log angeben.</span><span class="sxs-lookup"><span data-stu-id="5c999-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="5c999-114">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="5c999-114">This is the default value.</span></span> |
| <span data-ttu-id="5c999-115">1</span><span class="sxs-lookup"><span data-stu-id="5c999-115">1</span></span>     | <span data-ttu-id="5c999-116">Alle Fehler unabhängig vom angegebenen Client protokollieren.</span><span class="sxs-lookup"><span data-stu-id="5c999-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="5c999-117">2</span><span class="sxs-lookup"><span data-stu-id="5c999-117">2</span></span>     | <span data-ttu-id="5c999-118">Protokollieren Sie niemals Fehler, unabhängig vom angegebenen Client.</span><span class="sxs-lookup"><span data-stu-id="5c999-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="5c999-119">Wenn Sie eine Anwendung zum Steuern der Ereignisprotokollierung benötigen, empfiehlt es sich, diesen Wert auf 0 festzulegen und den Client Code zu schreiben, um ihn bei Bedarf zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5c999-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="5c999-120">Es wird dringend empfohlen, den Wert nicht auf 2 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5c999-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="5c999-121">Wenn die Ereignisprotokollierung deaktiviert ist, ist es schwieriger, Probleme zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="5c999-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="5c999-122">Bei Fehlern in Bezug auf Computer Einschränkungen, bei denen com keine CLSCTX-Bits hat, behandelt com den Wert 0 als 1.</span><span class="sxs-lookup"><span data-stu-id="5c999-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c999-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c999-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c999-124">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="5c999-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




