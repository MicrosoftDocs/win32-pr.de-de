---
description: Weitere Informationen finden Sie in der API. getcolumndictionary-Methode.
title: API. getcolumndictionary-Methode
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342803"
---
# <a name="apigetcolumndictionary-method"></a><span data-ttu-id="fb9b1-103">API. getcolumndictionary-Methode</span><span class="sxs-lookup"><span data-stu-id="fb9b1-103">Api.GetColumnDictionary method</span></span>

<span data-ttu-id="fb9b1-104">Erstellt ein Wörterbuch, das Spaltennamen ihren Spalten-IDs zuordnet.</span><span class="sxs-lookup"><span data-stu-id="fb9b1-104">Creates a dictionary which maps column names to their column IDs.</span></span>

<span data-ttu-id="fb9b1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb9b1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fb9b1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fb9b1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb9b1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="fb9b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb9b1-108">Parameters</span></span>

  - <span data-ttu-id="fb9b1-109">-sid</span><span class="sxs-lookup"><span data-stu-id="fb9b1-109">sesid</span></span>  
    <span data-ttu-id="fb9b1-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb9b1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fb9b1-111">Die zu verwendende-sid.</span><span class="sxs-lookup"><span data-stu-id="fb9b1-111">The sesid to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fb9b1-112">TableID</span><span class="sxs-lookup"><span data-stu-id="fb9b1-112">tableid</span></span>  
    <span data-ttu-id="fb9b1-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb9b1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fb9b1-114">Die Tabelle, für die die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb9b1-114">The table to retrieve the information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fb9b1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb9b1-115">Return value</span></span>

<span data-ttu-id="fb9b1-116">Typ: [System. Collections. Generic. IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span><span class="sxs-lookup"><span data-stu-id="fb9b1-116">Type: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span></span>  
<span data-ttu-id="fb9b1-117">Ein Wörterbuch, das Spaltennamen für Spalten-IDs entspricht.</span><span class="sxs-lookup"><span data-stu-id="fb9b1-117">A dictionary mapping column names to column IDs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb9b1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb9b1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb9b1-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="fb9b1-119">Reference</span></span>

[<span data-ttu-id="fb9b1-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb9b1-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fb9b1-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="fb9b1-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fb9b1-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb9b1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
