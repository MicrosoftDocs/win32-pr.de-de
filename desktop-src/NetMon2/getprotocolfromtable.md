---
description: Die getprotocolfromtable-Funktion gibt ein Handle für ein Protokoll&\# 8212; basierend auf einer angegebenen Übergabe Tabelle und einem angegebenen Wert zurück.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Getprotocolfromtable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958709"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="0c0e7-103">Getprotocolfromtable-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c0e7-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="0c0e7-104">Die **getprotocolfromtable** -Funktion gibt ein Handle für ein Protokoll zurück, das auf einer angegebenen Übergabe Tabelle und einem angegebenen Wert basiert.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c0e7-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="0c0e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c0e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c0e7-107">*htable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c0e7-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0e7-108">Handle für eine Übergabe Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="0c0e7-109">*Itemtefind* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c0e7-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0e7-110">Der Wert, der verwendet wird, um das Protokoll in einer Übergabe Tabelle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="0c0e7-111">Der Wert muss in den Protokolldaten verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="0c0e7-112">*lpinstdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0c0e7-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0e7-113">Wenn Sie in der Übergabe Tabelle verfügbar sind, Instanzdaten für das nächste Protokoll.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="0c0e7-114">Instanzdaten dürfen nicht länger sein als eine Länge von DWORD \_ ptr.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c0e7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c0e7-115">Return value</span></span>

<span data-ttu-id="0c0e7-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Protokoll handle.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="0c0e7-117">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c0e7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c0e7-118">Remarks</span></span>

<span data-ttu-id="0c0e7-119">Beim Implementieren der " [Erkennungs](recognizeframe.md) Funktion"-Exportfunktion wird die **getprotocolfromtable** -Funktion verwendet, um ein Handle für das nächste Protokoll zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="0c0e7-120">Die **getprotocolfromtable** -Funktion wird aufgerufen, um ein Handle aus dem nächsten Protokoll abzurufen, wenn das Protokoll angibt, welches Protokoll befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="0c0e7-121">**Instanzdaten**</span><span class="sxs-lookup"><span data-stu-id="0c0e7-121">**Instance data**</span></span>

<span data-ttu-id="0c0e7-122">Instanzdaten können beliebige Daten sein, die kleiner oder gleich einem DWORD- \_ ptr sind, oder ein Zeiger auf Daten, wie z. b. unformatierte Frame-Daten, die nicht vom Parser zugeordnet oder freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0c0e7-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c0e7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c0e7-123">Requirements</span></span>



| <span data-ttu-id="0c0e7-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c0e7-124">Requirement</span></span> | <span data-ttu-id="0c0e7-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0c0e7-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0e7-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c0e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0e7-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c0e7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0c0e7-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c0e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0e7-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c0e7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0c0e7-130">Header</span><span class="sxs-lookup"><span data-stu-id="0c0e7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c0e7-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c0e7-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0c0e7-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c0e7-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c0e7-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c0e7-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c0e7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0c0e7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c0e7-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c0e7-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c0e7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c0e7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0e7-137">Erkenzeframe</span><span class="sxs-lookup"><span data-stu-id="0c0e7-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




