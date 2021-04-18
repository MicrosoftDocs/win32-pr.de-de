---
description: 'Weitere Informationen finden Sie hier: JET_SNP-Enumeration'
title: JET_SNP-Enumeration
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344247"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="dd697-103">JET_SNP-Enumeration</span><span class="sxs-lookup"><span data-stu-id="dd697-103">JET_SNP enumeration</span></span>

<span data-ttu-id="dd697-104">Der Typ des Vorgangs, für den der Status gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="dd697-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="dd697-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dd697-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dd697-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dd697-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dd697-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd697-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="dd697-108">Member</span><span class="sxs-lookup"><span data-stu-id="dd697-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="dd697-109">Membername</span><span class="sxs-lookup"><span data-stu-id="dd697-109">Member name</span></span></th>
<th><span data-ttu-id="dd697-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd697-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dd697-111">Reparieren</span><span class="sxs-lookup"><span data-stu-id="dd697-111">Repair</span></span></td>
<td><span data-ttu-id="dd697-112">Der Rückruf ist für eine Reparaturoption vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="dd697-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dd697-113">Kompakt</span><span class="sxs-lookup"><span data-stu-id="dd697-113">Compact</span></span></td>
<td><span data-ttu-id="dd697-114">Der Rückruf ist für die Daten Bank Defragmentierung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="dd697-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dd697-115">Restore</span><span class="sxs-lookup"><span data-stu-id="dd697-115">Restore</span></span></td>
<td><span data-ttu-id="dd697-116">Rückruf ist für Wiederherstellungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="dd697-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dd697-117">Backup</span><span class="sxs-lookup"><span data-stu-id="dd697-117">Backup</span></span></td>
<td><span data-ttu-id="dd697-118">Rückruf ist für Sicherungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="dd697-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dd697-119">Volumebereinigung</span><span class="sxs-lookup"><span data-stu-id="dd697-119">Scrub</span></span></td>
<td><span data-ttu-id="dd697-120">Der Rückruf ist für die Daten Bank nulgung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="dd697-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dd697-121">Upgraderecordformat</span><span class="sxs-lookup"><span data-stu-id="dd697-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="dd697-122">Der Rückruf dient zum Aktualisieren des Daten Satz Formats aller Datenbankseiten.</span><span class="sxs-lookup"><span data-stu-id="dd697-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="dd697-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd697-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dd697-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="dd697-124">Reference</span></span>

[<span data-ttu-id="dd697-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd697-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
