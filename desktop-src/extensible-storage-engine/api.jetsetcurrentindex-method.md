---
description: Weitere Informationen finden Sie in der API. jetsetcurrentindex-Methode.
title: API. jetsetcurrentindex-Methode
TOCTitle: 'JetSetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed3c069962fe879e250f90e34744780dfe2eb862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363772"
---
# <a name="apijetsetcurrentindex-method"></a><span data-ttu-id="489e5-103">API. jetsetcurrentindex-Methode</span><span class="sxs-lookup"><span data-stu-id="489e5-103">Api.JetSetCurrentIndex method</span></span>

<span data-ttu-id="489e5-104">Legen Sie den aktuellen Index eines Cursors fest.</span><span class="sxs-lookup"><span data-stu-id="489e5-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="489e5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="489e5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="489e5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="489e5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="489e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="489e5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetSetCurrentIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetSetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="489e5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="489e5-108">Parameters</span></span>

  - <span data-ttu-id="489e5-109">-sid</span><span class="sxs-lookup"><span data-stu-id="489e5-109">sesid</span></span>  
    <span data-ttu-id="489e5-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="489e5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="489e5-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="489e5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="489e5-112">TableID</span><span class="sxs-lookup"><span data-stu-id="489e5-112">tableid</span></span>  
    <span data-ttu-id="489e5-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="489e5-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="489e5-114">Der Cursor, für den der Index festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="489e5-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="489e5-115">Index</span><span class="sxs-lookup"><span data-stu-id="489e5-115">index</span></span>  
    <span data-ttu-id="489e5-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="489e5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="489e5-117">Der Name des Indexes, der ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="489e5-117">The name of the index to be selected.</span></span> <span data-ttu-id="489e5-118">Wenn dieser Wert NULL oder leer ist, wird der primäre Index ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="489e5-118">If this is null or empty the primary index will be selected.</span></span>

## <a name="see-also"></a><span data-ttu-id="489e5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="489e5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="489e5-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="489e5-120">Reference</span></span>

[<span data-ttu-id="489e5-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="489e5-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="489e5-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="489e5-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="489e5-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="489e5-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
