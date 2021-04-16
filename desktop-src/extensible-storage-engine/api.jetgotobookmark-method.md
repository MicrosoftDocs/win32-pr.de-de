---
description: Weitere Informationen zur API. jetgodebookmark-Methode
title: API. jetgodebookmark-Methode
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530203"
---
# <a name="apijetgotobookmark-method"></a><span data-ttu-id="833ff-103">API. jetgodebookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="833ff-103">Api.JetGotoBookmark method</span></span>

<span data-ttu-id="833ff-104">Positioniert einen Cursor auf einen Index Eintrag für den Datensatz, der dem angegebenen Lesezeichen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="833ff-104">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="833ff-105">Das Lesezeichen kann mit jedem für eine Tabelle definierten Index verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="833ff-105">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="833ff-106">Das Lesezeichen für einen Datensatz kann mithilfe von [jetgetbookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetgetbookmark-method.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="833ff-106">The bookmark for a record can be retrieved using [JetGetBookmark(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetgetbookmark-method.md).</span></span>

<span data-ttu-id="833ff-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="833ff-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="833ff-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="833ff-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="833ff-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="833ff-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="833ff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="833ff-110">Parameters</span></span>

  - <span data-ttu-id="833ff-111">-sid</span><span class="sxs-lookup"><span data-stu-id="833ff-111">sesid</span></span>  
    <span data-ttu-id="833ff-112">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="833ff-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="833ff-113">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="833ff-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="833ff-114">TableID</span><span class="sxs-lookup"><span data-stu-id="833ff-114">tableid</span></span>  
    <span data-ttu-id="833ff-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="833ff-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="833ff-116">Der Cursor, der positioniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="833ff-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="833ff-117">Lesezeichen (bookmark)</span><span class="sxs-lookup"><span data-stu-id="833ff-117">bookmark</span></span>  
    <span data-ttu-id="833ff-118">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="833ff-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="833ff-119">Das Lesezeichen, das zum Positionieren des Cursors verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="833ff-119">The bookmark used to position the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="833ff-120">bookmarksize</span><span class="sxs-lookup"><span data-stu-id="833ff-120">bookmarkSize</span></span>  
    <span data-ttu-id="833ff-121">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="833ff-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="833ff-122">Die Größe des Lesezeichens.</span><span class="sxs-lookup"><span data-stu-id="833ff-122">The size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="833ff-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="833ff-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="833ff-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="833ff-124">Reference</span></span>

[<span data-ttu-id="833ff-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="833ff-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="833ff-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="833ff-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="833ff-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="833ff-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
