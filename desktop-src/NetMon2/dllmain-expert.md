---
description: Der Experte implementiert die DllMain-Funktion. Das Betriebssystem ruft DllMain auf, um ein Handle für eine Instanz des Experten abzurufen.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: DllMain-Funktion für expertenrückruf (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866271"
---
# <a name="dllmain-expert-callback-function"></a><span data-ttu-id="b413e-104">DllMain-Funktion für expertenrückruf</span><span class="sxs-lookup"><span data-stu-id="b413e-104">DllMain Expert callback function</span></span>

<span data-ttu-id="b413e-105">Der Experte implementiert die [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b413e-105">The expert implements the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> <span data-ttu-id="b413e-106">Das Betriebssystem ruft **DllMain** auf, um ein Handle für eine Instanz des Experten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b413e-106">The operating system calls **DllMain** to obtain a handle to an instance of the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="b413e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b413e-107">Syntax</span></span>


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="b413e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b413e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b413e-109">*HINSTANCE* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b413e-109">*hInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b413e-110">Handle für eine Instanz des Experten.</span><span class="sxs-lookup"><span data-stu-id="b413e-110">Handle to an instance of the expert.</span></span>

<span data-ttu-id="b413e-111">Wenn der Experte den Netzwerkmonitor Benutzeroberfläche verwendet, muss der *HINSTANCE* -Wert in einer globalen Variablen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b413e-111">If the expert uses the Network Monitor user interface, the *hInstance* value must be stored in a global variable.</span></span> <span data-ttu-id="b413e-112">Diese Vorgehensweise ist nur erforderlich, wenn der Wert des *ulReason* -Parameters auf DLL- \_ Prozess anfügen festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="b413e-112">This approach is necessary only when the value of the *ulReason* parameter is set to DLL\_PROCESS\_ATTACH.</span></span>

</dd> <dt>

<span data-ttu-id="b413e-113">*ulReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b413e-113">*ulReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b413e-114">Indikator für den Grund, warum die Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b413e-114">Indicator of why the function was called.</span></span> <span data-ttu-id="b413e-115">Ein Wert von DLL- \_ Prozess \_ Anfügen (gilt beim ersten Laden der dll) gibt an, dass der Experte den *HINSTANCE* -Wert in einer globalen Variablen speichern soll.</span><span class="sxs-lookup"><span data-stu-id="b413e-115">A value of DLL\_PROCESS\_ATTACH, (which applies when the DLL is first loaded) indicates that the expert should save the *hInstance* value in a global variable.</span></span>

<span data-ttu-id="b413e-116">Mit jedem anderen Wert können alle Aufrufe der [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b413e-116">With any other value, all calls to the [**DllMain**](/windows/desktop/Dlls/dllmain) function can be ignored.</span></span> <span data-ttu-id="b413e-117">Eine Liste aller möglichen Flags, die vom Betriebssystem festgelegt werden, finden Sie unter **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="b413e-117">For a list of all possible flags set by the operating system, see **DLLMain**.</span></span>

</dd> <dt>

<span data-ttu-id="b413e-118">*Reserved*</span><span class="sxs-lookup"><span data-stu-id="b413e-118">*Reserved*</span></span> 
</dt> <dd>

<span data-ttu-id="b413e-119">Der Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b413e-119">Parameter is not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b413e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b413e-120">Return value</span></span>

<span data-ttu-id="b413e-121">Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="b413e-121">If the function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="b413e-122">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="b413e-122">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b413e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b413e-123">Remarks</span></span>

<span data-ttu-id="b413e-124">Das Betriebssystem Ruft die Funktion **DllMain** -Experte auf, wenn ein Prozess die Experten-dll lädt oder entlädt.</span><span class="sxs-lookup"><span data-stu-id="b413e-124">The operating system calls the **DllMain** expert function when a process loads or unloads the expert DLL.</span></span> <span data-ttu-id="b413e-125">Die Funktion **DllMain** -Experte muss nur exportiert werden, wenn der Experte über eine Benutzeroberfläche verfügt, um entweder die Konfiguration oder die Ergebnisse anzuzeigen, und dann nur den richtigen *HINSTANCE* -Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b413e-125">The **DllMain** expert function must be exported only if the expert has a user interface for viewing either configuration or results, and then only to return the proper *hInstance* value.</span></span>

<span data-ttu-id="b413e-126">Die Funktion **DllMain** -Experte basiert auf der [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion der Dynamic Link Library.</span><span class="sxs-lookup"><span data-stu-id="b413e-126">The **DllMain** expert function is based on the dynamic link library [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b413e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b413e-127">Requirements</span></span>



| <span data-ttu-id="b413e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b413e-128">Requirement</span></span> | <span data-ttu-id="b413e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b413e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b413e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b413e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b413e-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b413e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b413e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b413e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b413e-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b413e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b413e-134">Header</span><span class="sxs-lookup"><span data-stu-id="b413e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b413e-135"><dt>Process. h</dt></span><span class="sxs-lookup"><span data-stu-id="b413e-135"><dt>Process.h</dt></span></span> </dl> |



 

