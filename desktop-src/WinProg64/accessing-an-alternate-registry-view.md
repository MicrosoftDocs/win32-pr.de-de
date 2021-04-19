---
title: Zugreifen auf eine Alternative Registrierungs Ansicht
description: Eine 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, greift standardmäßig auf die 32-Bit-Registrierungsansicht zu, und eine 64-Bit-Anwendung greift auf die 64-Bit-Registrierungsansicht zu.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- Registrierungs Sichten 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Registrierungs Sichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106355088"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="9ef66-105">Zugreifen auf eine Alternative Registrierungs Ansicht</span><span class="sxs-lookup"><span data-stu-id="9ef66-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="9ef66-106">Eine 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, greift standardmäßig auf die 32-Bit-Registrierungsansicht zu, und eine 64-Bit-Anwendung greift auf die 64-Bit-Registrierungsansicht zu.</span><span class="sxs-lookup"><span data-stu-id="9ef66-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="9ef66-107">Die folgenden Flags ermöglichen 32-Bit-Anwendungen den Zugriff auf umgeleitete Schlüssel in der 64-Bit-Registrierungs Ansicht und 64-Bit-Anwendungen für den Zugriff auf umgeleitete Schlüssel in der 32-Bit-Registrierungs Ansicht.</span><span class="sxs-lookup"><span data-stu-id="9ef66-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="9ef66-108">Diese Flags haben keine Auswirkung auf freigegebene Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="9ef66-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="9ef66-109">Weitere Informationen finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="9ef66-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="9ef66-110">Flagname</span><span class="sxs-lookup"><span data-stu-id="9ef66-110">Flag name</span></span>         | <span data-ttu-id="9ef66-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9ef66-111">Value</span></span>  | <span data-ttu-id="9ef66-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ef66-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ef66-113">Key \_ WOW64 \_ 64key</span><span class="sxs-lookup"><span data-stu-id="9ef66-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="9ef66-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="9ef66-114">0x0100</span></span> | <span data-ttu-id="9ef66-115">Greifen Sie entweder über eine 32-Bit-oder 64-Bit-Anwendung auf einen 64-Bit-Schlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="9ef66-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="9ef66-116">Key \_ WOW64 \_ 32key</span><span class="sxs-lookup"><span data-stu-id="9ef66-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="9ef66-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="9ef66-117">0x0200</span></span> | <span data-ttu-id="9ef66-118">Greifen Sie entweder über eine 32-Bit-oder 64-Bit-Anwendung auf einen 32-Bit-Schlüssel zu.</span><span class="sxs-lookup"><span data-stu-id="9ef66-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="9ef66-119">**Windows 10 auf ARM:** Dies bezieht sich auf die 32-Bit-ARM-Registrierungs Sicht für 32-Bit-ARM-Prozesse und die 32-Bit-x86-Registrierungs Ansicht für 32-Bit-x86-und 64-Bit ARM64-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="9ef66-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="9ef66-120">Diese Flags können im Parameter *samgewünschter* Parameter der folgenden Registrierungsfunktionen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="9ef66-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="9ef66-121">**Regkreatekeyex**</span><span class="sxs-lookup"><span data-stu-id="9ef66-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="9ef66-122">**Regdeletekeyex**</span><span class="sxs-lookup"><span data-stu-id="9ef66-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="9ef66-123">**Fehler bei RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="9ef66-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="9ef66-124">Entweder Key \_ WOW64 \_ 32key oder Key \_ WOW64 \_ 64key kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ef66-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="9ef66-125">Wenn beide Flags angegeben sind, schlägt die Funktion mit einem \_ ungültigen \_ Parameter fehl.</span><span class="sxs-lookup"><span data-stu-id="9ef66-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="9ef66-126">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Wenn beide Flags angegeben sind, ist das Verhalten der Funktion nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9ef66-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="9ef66-127">Die [**regdeletekey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) -Funktion kann nicht für den Zugriff auf eine Alternative Registrierungs Ansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ef66-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="9ef66-128">Im folgenden finden Sie bewährte Methoden für den Zugriff auf die Registrierung von einer Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="9ef66-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="9ef66-129">Nachdem die Anwendung mit einem der Flags auf eine Alternative Registrierungs Ansicht zugegriffen hat, müssen alle nachfolgenden Vorgänge (erstellen, löschen oder öffnen) für untergeordnete Registrierungsschlüssel explizit dasselbe Flag verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ef66-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="9ef66-130">Andernfalls kann es zu unerwartetem Verhalten kommen.</span><span class="sxs-lookup"><span data-stu-id="9ef66-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="9ef66-131">Um alle Schlüssel in beiden Ansichten genau aufzuzählen, führen Sie die Enumeration in zwei Durchläufen aus.</span><span class="sxs-lookup"><span data-stu-id="9ef66-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="9ef66-132">Der erste Durchlauf sollte ein Handle verwenden, das mit einem der-Flags geöffnet wurde, und der andere Durchlauf sollte ein Handle verwenden, das mit dem anderen Flag geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="9ef66-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="9ef66-133">Die Schlüssel **Wow6432Node** und **WowAA32Node** sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="9ef66-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="9ef66-134">Aus Kompatibilitätsgründen sollten Anwendungen diese Schlüssel nicht direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ef66-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="9ef66-135">Weitere Informationen zum Zugreifen auf die Alternative Registrierungs Ansicht über WMI finden Sie unter [anfordern von WMI-Daten auf einer 64-Bit-Plattform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span><span class="sxs-lookup"><span data-stu-id="9ef66-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ef66-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ef66-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ef66-137">Registrierungs Redirector</span><span class="sxs-lookup"><span data-stu-id="9ef66-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="9ef66-138">Registrierungs Reflektion</span><span class="sxs-lookup"><span data-stu-id="9ef66-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

