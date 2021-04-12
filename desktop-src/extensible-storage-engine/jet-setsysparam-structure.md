---
description: 'Weitere Informationen finden Sie hier: JET_SETSYSPARAM Struktur'
title: JET_SETSYSPARAM Struktur
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342989"
---
# <a name="jet_setsysparam-structure"></a><span data-ttu-id="eece3-103">JET_SETSYSPARAM Struktur</span><span class="sxs-lookup"><span data-stu-id="eece3-103">JET_SETSYSPARAM Structure</span></span>


<span data-ttu-id="eece3-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eece3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setsysparam-structure"></a><span data-ttu-id="eece3-105">JET_SETSYSPARAM Struktur</span><span class="sxs-lookup"><span data-stu-id="eece3-105">JET_SETSYSPARAM Structure</span></span>

<span data-ttu-id="eece3-106">Ein Array von **JET_SETSYSPARAM** Strukturen gibt einen bestimmten Satz globaler Systemparameter an, die bei Verwendung der [jetenablemultiinstance](./jetenablemultiinstance-function.md) -Funktion als Argument festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eece3-106">An array of **JET_SETSYSPARAM** structures indicate a specific set of global system parameters that are set as an argument when using the [JetEnableMultiInstance](./jetenablemultiinstance-function.md) function.</span></span>

<span data-ttu-id="eece3-107">**Windows XP:** Diese Struktur wird in Windows XP eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eece3-107">**Windows XP:** This structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a><span data-ttu-id="eece3-108">Member</span><span class="sxs-lookup"><span data-stu-id="eece3-108">Members</span></span>

<span data-ttu-id="eece3-109">**paramid**</span><span class="sxs-lookup"><span data-stu-id="eece3-109">**paramid**</span></span>

<span data-ttu-id="eece3-110">Die ID des System Parameters, der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="eece3-110">The ID of the system parameter that will be set.</span></span>

<span data-ttu-id="eece3-111">Eine umfassende Liste der Systemparameter und deren Eigenschaften finden Sie unter [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="eece3-111">See [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md) for a complete list of system parameters and their properties.</span></span>

<span data-ttu-id="eece3-112">**lParam**</span><span class="sxs-lookup"><span data-stu-id="eece3-112">**lParam**</span></span>

<span data-ttu-id="eece3-113">Der optionale Wert, der für den ausgewählten Systemparameter festgelegt werden soll, wenn dieser Systemparameter einen ganzzahligen Typ hat.</span><span class="sxs-lookup"><span data-stu-id="eece3-113">The optional value to be set for the selected system parameter if that system parameter is of an integer type.</span></span>

<span data-ttu-id="eece3-114">**RT**</span><span class="sxs-lookup"><span data-stu-id="eece3-114">**sz**</span></span>

<span data-ttu-id="eece3-115">Der optionale Wert, der für den ausgewählten Systemparameter festgelegt werden soll, wenn dieser Systemparameter vom Typ String ist.</span><span class="sxs-lookup"><span data-stu-id="eece3-115">The optional value to be set for the selected system parameter if that system parameter is of a string type.</span></span>

<span data-ttu-id="eece3-116">**irre**</span><span class="sxs-lookup"><span data-stu-id="eece3-116">**err**</span></span>

<span data-ttu-id="eece3-117">Der Fehler, der sich aus dem Aufrufen von [jetsetsystemparameter](./jetsetsystemparameter-function.md) mit den zuvor angegebenen Parametern ergibt.</span><span class="sxs-lookup"><span data-stu-id="eece3-117">The error resulting from the call to [JetSetSystemParameter](./jetsetsystemparameter-function.md) with the previously specified parameters.</span></span>

### <a name="requirements"></a><span data-ttu-id="eece3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eece3-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eece3-119"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="eece3-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eece3-120">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="eece3-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eece3-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="eece3-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eece3-122">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="eece3-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eece3-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="eece3-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eece3-124">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="eece3-124">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eece3-125"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="eece3-125"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="eece3-126">Wird als <strong>JET_ SETSYSPARAM_W</strong> (Unicode) und <strong>JET_ SETSYSPARAM_A</strong> (ANSI) implementiert.</span><span class="sxs-lookup"><span data-stu-id="eece3-126">Implemented as <strong>JET_ SETSYSPARAM_W</strong> (Unicode) and <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="eece3-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eece3-127">See Also</span></span>

[<span data-ttu-id="eece3-128">System Parameter für Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="eece3-128">Extensible Storage Engine System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)  
[<span data-ttu-id="eece3-129">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="eece3-129">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="eece3-130">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eece3-130">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eece3-131">Jetenablemultiinstance</span><span class="sxs-lookup"><span data-stu-id="eece3-131">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="eece3-132">Jetsetsystemparameter</span><span class="sxs-lookup"><span data-stu-id="eece3-132">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
