---
description: 'Weitere Informationen: Konvertierungen von Membern'
title: Konvertierungs Elemente
TOCTitle: Conversions members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Conversions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions_members(v=EXCHG.10)
ms:contentKeyID: 55107253
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7e192b338c1d19b207b7e7e242289ca7f6782175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130204"
---
# <a name="conversions-members"></a><span data-ttu-id="110fc-103">Konvertierungs Elemente</span><span class="sxs-lookup"><span data-stu-id="110fc-103">Conversions members</span></span>

<span data-ttu-id="110fc-104">Geschützte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="110fc-104">Include protected members</span></span>  
<span data-ttu-id="110fc-105">Geerbte Member einschließen</span><span class="sxs-lookup"><span data-stu-id="110fc-105">Include inherited members</span></span>  

<span data-ttu-id="110fc-106">Stellen Sie Methoden zum Konvertieren von Daten und Flags zwischen Win32 und dem .NET Framework bereit.</span><span class="sxs-lookup"><span data-stu-id="110fc-106">Provide methods to convert data and flags between Win32 and the .NET Framework.</span></span>

<span data-ttu-id="110fc-107">Der [konvertiertyp](./conversions-class.md) macht die folgenden Member verfügbar.</span><span class="sxs-lookup"><span data-stu-id="110fc-107">The [Conversions](./conversions-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="110fc-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="110fc-108">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="110fc-109">Name</span><span class="sxs-lookup"><span data-stu-id="110fc-109">Name</span></span></th>
<th><span data-ttu-id="110fc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="110fc-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="110fc-113"><a href="dn334187(v=exchg.10).md">Compareoptionsfromlcmapflags</a></span><span class="sxs-lookup"><span data-stu-id="110fc-113"><a href="dn334187(v=exchg.10).md">CompareOptionsFromLCMapFlags</a></span></span></td>
<td><span data-ttu-id="110fc-114">Die angegebenen Flags für lcmapflags werden in Vergleichs Optionen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="110fc-114">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="110fc-115">Unbekannte Optionen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="110fc-115">Unknown options are ignored.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="110fc-118"><a href="dn334235(v=exchg.10).md">Convertdoubleumdatetime</a></span><span class="sxs-lookup"><span data-stu-id="110fc-118"><a href="dn334235(v=exchg.10).md">ConvertDoubleToDateTime</a></span></span></td>
<td><span data-ttu-id="110fc-119">Konvertiert ein Double (OA-Datums-/Uhrzeitformat) in einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="110fc-119">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="110fc-120">Anders als DateTime. fromuadate löst dies keine Ausnahmen aus.</span><span class="sxs-lookup"><span data-stu-id="110fc-120">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Öffentliche Methode" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Statischer Member" alt="Static member" /></td>
<td><span data-ttu-id="110fc-123"><a href="dn334186(v=exchg.10).md">Lcmapflagsfromcompareoptions</a></span><span class="sxs-lookup"><span data-stu-id="110fc-123"><a href="dn334186(v=exchg.10).md">LCMapFlagsFromCompareOptions</a></span></span></td>
<td><span data-ttu-id="110fc-124">Legen Sie CompareOptions fest, und wandeln Sie Sie aus LCMapString in Flags um.</span><span class="sxs-lookup"><span data-stu-id="110fc-124">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="110fc-125">Unbekannte Optionen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="110fc-125">Unknown options are ignored.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="110fc-126">Oben</span><span class="sxs-lookup"><span data-stu-id="110fc-126">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="110fc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="110fc-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="110fc-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="110fc-128">Reference</span></span>

[<span data-ttu-id="110fc-129">Konvertierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="110fc-129">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="110fc-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="110fc-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
