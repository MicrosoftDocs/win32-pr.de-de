---
description: Schließt ein Handle für einen Druck ticketanbieter.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Unbindptproviderthunk-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363455"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="30ef0-103">Unbindptproviderthunk-Funktion</span><span class="sxs-lookup"><span data-stu-id="30ef0-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="30ef0-104">\[Diese Funktion wird nicht unterstützt und wird in zukünftigen Versionen von Windows möglicherweise deaktiviert oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="30ef0-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="30ef0-105">[**Ptcloseprovider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) bietet gleichwertige Funktionen und sollte stattdessen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="30ef0-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="30ef0-106">Schließt ein Handle für einen Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="30ef0-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ef0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ef0-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="30ef0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30ef0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ef0-109">*hprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30ef0-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ef0-110">Ein Handle für einen geöffneten Druck ticketanbieter.</span><span class="sxs-lookup"><span data-stu-id="30ef0-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="30ef0-111">Dieses Handle wird von der [**bindptproviderthunk**](bindptproviderthunk.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30ef0-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ef0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30ef0-112">Return value</span></span>

<span data-ttu-id="30ef0-113">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück; andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30ef0-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="30ef0-114">Weitere Informationen zu COM-Fehlercodes finden Sie unter [Fehlerbehandlung](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="30ef0-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30ef0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30ef0-115">Requirements</span></span>



| <span data-ttu-id="30ef0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30ef0-116">Requirement</span></span> | <span data-ttu-id="30ef0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="30ef0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30ef0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30ef0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="30ef0-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30ef0-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="30ef0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30ef0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="30ef0-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30ef0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="30ef0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="30ef0-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ef0-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ef0-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ef0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30ef0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ef0-125">Druck Schema</span><span class="sxs-lookup"><span data-stu-id="30ef0-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="30ef0-126">**Ptcloseprovider**</span><span class="sxs-lookup"><span data-stu-id="30ef0-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="30ef0-127">Drucken</span><span class="sxs-lookup"><span data-stu-id="30ef0-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="30ef0-128">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="30ef0-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

