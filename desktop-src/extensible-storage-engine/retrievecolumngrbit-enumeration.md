---
description: 'Weitere Informationen finden Sie hier: retrievecolumngrbit-Enumeration'
title: Retrievecolumngrbit-Enumeration
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349452"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="e567a-103">Retrievecolumngrbit-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e567a-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="e567a-104">Optionen für jetretrievecolumgen.</span><span class="sxs-lookup"><span data-stu-id="e567a-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="e567a-105">Diese Enumeration enthält ein [FlagsAttribute](/dotnet/api/system.flagsattribute)-Attribut, das eine bitweise Kombination der Memberwerte zulässt.</span><span class="sxs-lookup"><span data-stu-id="e567a-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="e567a-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e567a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e567a-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e567a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e567a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e567a-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="e567a-109">Member</span><span class="sxs-lookup"><span data-stu-id="e567a-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e567a-110">Membername</span><span class="sxs-lookup"><span data-stu-id="e567a-110">Member name</span></span></th>
<th><span data-ttu-id="e567a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e567a-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e567a-112">Keine</span><span class="sxs-lookup"><span data-stu-id="e567a-112">None</span></span></td>
<td><span data-ttu-id="e567a-113">Standardoptionen.</span><span class="sxs-lookup"><span data-stu-id="e567a-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e567a-114">Retrievecopy</span><span class="sxs-lookup"><span data-stu-id="e567a-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="e567a-115">Dieses Flag bewirkt, dass die Spalte "abrufen" den geänderten Wert anstelle des ursprünglichen Werts abruft.</span><span class="sxs-lookup"><span data-stu-id="e567a-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="e567a-116">Wenn der Wert nicht geändert wurde, wird der ursprüngliche Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e567a-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="e567a-117">Auf diese Weise kann ein Wert, der noch nicht eingefügt oder aktualisiert wurde, beim Einfügen oder Aktualisieren eines Datensatzes abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e567a-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e567a-118">"Retrievefromindex"</span><span class="sxs-lookup"><span data-stu-id="e567a-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="e567a-119">Diese Option wird verwendet, um nach Möglichkeit Spaltenwerte aus dem Index abzurufen, ohne auf den Datensatz zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e567a-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="e567a-120">Auf diese Weise kann das unnötige Laden von Datensätzen vermieden werden, wenn benötigte Daten aus Indexeinträgen selbst verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e567a-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e567a-121">Retrievefromprimarybookmark</span><span class="sxs-lookup"><span data-stu-id="e567a-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="e567a-122">Diese Option wird zum Abrufen von Spaltenwerten aus dem Index-Lesezeichen verwendet und unterscheidet sich möglicherweise vom Indexwert, wenn eine Spalte sowohl im primären Index als auch im aktuellen Index angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e567a-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="e567a-123">Diese Option sollte nicht angegeben werden, wenn der aktuelle Index der gruppierte Index oder der primäre Index ist.</span><span class="sxs-lookup"><span data-stu-id="e567a-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="e567a-124">Dieses Bit kann nicht festgelegt werden, wenn "retrievefromindex" ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e567a-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e567a-125">Retrievetag</span><span class="sxs-lookup"><span data-stu-id="e567a-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="e567a-126">Diese Option wird verwendet, um die Sequenznummer eines mehrwertigen Spaltenwerts in JET_RETINFO. itagsequence abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e567a-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="e567a-127">Das Abrufen der Sequenznummer kann ein kostspieliger Vorgang sein und sollte nur bei Bedarf ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e567a-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="e567a-128">Abrufen von evenull</span><span class="sxs-lookup"><span data-stu-id="e567a-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="e567a-129">Diese Option wird verwendet, um NULL-Werte für mehrwertige Spalten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e567a-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="e567a-130">Wenn diese Option nicht angegeben ist, werden NULL-Werte für mehrwertige Spalten automatisch übersprungen.</span><span class="sxs-lookup"><span data-stu-id="e567a-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="e567a-131">Retrieveignoredefault</span><span class="sxs-lookup"><span data-stu-id="e567a-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="e567a-132">Diese Option wirkt sich nur auf mehrwertige Spalten aus und bewirkt, dass ein NULL-Wert zurückgegeben wird, wenn die angeforderte Sequenznummer 1 ist und für die Spalte im Datensatz keine Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e567a-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="e567a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e567a-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e567a-134">Referenz</span><span class="sxs-lookup"><span data-stu-id="e567a-134">Reference</span></span>

[<span data-ttu-id="e567a-135">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e567a-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
