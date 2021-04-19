---
description: Fügt für den Computer, von dem Sie aufgerufen wird, einen alternativen lokalen Netzwerknamen hinzu.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: Addlocalalternativen Computername-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361628"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="faf4a-103">Addlocalalternativen Computername-Funktion</span><span class="sxs-lookup"><span data-stu-id="faf4a-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="faf4a-104">Fügt für den Computer, von dem Sie aufgerufen wird, einen alternativen lokalen Netzwerknamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="faf4a-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf4a-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="faf4a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faf4a-107">*lpdnsfqhostname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faf4a-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf4a-108">Der Alternative Name, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="faf4a-108">The alternate name to be added.</span></span> <span data-ttu-id="faf4a-109">Der Name muss das Format " **computernamednsfullyqualified** " aufweisen, wie in der-Enumeration des [**Computer \_ Namen \_ Formats**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) definiert, und die [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) -Funktion muss Sie in der Lage sein, Sie zu validieren, wenn ihr Format auf **dnsnamehostnamefull** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="faf4a-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="faf4a-110">*ulflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="faf4a-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf4a-111">Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="faf4a-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf4a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="faf4a-112">Return value</span></span>

<span data-ttu-id="faf4a-113">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion den **Fehler \_ Erfolg** zurück.</span><span class="sxs-lookup"><span data-stu-id="faf4a-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="faf4a-114">Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="faf4a-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="faf4a-115">Zu den zurückgegebenen Fehlercodes zählen die folgenden:</span><span class="sxs-lookup"><span data-stu-id="faf4a-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="faf4a-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="faf4a-116">Return code</span></span>                                                                                               | <span data-ttu-id="faf4a-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faf4a-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faf4a-118"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="faf4a-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="faf4a-119">Gibt an, dass der *lpdnsfqhostname* -Parameter nicht auf einen gültigen DNS-Namen verweist oder dass der *ulflags* -Parameter ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="faf4a-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="faf4a-120"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="faf4a-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="faf4a-121">Es steht nicht genügend Arbeitsspeicher zur Verfügung, um den Vorgang durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="faf4a-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="faf4a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faf4a-122">Requirements</span></span>



| <span data-ttu-id="faf4a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faf4a-123">Requirement</span></span> | <span data-ttu-id="faf4a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="faf4a-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf4a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="faf4a-125">Library</span></span><br/>                | <dl> <span data-ttu-id="faf4a-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="faf4a-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="faf4a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="faf4a-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="faf4a-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faf4a-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="faf4a-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="faf4a-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="faf4a-130">**Addlocalalternativen computernamew** (Unicode) und **addlocalalternativen computernamea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="faf4a-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="faf4a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faf4a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf4a-132">**Format des Computer \_ namens \_**</span><span class="sxs-lookup"><span data-stu-id="faf4a-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="faf4a-133">**DnsValidateName \_ W**</span><span class="sxs-lookup"><span data-stu-id="faf4a-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
