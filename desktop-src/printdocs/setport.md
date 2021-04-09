---
description: Die Funktion "setPort" legt den einem Druckerport zugeordneten Status fest.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: SetPort-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042212"
---
# <a name="setport-function"></a><span data-ttu-id="a2cf9-103">SetPort-Funktion</span><span class="sxs-lookup"><span data-stu-id="a2cf9-103">SetPort function</span></span>

<span data-ttu-id="a2cf9-104">Die Funktion " **setPort** " legt den einem Druckerport zugeordneten Status fest.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2cf9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2cf9-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a2cf9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2cf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2cf9-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2cf9-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cf9-108">Zeiger auf eine mit NULL endend beendete Zeichenfolge, die den Namen des Drucker Servers angibt, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="a2cf9-109">Legen Sie diesen Parameter auf **null** fest, wenn sich der Port auf dem lokalen Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="a2cf9-110">*pportname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2cf9-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cf9-111">Zeiger auf eine mit NULL endend beendete Zeichenfolge, die den Namen des Drucker Anschlusses angibt.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="a2cf9-112">*dwlevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2cf9-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cf9-113">Gibt den Typ der Struktur an, auf die durch den *pportinfo* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="a2cf9-114">Dieser Wert muss 3 sein, was der Datenstruktur [**Port \_ Info \_ 3**](port-info-3.md) entspricht.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2cf9-115">*pportinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2cf9-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2cf9-116">Ein Zeiger auf eine [**Port \_ Info \_ 3**](port-info-3.md) -Struktur, die die festzulegenden Port Statusinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2cf9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2cf9-117">Return value</span></span>

<span data-ttu-id="a2cf9-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a2cf9-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a2cf9-119">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2cf9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2cf9-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2cf9-121">Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a2cf9-122">Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a2cf9-123">Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a2cf9-124">Der Aufrufer der Funktion " **setPort** " muss als Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="a2cf9-125">Wenn es sich beim Aufrufer um einen Port Monitor oder einen sprach Monitor handelt, muss er außerdem [**revertyself**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufrufen, um den Identitätswechsel zu beenden, bevor **setPort** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="a2cf9-126">Alle Programme, die **setPort** aufrufen, müssen über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="a2cf9-127">Wenn Sie einen druckerportstatuswert mit dem Wert " \_ \_ Fehler beim Porttyp" festlegen \_ , beendet der Druck Spooler das Senden von Aufträgen an den Port.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="a2cf9-128">Der Druck Spooler setzt das Senden von Aufträgen an den Port fort, wenn der Port Status durch einen anderen Aufrufen von **setPort** gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a2cf9-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2cf9-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2cf9-129">Requirements</span></span>



| <span data-ttu-id="a2cf9-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2cf9-130">Requirement</span></span> | <span data-ttu-id="a2cf9-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a2cf9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2cf9-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2cf9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a2cf9-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2cf9-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a2cf9-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2cf9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a2cf9-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2cf9-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a2cf9-136">Header</span><span class="sxs-lookup"><span data-stu-id="a2cf9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2cf9-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2cf9-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a2cf9-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a2cf9-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2cf9-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2cf9-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a2cf9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a2cf9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2cf9-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a2cf9-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a2cf9-142">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a2cf9-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2cf9-143">**Setportw** (Unicode) und **setporta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2cf9-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="a2cf9-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2cf9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2cf9-145">Drucken</span><span class="sxs-lookup"><span data-stu-id="a2cf9-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a2cf9-146">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a2cf9-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a2cf9-147">**Port \_ Info \_ 3**</span><span class="sxs-lookup"><span data-stu-id="a2cf9-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

