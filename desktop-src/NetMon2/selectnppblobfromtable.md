---
description: Die selectnppblobfromtable-Funktion wählt eine NIC aus einer angegebenen NPP-BLOB-Tabelle aus.
ms.assetid: 7f8010ed-472a-49b2-8d97-92851b6c14cd
title: Selectnppblobfromtable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectNPPBlobFromTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d8f504d76d43b8a398947f435f7bd488678ea394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214758"
---
# <a name="selectnppblobfromtable-function"></a><span data-ttu-id="d96b6-103">Selectnppblobfromtable-Funktion</span><span class="sxs-lookup"><span data-stu-id="d96b6-103">SelectNPPBlobFromTable function</span></span>

<span data-ttu-id="d96b6-104">Die **selectnppblobfromtable** -Funktion wählt eine NIC aus einer angegebenen NPP-BLOB-Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="d96b6-104">The **SelectNPPBlobFromTable** function selects a NIC from a supplied NPP BLOB table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d96b6-105">Syntax</span></span>


```C++
DWORD SelectNPPBlobFromTable(
  _In_  HWND        hwnd,
  _In_  PBLOB_TABLE pBlobTable,
  _Out_ HBLOB       *hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d96b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d96b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d96b6-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d96b6-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d96b6-108">Handle für das Fenster, das das Dialogfeld " **Netzwerk auswählen** " anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d96b6-108">Handle to the window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="d96b6-109">*pblobtable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d96b6-109">*pBlobTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d96b6-110">Ein Zeiger auf die angegebene BLOB-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d96b6-110">Pointer to the supplied BLOB table.</span></span> <span data-ttu-id="d96b6-111">Netzwerkmonitor verwendet diese Tabelle, um das Dialogfeld **Netzwerk auswählen** aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="d96b6-111">Network Monitor uses this table to populate the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="d96b6-112">*hblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d96b6-112">*hBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d96b6-113">Handle für das BLOB, das die ausgewählte NIC darstellt.</span><span class="sxs-lookup"><span data-stu-id="d96b6-113">Handle to the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d96b6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d96b6-114">Return value</span></span>

<span data-ttu-id="d96b6-115">Wenn die Funktion erfolgreich ausgeführt wurde und der Benutzer eine NIC auswählt, ist der Rückgabewert nmerr \_ Success; das BLOB, auf das *hblob* verweist, wird ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d96b6-115">If the function is successful and the user selects a NIC, the return value is NMERR\_SUCCESS; the BLOB pointed to by *hBlob* is filled in.</span></span>

<span data-ttu-id="d96b6-116">Wenn der Benutzer keine NIC auswählt, wird der Rückgabewert nmerr \_ No \_ NPP \_ ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d96b6-116">If the user does not select a NIC, the return value is NMERR\_NO\_NPP\_SELECTED.</span></span>

<span data-ttu-id="d96b6-117">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein weiterer nmerr-Wert.</span><span class="sxs-lookup"><span data-stu-id="d96b6-117">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d96b6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d96b6-118">Remarks</span></span>

<span data-ttu-id="d96b6-119">Wenn Sie aufgerufen wird, zeigt Netzwerkmonitor das Dialogfeld **Netzwerk auswählen** an, mit dem Sie eine NIC auswählen können.</span><span class="sxs-lookup"><span data-stu-id="d96b6-119">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="d96b6-120">Das NPP-BLOB, das die ausgewählte NIC darstellt, kehrt zur aufrufenden Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="d96b6-120">The NPP BLOB that represents the selected NIC returns to the calling application.</span></span>

<span data-ttu-id="d96b6-121">Weitere Informationen zu den verschiedenen Möglichkeiten, NICs auszuwählen, finden Sie unter [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) .</span><span class="sxs-lookup"><span data-stu-id="d96b6-121">To learn the various ways you can select NICs, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="d96b6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d96b6-122">Requirements</span></span>



| <span data-ttu-id="d96b6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d96b6-123">Requirement</span></span> | <span data-ttu-id="d96b6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d96b6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d96b6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d96b6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d96b6-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d96b6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d96b6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d96b6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d96b6-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d96b6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d96b6-129">Header</span><span class="sxs-lookup"><span data-stu-id="d96b6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d96b6-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d96b6-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d96b6-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d96b6-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d96b6-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d96b6-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d96b6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d96b6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d96b6-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d96b6-134"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d96b6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d96b6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d96b6-136">Getnppblobfromui</span><span class="sxs-lookup"><span data-stu-id="d96b6-136">GetNPPBlobFromUI</span></span>](getnppblobfromui.md)
</dt> <dt>

[<span data-ttu-id="d96b6-137">Getnppblobtable</span><span class="sxs-lookup"><span data-stu-id="d96b6-137">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="d96b6-138">Spezielle BLOB-Einträge</span><span class="sxs-lookup"><span data-stu-id="d96b6-138">Special BLOB Entries</span></span>](special-blob-entries.md)
</dt> </dl>

 

 




