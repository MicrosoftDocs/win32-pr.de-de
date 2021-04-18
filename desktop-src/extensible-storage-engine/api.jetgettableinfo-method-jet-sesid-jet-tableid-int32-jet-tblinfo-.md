---
description: 'Weitere Informationen finden Sie unter: API. jetgettableinfo-Methode (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)'
title: API. jetgettableinfo-Methode (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3e276d118dcbb13fe7e67b33e8705581b16be67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352654"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-int32-jet_tblinfo"></a><span data-ttu-id="c3d16-103">API. jetgettableinfo-Methode (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="c3d16-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</span></span>

<span data-ttu-id="c3d16-104">Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="c3d16-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="c3d16-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3d16-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3d16-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3d16-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d16-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3d16-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As Integer
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="c3d16-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3d16-108">Parameters</span></span>

  - <span data-ttu-id="c3d16-109">-sid</span><span class="sxs-lookup"><span data-stu-id="c3d16-109">sesid</span></span>  
    <span data-ttu-id="c3d16-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3d16-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c3d16-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c3d16-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3d16-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c3d16-112">tableid</span></span>  
    <span data-ttu-id="c3d16-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3d16-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c3d16-114">Die Tabelle, zu der Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c3d16-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3d16-115">result</span><span class="sxs-lookup"><span data-stu-id="c3d16-115">result</span></span>  
    <span data-ttu-id="c3d16-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c3d16-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c3d16-117">Informationen wurden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c3d16-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3d16-118">infolevel</span><span class="sxs-lookup"><span data-stu-id="c3d16-118">infoLevel</span></span>  
    <span data-ttu-id="c3d16-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c3d16-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="c3d16-120">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="c3d16-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d16-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3d16-121">Remarks</span></span>

<span data-ttu-id="c3d16-122">Diese Überladung wird mit [spacebesitz](./jet-tblinfo-enumeration.md) und [SpaceAvailable](./jet-tblinfo-enumeration.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3d16-122">This overload is used with [SpaceOwned](./jet-tblinfo-enumeration.md) and [SpaceAvailable](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c3d16-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3d16-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3d16-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="c3d16-124">Reference</span></span>

[<span data-ttu-id="c3d16-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="c3d16-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c3d16-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="c3d16-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c3d16-127">Jetgettableinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="c3d16-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="c3d16-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c3d16-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
