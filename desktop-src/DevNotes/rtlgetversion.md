---
description: Ruft Versionsinformationen zum aktuell laufenden Betriebssystem ab.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Rtlgetversion-Funktion (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126404"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="0ff61-103">Rtlgetversion-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ff61-103">RtlGetVersion function</span></span>

<span data-ttu-id="0ff61-104">Ruft Versionsinformationen zum aktuell laufenden Betriebssystem ab.</span><span class="sxs-lookup"><span data-stu-id="0ff61-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ff61-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="0ff61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ff61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff61-107">*lpversioninformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0ff61-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff61-108">Zeiger auf eine [**RTL \_ osversioninfow**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) -Struktur oder eine [**RTL \_ osversioninfoexw**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) -Struktur, die die Versionsinformationen zum aktuell ausgelaufenden Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="0ff61-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="0ff61-109">Ein Aufrufer gibt an, welche Eingabe Struktur verwendet wird, indem der **dwOSVersionInfoSize** -Member der-Struktur auf die Größe in Bytes der verwendeten Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0ff61-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff61-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ff61-110">Return value</span></span>

<span data-ttu-id="0ff61-111">Gibt den Status \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="0ff61-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff61-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ff61-112">Remarks</span></span>

<span data-ttu-id="0ff61-113">**Rtlgetversion** ist die Entsprechung der [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) -Funktion in der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0ff61-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="0ff61-114">Sehen Sie sich das Beispiel in der Windows SDK an, in dem gezeigt wird, wie Sie die System Version erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ff61-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="0ff61-115">Wenn Sie **rtlgetversion** verwenden, um zu bestimmen, ob eine bestimmte Version des Betriebssystems ausgeführt wird, muss ein Aufrufer nach Versionsnummern suchen, die größer oder gleich der erforderlichen Versionsnummer sind.</span><span class="sxs-lookup"><span data-stu-id="0ff61-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="0ff61-116">Dadurch wird sichergestellt, dass ein Versions Test für spätere Versionen von Windows erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0ff61-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="0ff61-117">Da Betriebssystemfunktionen in einer verteilbaren dll hinzugefügt werden können, ist die Überprüfung nur der Haupt-und neben Versionsnummern nicht die zuverlässigste Möglichkeit, das vorhanden sein eines bestimmten System Features zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0ff61-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="0ff61-118">Ein Treiber sollte [**rtlverifyversioninfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) verwenden, um zu testen, ob eine bestimmte Systemfunktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0ff61-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff61-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ff61-119">Requirements</span></span>



| <span data-ttu-id="0ff61-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ff61-120">Requirement</span></span> | <span data-ttu-id="0ff61-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0ff61-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff61-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ff61-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff61-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ff61-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0ff61-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ff61-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff61-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ff61-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0ff61-126">Zielplattform</span><span class="sxs-lookup"><span data-stu-id="0ff61-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="0ff61-127"><dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff61-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="0ff61-128">Header</span><span class="sxs-lookup"><span data-stu-id="0ff61-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ff61-129"><dt>Ntddk. h (einschließlich ntddk. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff61-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="0ff61-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ff61-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ff61-131"><dt>Ntdll. lib; </dt> <dt>Nzu-nl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ff61-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="0ff61-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0ff61-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ff61-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ff61-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff61-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ff61-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff61-135">**Psgetversion**</span><span class="sxs-lookup"><span data-stu-id="0ff61-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
