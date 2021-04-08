---
description: Wählt eine Register-NIC aus.
ms.assetid: 27814a40-6933-498b-a0d2-535698b1e402
title: Getnppblobfromui-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobFromUI
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 4ff3887f10d35ec3b66d8eaaf1443140c768ca55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960023"
---
# <a name="getnppblobfromui-function"></a><span data-ttu-id="cf5db-103">Getnppblobfromui-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf5db-103">GetNPPBlobFromUI function</span></span>

<span data-ttu-id="cf5db-104">Die **getnppblobfromui** -Funktion wählt eine Register-NIC aus.</span><span class="sxs-lookup"><span data-stu-id="cf5db-104">The **GetNPPBlobFromUI** function selects a register NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf5db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf5db-105">Syntax</span></span>


```C++
DWORD GetNPPBlobFromUI(
  _In_  HWND  hwnd,
  _In_  HBLOB hFilterBlob,
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="cf5db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf5db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf5db-107">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf5db-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5db-108">Ein Handle für ein Fenster, das das Dialogfeld " **Netzwerk auswählen** " anzeigt.</span><span class="sxs-lookup"><span data-stu-id="cf5db-108">A handle to a window that displays the **Select a network** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="cf5db-109">*hfilterblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf5db-109">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5db-110">Ein Handle für ein [*filterblob*](f.md) , das verwendet wird, um einzuschränken, welche NICs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cf5db-110">A handle to a [*filter BLOB*](f.md) used to limit which NICs are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="cf5db-111">*phblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf5db-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf5db-112">Ein Zeiger auf das Handle des BLOBs, das die ausgewählte NIC darstellt.</span><span class="sxs-lookup"><span data-stu-id="cf5db-112">A pointer to the handle of the BLOB that represents the selected NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf5db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf5db-113">Return value</span></span>

<span data-ttu-id="cf5db-114">Wenn die Funktion erfolgreich ist (der Benutzer wählt eine NIC aus), ist der Rückgabewert nmerr \_ Success, und das BLOB, auf das *phblob* verweist, wird ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="cf5db-114">If the function is successful (the user selects a NIC), the return value is NMERR\_SUCCESS, and the BLOB that *phBlob* points to is filled in.</span></span>

<span data-ttu-id="cf5db-115">Wenn der Benutzer keine NIC auswählt, wird der Rückgabewert **nmerr \_ No \_ NPP \_ ausgewählt**.</span><span class="sxs-lookup"><span data-stu-id="cf5db-115">If the user does not select an NIC, the return value is **NMERR\_NO\_NPP\_SELECTED**.</span></span>

<span data-ttu-id="cf5db-116">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein weiterer nmerr-Wert.</span><span class="sxs-lookup"><span data-stu-id="cf5db-116">If the function is unsuccessful, the return value is another NMERR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf5db-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf5db-117">Remarks</span></span>

<span data-ttu-id="cf5db-118">Wenn Sie aufgerufen wird, zeigt Netzwerkmonitor das Dialogfeld **Netzwerk auswählen** an, mit dem Sie eine NIC auswählen können.</span><span class="sxs-lookup"><span data-stu-id="cf5db-118">When called, Network Monitor displays the **Select a network** dialog box, which you can use to select a NIC.</span></span> <span data-ttu-id="cf5db-119">Das NPP-BLOB, das die NIC darstellt, wird an die aufrufenden Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf5db-119">The NPP BLOB that represents the NIC is returned to the calling application.</span></span>

<span data-ttu-id="cf5db-120">Wenn das von *hfilterblob* benannte BLOB ein [*spezielles BLOB*](s.md)ist, versucht der Finder, es zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cf5db-120">If the BLOB named by *hFilterBlob* is a [*special BLOB*](s.md), the finder will attempt to process it.</span></span> <span data-ttu-id="cf5db-121">Ein Beispiel wäre ein-Befehl, der zuvor ein spezielles BLOB von der Remote-NPP zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="cf5db-121">An example would be a call that had previously returned a special BLOB from the remote NPP.</span></span> <span data-ttu-id="cf5db-122">Die Anwendung hat das erforderliche Tag, den Computernamen, eingefügt \_ .</span><span class="sxs-lookup"><span data-stu-id="cf5db-122">The application inserted the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="cf5db-123">In dieser Situation übergibt der Finder dieses BLOB an den NPP-Remote Computer, der dann eine Tabelle mit NPP-BLOBs zurückgibt, die den angeforderten Computer darstellen.</span><span class="sxs-lookup"><span data-stu-id="cf5db-123">In this situation, the finder would pass this BLOB to the remote NPP, which would then return a table of NPP BLOBs representing the machine requested.</span></span> <span data-ttu-id="cf5db-124">Diese NPP-Remote-Blobfelder werden im Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf5db-124">These remote NPP BLOBs would appear in the dialog box.</span></span>

<span data-ttu-id="cf5db-125">Der Aufrufer muss die [destroyblob](destroyblob.md) -Funktion aufzurufen, die das zurückgegebene BLOB zerstört, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="cf5db-125">The caller must call the [DestroyBlob](destroyblob.md) function, which destroys the returned BLOB when it is no longer required.</span></span>



| <span data-ttu-id="cf5db-126">Weitere Informationen über</span><span class="sxs-lookup"><span data-stu-id="cf5db-126">For more information about</span></span> | <span data-ttu-id="cf5db-127">Siehe</span><span class="sxs-lookup"><span data-stu-id="cf5db-127">See</span></span>                                                                          |
|----------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cf5db-128">Drei Möglichkeiten zum Auswählen von NICs</span><span class="sxs-lookup"><span data-stu-id="cf5db-128">Three ways to select NICs</span></span>  | [<span data-ttu-id="cf5db-129">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="cf5db-129">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |
| <span data-ttu-id="cf5db-130">Angeben eines filterblobs</span><span class="sxs-lookup"><span data-stu-id="cf5db-130">Specifying a filter BLOB</span></span>   | [<span data-ttu-id="cf5db-131">Angeben eines filterblobs</span><span class="sxs-lookup"><span data-stu-id="cf5db-131">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                     |



 

## <a name="requirements"></a><span data-ttu-id="cf5db-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf5db-132">Requirements</span></span>



| <span data-ttu-id="cf5db-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf5db-133">Requirement</span></span> | <span data-ttu-id="cf5db-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cf5db-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf5db-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf5db-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cf5db-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf5db-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cf5db-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf5db-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cf5db-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf5db-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf5db-139">Header</span><span class="sxs-lookup"><span data-stu-id="cf5db-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf5db-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf5db-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="cf5db-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf5db-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf5db-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf5db-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf5db-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cf5db-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf5db-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf5db-144"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf5db-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf5db-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf5db-146">Getnppblobtable</span><span class="sxs-lookup"><span data-stu-id="cf5db-146">GetNPPBlobTable</span></span>](getnppblobtable.md)
</dt> <dt>

[<span data-ttu-id="cf5db-147">Selectnppblobfromtable</span><span class="sxs-lookup"><span data-stu-id="cf5db-147">SelectNPPBlobFromTable</span></span>](selectnppblobfromtable.md)
</dt> </dl>

 

 




