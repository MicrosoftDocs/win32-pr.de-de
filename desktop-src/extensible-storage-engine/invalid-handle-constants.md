---
description: 'Weitere Informationen: Ungültige handle-Konstanten'
title: Ungültige handle-Konstanten
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050408"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="998e9-103">Ungültige handle-Konstanten</span><span class="sxs-lookup"><span data-stu-id="998e9-103">Invalid Handle Constants</span></span>


<span data-ttu-id="998e9-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="998e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="998e9-105">Ungültige handle-Konstanten</span><span class="sxs-lookup"><span data-stu-id="998e9-105">Invalid Handle Constants</span></span>

<span data-ttu-id="998e9-106">Die folgenden Konstanten weisen auf ungültige Handles für verschiedene Aspekte von ESE hin.</span><span class="sxs-lookup"><span data-stu-id="998e9-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="998e9-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="998e9-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="998e9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="998e9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="998e9-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="998e9-109">JET_instanceNil</span></span><br />
<span data-ttu-id="998e9-110">(~ (JET_INSTANCE) 0)</span><span class="sxs-lookup"><span data-stu-id="998e9-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="998e9-111">Ein ungültiges Handle für eine Daten Bank Instanz.</span><span class="sxs-lookup"><span data-stu-id="998e9-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="998e9-112">
<strong>Windows XP:</strong> Eingeführt in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="998e9-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="998e9-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="998e9-113">JET_sesidNil</span></span><br />
<span data-ttu-id="998e9-114">(~ (JET_SESID) 0)</span><span class="sxs-lookup"><span data-stu-id="998e9-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="998e9-115">Ein ungültiges Handle für eine Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="998e9-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="998e9-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="998e9-116">JET_tableidNil</span></span><br />
<span data-ttu-id="998e9-117">(~ (JET_TABLEID) 0)</span><span class="sxs-lookup"><span data-stu-id="998e9-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="998e9-118">Ein ungültiges Handle für eine Tabellen-ID.</span><span class="sxs-lookup"><span data-stu-id="998e9-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="998e9-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="998e9-119">JET_bitNil</span></span><br />
<span data-ttu-id="998e9-120">((JET_GRBIT) 0)</span><span class="sxs-lookup"><span data-stu-id="998e9-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="998e9-121">Ein ungültiges Handle für eine Gruppe von Bits.</span><span class="sxs-lookup"><span data-stu-id="998e9-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="998e9-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="998e9-122">JET_LSNil</span></span><br />
<span data-ttu-id="998e9-123">(~ (JET_LS) 0)</span><span class="sxs-lookup"><span data-stu-id="998e9-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="998e9-124">Ein ungültiges Handle für den lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="998e9-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="998e9-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="998e9-125">JET_dbidNil</span></span><br />
<span data-ttu-id="998e9-126">((JET_DBID) 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="998e9-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="998e9-127">Ein ungültiges Handle für die Datenbank-ID.</span><span class="sxs-lookup"><span data-stu-id="998e9-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="998e9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="998e9-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="998e9-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="998e9-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="998e9-130">Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="998e9-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="998e9-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="998e9-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="998e9-132">Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="998e9-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="998e9-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="998e9-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="998e9-134">In "ESENT. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="998e9-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

