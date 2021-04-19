---
description: 'Weitere Informationen finden Sie hier: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364082"
---
# <a name="jet_ls"></a><span data-ttu-id="314ac-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="314ac-103">JET_LS</span></span>


<span data-ttu-id="314ac-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="314ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="314ac-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="314ac-105">JET_LS</span></span>

<span data-ttu-id="314ac-106">Der **JET_LS** -Datentyp enthält ein Kontext Handle für den lokalen Speicher (LS). Dieses Handle kann einem Cursor oder einer Tabelle zugeordnet werden und verweist möglicherweise auf dynamisch zugeordnete Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="314ac-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="314ac-107">**Windows XP: JET_LS** wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="314ac-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="314ac-108">Datentypen</span><span class="sxs-lookup"><span data-stu-id="314ac-108">Data Types</span></span>

<span data-ttu-id="314ac-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="314ac-109">JET_LS</span></span>

<span data-ttu-id="314ac-110">Der Wert JET_LSNil gibt ein ungültiges Kontext Handle an.</span><span class="sxs-lookup"><span data-stu-id="314ac-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="314ac-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="314ac-111">Remarks</span></span>

<span data-ttu-id="314ac-112">Ein Kontext Handle ist anfänglich mit dem **JET_LS** -Datentyp verknüpft, wobei [jetsetls](./jetsetls-function.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="314ac-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="314ac-113">Das Kontext Handle kann mithilfe von [jetgetls](./jetgetls-function.md)aus dem **JET_LS** -Datentyp abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="314ac-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="314ac-114">Das Kontext Handle kann explizit vom **JET_LS** -Datentyp mithilfe von [jetgetls](./jetgetls-function.md) mit JET_bitLSReset getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="314ac-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="314ac-115">Alternativ kann das Kontext Handle implizit vom **JET_LS** Datentyp getrennt werden, wenn das zugrunde liegende Objekt von der Datenbank-Engine als Ergebnis einer direkten oder indirekten Aktion durch die Anwendung freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="314ac-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="314ac-116">Im impliziten Fall wird ein Lauf Zeit Rückruf für die Anwendung ausgegeben, sodass er das Kontext Handle bereinigen kann.</span><span class="sxs-lookup"><span data-stu-id="314ac-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="314ac-117">Weitere Informationen zum impliziten Aufheben der Zuordnung des Datentyps **JET_LS** finden Sie unter [jetsetls](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="314ac-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="314ac-118">Die folgenden Flags sind dem JET_LS-Datentyp zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="314ac-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="314ac-119">Begriff</span><span class="sxs-lookup"><span data-stu-id="314ac-119">Term</span></span></p></th>
<th><p><span data-ttu-id="314ac-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="314ac-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314ac-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="314ac-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="314ac-122">Der Kontext Handle wird vom-Objekt getrennt.</span><span class="sxs-lookup"><span data-stu-id="314ac-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314ac-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="314ac-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="314ac-124">Legen Sie den einem Tabellen Cursor zugeordneten lokalen Speicher fest, oder rufen Sie ihn ab.</span><span class="sxs-lookup"><span data-stu-id="314ac-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314ac-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="314ac-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="314ac-126">Festlegen oder Abrufen des lokalen Speichers, der einer Tabelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="314ac-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314ac-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="314ac-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="314ac-128">Das Kontext Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="314ac-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="314ac-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="314ac-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314ac-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="314ac-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="314ac-131">Erfordert Windows Vista oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="314ac-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314ac-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="314ac-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="314ac-133">Erfordert Windows Server 2008 oder Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="314ac-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314ac-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="314ac-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="314ac-135">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="314ac-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="314ac-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="314ac-136">See Also</span></span>

[<span data-ttu-id="314ac-137">Jetsetls</span><span class="sxs-lookup"><span data-stu-id="314ac-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="314ac-138">Jetgetls</span><span class="sxs-lookup"><span data-stu-id="314ac-138">JetGetLS</span></span>](./jetgetls-function.md)
