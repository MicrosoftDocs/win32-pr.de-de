---
title: Getprocesshandlefromhwnd-Funktion
description: Ruft ein Prozess handle von einem Fenster Handle ab.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Getprocesshandlefromhwnd-Funktion Windows-Barrierefreiheit
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103820"
---
# <a name="getprocesshandlefromhwnd-function"></a><span data-ttu-id="06469-104">Getprocesshandlefromhwnd-Funktion</span><span class="sxs-lookup"><span data-stu-id="06469-104">GetProcessHandleFromHwnd function</span></span>

<span data-ttu-id="06469-105">Ruft ein Prozess handle von einem Fenster Handle ab.</span><span class="sxs-lookup"><span data-stu-id="06469-105">Retrieves a process handle from a window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="06469-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="06469-106">Syntax</span></span>


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="06469-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="06469-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06469-108">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06469-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06469-109">Typ: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06469-109">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="06469-110">Das Fensterhandle.</span><span class="sxs-lookup"><span data-stu-id="06469-110">The window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06469-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06469-111">Return value</span></span>

<span data-ttu-id="06469-112">Typ: **[ **handle**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="06469-112">Type: **[**HANDLE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="06469-113">Bei erfolgreicher Ausführung wird das Handle des Prozesses zurückgegeben, der das Fenster besitzt.</span><span class="sxs-lookup"><span data-stu-id="06469-113">If successful, returns the handle of the process that owns the window.</span></span>

<span data-ttu-id="06469-114">Wenn dies nicht erfolgreich ist, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06469-114">If not successful, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="06469-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06469-115">Remarks</span></span>

<span data-ttu-id="06469-116">In früheren Versionen des Betriebssystems konnte ein Prozess einen anderen Prozess (z. b. für den Zugriff auf den Arbeitsspeicher) mit [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)eröffnen.</span><span class="sxs-lookup"><span data-stu-id="06469-116">In previous versions of the operating system, a process could open another process (to access its memory, for example) using [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess).</span></span> <span data-ttu-id="06469-117">Diese Funktion ist erfolgreich, wenn der Aufrufer über entsprechende Berechtigungen verfügt. in der Regel müssen der Aufrufer und der Ziel Prozess derselbe Benutzer sein.</span><span class="sxs-lookup"><span data-stu-id="06469-117">This function succeeds if the caller has appropriate privileges; usually the caller and target process must be the same user.</span></span>

<span data-ttu-id="06469-118">Bei Windows Vista schlägt [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) jedoch in dem Szenario fehl, in dem der Aufrufer UIAccess hat, und der Ziel Prozess erhöht sich.</span><span class="sxs-lookup"><span data-stu-id="06469-118">On Windows Vista, however, [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) fails in the scenario where the caller has UIAccess, and the target process is elevated.</span></span> <span data-ttu-id="06469-119">In diesem Fall befindet sich der Besitzer des Ziel Prozesses in der Gruppe "Administratoren", aber der aufrufende Prozess wird mit dem eingeschränkten Token ausgeführt, ist also nicht Mitglied dieser Gruppe und wird der Zugriff auf den erweiterten Prozess verweigert.</span><span class="sxs-lookup"><span data-stu-id="06469-119">In this case, the owner of the target process is in the Administrators group, but the calling process is running with the restricted token, so does not have membership in this group, and is denied access to the elevated process.</span></span> <span data-ttu-id="06469-120">Wenn der Aufrufer über UIAccess verfügt, kann er jedoch einen Windows-Hook verwenden, um Code in den Ziel Prozess einzufügen und innerhalb des Ziel Prozesses ein Handle zurück an den Aufrufer zu senden.</span><span class="sxs-lookup"><span data-stu-id="06469-120">If the caller has UIAccess, however, they can use a windows hook to inject code into the target process, and from within the target process, send a handle back to the caller.</span></span>

<span data-ttu-id="06469-121">**Getprocesshandlefromhwnd** ist eine Hilfsfunktion, die diese Technik verwendet, um das Handle des Prozesses zu erhalten, der das angegebene HWND besitzt.</span><span class="sxs-lookup"><span data-stu-id="06469-121">**GetProcessHandleFromHwnd** is a convenience function that uses this technique to obtain the handle of the process that owns the specified HWND.</span></span> <span data-ttu-id="06469-122">Beachten Sie, dass Sie nur erfolgreich ist, wenn der Aufrufer und der Ziel Prozess als derselbe Benutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="06469-122">Note that it only succeeds in cases where the caller and target process are running as the same user.</span></span> <span data-ttu-id="06469-123">Das zurückgegebene Handle verfügt über die folgenden Berechtigungen: Prozess-DUP-handle Prozess-VM-Vorgang Prozess-VM \_ \_ \| \_ \_ \| \_ \_ \| Schreibvorgang VM \_ Schreibvorgang \_ \| synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="06469-123">The returned handle has the following privileges: PROCESS\_DUP\_HANDLE \| PROCESS\_VM\_OPERATION \| PROCESS\_VM\_READ \| PROCESS\_VM\_WRITE \| SYNCHRONIZE.</span></span> <span data-ttu-id="06469-124">Wenn andere Berechtigungen erforderlich sind, ist es möglicherweise erforderlich, die einbinden-Technik explizit zu implementieren, anstatt diese Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="06469-124">If other privileges are required, it may be necessary to implement the hooking technique explicitly instead of using this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="06469-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06469-125">Requirements</span></span>



| <span data-ttu-id="06469-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06469-126">Requirement</span></span> | <span data-ttu-id="06469-127">Wert</span><span class="sxs-lookup"><span data-stu-id="06469-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06469-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06469-128">Minimum supported client</span></span><br/> | <span data-ttu-id="06469-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06469-129">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06469-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06469-130">Minimum supported server</span></span><br/> | <span data-ttu-id="06469-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06469-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06469-132">DLL</span><span class="sxs-lookup"><span data-stu-id="06469-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06469-133"><dt>Oleacc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06469-133"><dt>Oleacc.dll</dt></span></span> </dl> |



 

