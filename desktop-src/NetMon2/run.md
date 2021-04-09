---
description: Der Experte muss die Run-Funktion implementieren. Netzwerkmonitor Ruft die Run-Funktion auf, um den Experten innerhalb der Experten-dll zu starten.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Run Callback-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862899"
---
# <a name="run-callback-function"></a><span data-ttu-id="4582b-104">Rückruffunktion ausführen</span><span class="sxs-lookup"><span data-stu-id="4582b-104">Run callback function</span></span>

<span data-ttu-id="4582b-105">Der Experte muss die **Run** -Funktion implementieren.</span><span class="sxs-lookup"><span data-stu-id="4582b-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="4582b-106">Netzwerkmonitor Ruft die **Run** -Funktion auf, um den Experten innerhalb der Experten-dll zu starten.</span><span class="sxs-lookup"><span data-stu-id="4582b-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="4582b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4582b-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="4582b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4582b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4582b-109">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4582b-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4582b-110">Eindeutiger Bezeichner des Experten, der an alle expertenspezifischen Netzwerkmonitor Funktionen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4582b-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="4582b-111">Der *hexpertkey* -Bezeichner kann einen anderen als den von der Funktion " [**configure**](configure.md) " übergebenen expertenschlüssel übergeben.</span><span class="sxs-lookup"><span data-stu-id="4582b-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="4582b-112">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4582b-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4582b-113">Zeiger auf die vorhandene Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4582b-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="4582b-114">Der *pConfig* -Parameter kann **null** sein, was bedeutet, dass der Experte mit hart codierten Standardwerten oder Startinformationen, auf die der *pexpertstartupinfo* -Parameter verweist, ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4582b-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="4582b-115">*pexpertstartupinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4582b-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4582b-116">Zeiger auf das Erfassungs Element, das den Fokus besitzt, wenn der Experte gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4582b-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="4582b-117">*StartupFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4582b-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4582b-118">Indikator dafür, wie der Experte den *pexpertstartupinfo* -Parameter verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4582b-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="4582b-119">Das einzige Flag, das definiert ist, ist:</span><span class="sxs-lookup"><span data-stu-id="4582b-119">The only flag defined is:</span></span>



| <span data-ttu-id="4582b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4582b-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="4582b-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4582b-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="4582b-122"><dt>**Das \_ \_ Startflag für Experten \_ verwendet \_ Start \_ Daten für \_ \_ Konfigurations \_ Daten.**</dt></span><span class="sxs-lookup"><span data-stu-id="4582b-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="4582b-123">Dieses Flag gibt an, dass der Experte den *pexpertstartupinfo* -Parameter verwendet und nicht den *pConfig* -Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="4582b-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="4582b-124">In der Regel können Sie dieses Flag festlegen, wenn der Experte von einem Rechtsklick aus beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="4582b-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="4582b-125">Wenn das Flag nicht festgelegt ist, können die folgenden beiden Aktionen auftreten: entweder der Experte startet nicht mit der rechten Maustaste, oder der Experte startet mit der rechten Maustaste, und der Benutzer konfiguriert ihn.</span><span class="sxs-lookup"><span data-stu-id="4582b-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4582b-126">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4582b-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4582b-127">Der *HWND* -Parameter des übergeordneten Elements (normalerweise die Netzwerkmonitor Benutzeroberfläche).</span><span class="sxs-lookup"><span data-stu-id="4582b-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4582b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4582b-128">Return value</span></span>

<span data-ttu-id="4582b-129">Wenn die Funktion erfolgreich ist (d. h., wenn der Experte startet), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="4582b-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="4582b-130">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="4582b-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4582b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4582b-131">Remarks</span></span>

<span data-ttu-id="4582b-132">Beim Ausführen durchläuft der Experte die Frames in der Erfassungs Datei und generiert entweder einen Bericht oder erstellt Ereignisse, die Probleme anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4582b-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="4582b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4582b-133">Requirements</span></span>



| <span data-ttu-id="4582b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4582b-134">Requirement</span></span> | <span data-ttu-id="4582b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4582b-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4582b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4582b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4582b-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4582b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4582b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4582b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4582b-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4582b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4582b-140">Header</span><span class="sxs-lookup"><span data-stu-id="4582b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4582b-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4582b-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




