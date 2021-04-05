---
description: Weitere Informationen finden Sie in der API. jetsetcolumns-Methode.
title: API. jetsetcolumns-Methode
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750753"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="7c9c5-103">API. jetsetcolumns-Methode</span><span class="sxs-lookup"><span data-stu-id="7c9c5-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="7c9c5-104">Ermöglicht einer Anwendung das Festlegen mehrerer Spaltenwerte in einem einzelnen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="7c9c5-105">Ein Array von [JET_SETCOLUMN](./jet-setcolumn-class.md) Strukturen wird verwendet, um den Satz von Spaltenwerten zu beschreiben, die festgelegt werden sollen, und um Eingabepuffer für jeden festzulegenden Spaltenwert zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="7c9c5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7c9c5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7c9c5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7c9c5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9c5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c9c5-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="7c9c5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c9c5-109">Parameters</span></span>

  - <span data-ttu-id="7c9c5-110">-sid</span><span class="sxs-lookup"><span data-stu-id="7c9c5-110">sesid</span></span>  
    <span data-ttu-id="7c9c5-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c9c5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7c9c5-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c9c5-113">TableID</span><span class="sxs-lookup"><span data-stu-id="7c9c5-113">tableid</span></span>  
    <span data-ttu-id="7c9c5-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c9c5-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7c9c5-115">Der Cursor, für den die Spalten festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c9c5-116">SetColumns</span><span class="sxs-lookup"><span data-stu-id="7c9c5-116">setcolumns</span></span>  
    <span data-ttu-id="7c9c5-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="7c9c5-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="7c9c5-118">Ein Array von [JET_SETCOLUMN](./jet-setcolumn-class.md) -Strukturen, die die festzulegenden Daten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c9c5-119">NumColumns</span><span class="sxs-lookup"><span data-stu-id="7c9c5-119">numColumns</span></span>  
    <span data-ttu-id="7c9c5-120">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7c9c5-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7c9c5-121">Anzahl der Einträge im SetColumns-Parameter.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7c9c5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c9c5-122">Return value</span></span>

<span data-ttu-id="7c9c5-123">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7c9c5-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7c9c5-124">Eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-124">A warning.</span></span> <span data-ttu-id="7c9c5-125">Wenn für den letzten Spalten Satz eine Warnung angezeigt wird, wird diese Warnung von jetsetcolumns selbst zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c9c5-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7c9c5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c9c5-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7c9c5-127">Referenz</span><span class="sxs-lookup"><span data-stu-id="7c9c5-127">Reference</span></span>

[<span data-ttu-id="7c9c5-128">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="7c9c5-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7c9c5-129">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="7c9c5-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7c9c5-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="7c9c5-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
