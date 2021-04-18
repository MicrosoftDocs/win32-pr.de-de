---
description: Konfiguriert den Experten innerhalb der Experten-dll.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Rückruffunktion konfigurieren (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357730"
---
# <a name="configure-callback-function"></a><span data-ttu-id="9ebef-103">Rückruffunktion konfigurieren</span><span class="sxs-lookup"><span data-stu-id="9ebef-103">Configure callback function</span></span>

<span data-ttu-id="9ebef-104">Die Funktion **configure** konfiguriert den Experten innerhalb der Experten-dll.</span><span class="sxs-lookup"><span data-stu-id="9ebef-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="9ebef-105">Der Experte muss die **configure** -Funktion implementieren.</span><span class="sxs-lookup"><span data-stu-id="9ebef-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="9ebef-106">Beim Empfang des Funktions Aufrufes zeigt der Experte ein Dialogfeld an, in dem der Benutzer beliebige konfigurierbare Elemente ändern kann.</span><span class="sxs-lookup"><span data-stu-id="9ebef-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ebef-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="9ebef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ebef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ebef-109">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebef-110">Eindeutige expertenkennung.</span><span class="sxs-lookup"><span data-stu-id="9ebef-110">Unique expert identifier.</span></span>

<span data-ttu-id="9ebef-111">Der eindeutige Bezeichner wird an alle expertenspezifischen Netzwerkmonitor Funktionen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ebef-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="9ebef-112">Beachten Sie, dass es sich bei dem Bezeichner möglicherweise nicht um denselben expertenschlüssel handelt wie der, der an die Funktion [**Run (ausführen**](run.md) )</span><span class="sxs-lookup"><span data-stu-id="9ebef-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="9ebef-113">Speichern Sie den expertenschlüssel nicht aus dem **configure** -Befehl.</span><span class="sxs-lookup"><span data-stu-id="9ebef-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="9ebef-114">*ppconfig* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebef-115">Ein Zeiger auf einen Zeiger auf eine " [**expertenconfig**](expertconfig.md) "-Struktur beim Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9ebef-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="9ebef-116">Nach einem erfolgreichen beenden enthält die referenzierte [**expertenkonfigurationsstruktur**](expertconfig.md) die neuen Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="9ebef-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="9ebef-117">*pexpertstartupinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebef-118">Ein Zeiger auf das Erfassungs Element mit Fokus, wenn der Experte gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9ebef-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="9ebef-119">*StartupFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebef-120">Die Flags, die angeben, wie der Experte den *pexpertstartupinfo* -Parameter verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="9ebef-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="9ebef-121">Das einzige Flag, das **als expertenstartflag definiert ist, ist die \_ Verwendung von \_ \_ \_ Startdaten für \_ \_ \_ Konfigurations \_ Daten**.</span><span class="sxs-lookup"><span data-stu-id="9ebef-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="9ebef-122">Das-Flag gibt an, dass der Experte den *pexpertstartupinfo* -Parameter anstelle des übergebenen *ppconfig* -Parameters verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ebef-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="9ebef-123">In der Regel legen Sie das-Flag fest, wenn Sie den Experten über ein Kontextmenü starten.</span><span class="sxs-lookup"><span data-stu-id="9ebef-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="9ebef-124">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ebef-125">Ein Handle für das übergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="9ebef-125">A handle to the parent window.</span></span> <span data-ttu-id="9ebef-126">Verwenden Sie das Handle, um ein Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9ebef-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ebef-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ebef-127">Return value</span></span>

<span data-ttu-id="9ebef-128">Wenn die Funktion erfolgreich ist (d. h., wenn eine aktuelle Konfiguration vorhanden ist), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="9ebef-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="9ebef-129">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="9ebef-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebef-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ebef-130">Remarks</span></span>

<span data-ttu-id="9ebef-131">Netzwerkmonitor Ruft die **configure** -Funktion mit der aktuellen Konfiguration des Experten auf, sofern eine vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9ebef-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="9ebef-132">Der Experte zeigt ein Dialogfeld an, in dem Sie beliebige konfigurierbare Elemente ändern können.</span><span class="sxs-lookup"><span data-stu-id="9ebef-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="9ebef-133">Wenn *ppconfig* in übergeben wird und Netzwerkmonitor keine Konfiguration für den angegebenen Experten gespeichert hat, kann der Parameterwert **null** sein.</span><span class="sxs-lookup"><span data-stu-id="9ebef-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="9ebef-134">In diesem Fall geht die **configure** -Funktion von hart codierten Standardwerten aus (oder verwendet die Startinformationen), um das Dialogfeld zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="9ebef-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="9ebef-135">Die Konfigurationsdaten können auch **null** sein, wenn die Funktion " **configure** " zurückgegeben wird, und es wurde ein **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ebef-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="9ebef-136">Diese Situation tritt auf, wenn Netzwerkmonitor keinen gespeicherten Standardwert besitzt, und der Benutzer auf **Abbrechen** drückt.</span><span class="sxs-lookup"><span data-stu-id="9ebef-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="9ebef-137">Der Anfang der Datenstruktur " [**expertconfig**](expertconfig.md) " enthält einen privaten Abschnitt, in dem die Informationen zur Struktur Größe gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9ebef-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="9ebef-138">Die Größe der **expertenkonfigurationsstruktur** sollte die reservierte **DWORD** -Länge enthalten, die am Anfang der Struktur angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9ebef-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="9ebef-139">Wenn die Konfigurationsdaten z. b. 20 Bytes Speicherplatz benötigen, müssen Sie 24 Bytes zum Speichern der Daten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9ebef-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="9ebef-140">Wenn ein *ppconfig* -Wert **null** ist, ruft die **configure** -Funktion [**die Funktion "-Funktion"**](expertallocmemory.md) auf, um eine neue Konfiguration zuzuordnen, die die richtige Größe hat.</span><span class="sxs-lookup"><span data-stu-id="9ebef-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="9ebef-141">Wenn der Puffer nicht ausreichend ist, um die Expertendaten aufzunehmen, sollte der Experte die Funktion " [**expertrebelegcmemory**](expertreallocmemory.md) " anrufen.</span><span class="sxs-lookup"><span data-stu-id="9ebef-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebef-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ebef-142">Requirements</span></span>



| <span data-ttu-id="9ebef-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ebef-143">Requirement</span></span> | <span data-ttu-id="9ebef-144">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebef-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebef-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ebef-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9ebef-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9ebef-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ebef-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9ebef-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ebef-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9ebef-149">Header</span><span class="sxs-lookup"><span data-stu-id="9ebef-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ebef-150"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ebef-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




