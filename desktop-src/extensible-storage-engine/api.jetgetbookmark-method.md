---
description: Weitere Informationen finden Sie in der API. jetgetbookmark-Methode.
title: API. jetgetbookmark-Methode
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eaac3c0c92fa9d6cfa1a5bca660791b81efe5ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342836"
---
# <a name="apijetgetbookmark-method"></a><span data-ttu-id="a6ddf-103">API. jetgetbookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="a6ddf-103">Api.JetGetBookmark method</span></span>

<span data-ttu-id="a6ddf-104">Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="a6ddf-105">Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von [jetgobackbookmark (JET_SESID, JET_TABLEID, \[ \] Int32)](./api.jetgotobookmark-method.md)wieder in denselben Datensatz zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-105">This bookmark can then be used to reposition that cursor back to the same record using [JetGotoBookmark(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetgotobookmark-method.md).</span></span> <span data-ttu-id="a6ddf-106">Das Lesezeichen ist nicht länger als [Lese](./systemparameters.bookmarkmost-property.md) Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-106">The bookmark will be no longer than [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes.</span></span> <span data-ttu-id="a6ddf-107">Siehe auch [GetBookmark (JET_SESID JET_TABLEID)](./api.getbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="a6ddf-107">Also see [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span></span>

<span data-ttu-id="a6ddf-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a6ddf-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ddf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6ddf-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="a6ddf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6ddf-111">Parameters</span></span>

  - <span data-ttu-id="a6ddf-112">-sid</span><span class="sxs-lookup"><span data-stu-id="a6ddf-112">sesid</span></span>  
    <span data-ttu-id="a6ddf-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a6ddf-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6ddf-115">TableID</span><span class="sxs-lookup"><span data-stu-id="a6ddf-115">tableid</span></span>  
    <span data-ttu-id="a6ddf-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a6ddf-117">Der Cursor, von dem das Lesezeichen abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-117">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6ddf-118">Lesezeichen (bookmark)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-118">bookmark</span></span>  
    <span data-ttu-id="a6ddf-119">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="a6ddf-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="a6ddf-120">Der Puffer, der das Lesezeichen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-120">Buffer to contain the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6ddf-121">bookmarksize</span><span class="sxs-lookup"><span data-stu-id="a6ddf-121">bookmarkSize</span></span>  
    <span data-ttu-id="a6ddf-122">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a6ddf-123">Größe des Lesezeichen Puffers.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-123">Size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6ddf-124">actualbookmarksize</span><span class="sxs-lookup"><span data-stu-id="a6ddf-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="a6ddf-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a6ddf-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a6ddf-126">Gibt die tatsächliche Größe des Lesezeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="a6ddf-126">Returns the actual size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6ddf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6ddf-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6ddf-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="a6ddf-128">Reference</span></span>

[<span data-ttu-id="a6ddf-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="a6ddf-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a6ddf-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="a6ddf-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a6ddf-131">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a6ddf-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
