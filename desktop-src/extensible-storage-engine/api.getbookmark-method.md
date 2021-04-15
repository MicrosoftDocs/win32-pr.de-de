---
description: Weitere Informationen finden Sie in der API. GetBookmark-Methode.
title: API. GetBookmark-Methode
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524794"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="412cd-103">API. GetBookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="412cd-103">Api.GetBookmark method</span></span>

<span data-ttu-id="412cd-104">Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="412cd-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="412cd-105">Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von jetgobackbookmark wieder in denselben Datensatz zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="412cd-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="412cd-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="412cd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="412cd-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="412cd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="412cd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="412cd-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="412cd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="412cd-109">Parameters</span></span>

  - <span data-ttu-id="412cd-110">-sid</span><span class="sxs-lookup"><span data-stu-id="412cd-110">sesid</span></span>  
    <span data-ttu-id="412cd-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="412cd-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="412cd-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="412cd-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="412cd-113">TableID</span><span class="sxs-lookup"><span data-stu-id="412cd-113">tableid</span></span>  
    <span data-ttu-id="412cd-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="412cd-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="412cd-115">Der Cursor, von dem das Lesezeichen abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="412cd-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="412cd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="412cd-116">Return value</span></span>

<span data-ttu-id="412cd-117">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="412cd-117">Type: \[\]</span></span>  
<span data-ttu-id="412cd-118">Das Lesezeichen des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="412cd-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="412cd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="412cd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="412cd-120">Referenz</span><span class="sxs-lookup"><span data-stu-id="412cd-120">Reference</span></span>

[<span data-ttu-id="412cd-121">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="412cd-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="412cd-122">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="412cd-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="412cd-123">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="412cd-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
