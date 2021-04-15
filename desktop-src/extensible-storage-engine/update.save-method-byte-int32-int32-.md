---
description: 'Weitere Informationen finden Sie unter: Update. Save-Methode (Byte, Int32, Int32)'
title: Update. Save-Methode (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485155"
---
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="b4947-103">Update. Save-Methode (Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="b4947-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="b4947-104">Aktualisieren Sie TableID.</span><span class="sxs-lookup"><span data-stu-id="b4947-104">Update the tableid.</span></span>

<span data-ttu-id="b4947-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4947-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4947-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4947-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4947-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4947-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="b4947-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4947-108">Parameters</span></span>

  - <span data-ttu-id="b4947-109">Lesezeichen (bookmark)</span><span class="sxs-lookup"><span data-stu-id="b4947-109">bookmark</span></span>  
    <span data-ttu-id="b4947-110">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="b4947-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="b4947-111">Gibt das Lesezeichen des aktualisierten Datensatzes zurück.</span><span class="sxs-lookup"><span data-stu-id="b4947-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="b4947-112">Diese kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b4947-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4947-113">bookmarksize</span><span class="sxs-lookup"><span data-stu-id="b4947-113">bookmarkSize</span></span>  
    <span data-ttu-id="b4947-114">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b4947-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b4947-115">Die Größe des Lesezeichen Puffers.</span><span class="sxs-lookup"><span data-stu-id="b4947-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4947-116">actualbookmarksize</span><span class="sxs-lookup"><span data-stu-id="b4947-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="b4947-117">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b4947-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b4947-118">Gibt die tatsächliche Größe des Lesezeichens zurück.</span><span class="sxs-lookup"><span data-stu-id="b4947-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4947-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4947-119">Remarks</span></span>

<span data-ttu-id="b4947-120">Speichern ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="b4947-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="b4947-121">Das Update wird zunächst durch Aufrufen eines Update Objekts und anschließendes Aufrufen von jetsetcolumn oder jetsetcolumns gestartet, um den Daten Satz Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b4947-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="b4947-122">Zum Schluss wird das Update aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b4947-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="b4947-123">Indizes werden nur durch Update oder nicht von jetsetcolumn oder jetsetcolumns aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4947-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4947-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4947-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4947-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="b4947-125">Reference</span></span>

[<span data-ttu-id="b4947-126">Update-Klasse</span><span class="sxs-lookup"><span data-stu-id="b4947-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="b4947-127">Mitglieder aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b4947-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="b4947-128">Überladung speichern</span><span class="sxs-lookup"><span data-stu-id="b4947-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="b4947-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="b4947-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
