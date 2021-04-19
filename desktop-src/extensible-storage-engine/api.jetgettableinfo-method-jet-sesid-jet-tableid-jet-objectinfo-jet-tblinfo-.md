---
description: 'Weitere Informationen finden Sie unter: API. jetgettableinfo-Methode (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)'
title: API. jetgettableinfo-Methode (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100739
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbc95c771e2610ec23bdf503cdefa0399ee219ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355541"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_objectinfo-jet_tblinfo"></a><span data-ttu-id="701f4-103">API. jetgettableinfo-Methode (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="701f4-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</span></span>

<span data-ttu-id="701f4-104">Ruft verschiedene Informationen zu einer Tabelle in einer-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="701f4-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="701f4-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="701f4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="701f4-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="701f4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="701f4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="701f4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_OBJECTINFO, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_OBJECTINFO
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_OBJECTINFO result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="701f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="701f4-108">Parameters</span></span>

  - <span data-ttu-id="701f4-109">-sid</span><span class="sxs-lookup"><span data-stu-id="701f4-109">sesid</span></span>  
    <span data-ttu-id="701f4-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="701f4-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="701f4-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="701f4-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="701f4-112">TableID</span><span class="sxs-lookup"><span data-stu-id="701f4-112">tableid</span></span>  
    <span data-ttu-id="701f4-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="701f4-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="701f4-114">Die Tabelle, zu der Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="701f4-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="701f4-115">result</span><span class="sxs-lookup"><span data-stu-id="701f4-115">result</span></span>  
    <span data-ttu-id="701f4-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="701f4-116">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="701f4-117">Informationen wurden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="701f4-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="701f4-118">infolevel</span><span class="sxs-lookup"><span data-stu-id="701f4-118">infoLevel</span></span>  
    <span data-ttu-id="701f4-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="701f4-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="701f4-120">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="701f4-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="701f4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="701f4-121">Remarks</span></span>

<span data-ttu-id="701f4-122">Diese Überladung wird [standardmäßig](./jet-tblinfo-enumeration.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="701f4-122">This overload is used with [Default](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="701f4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="701f4-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="701f4-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="701f4-124">Reference</span></span>

[<span data-ttu-id="701f4-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="701f4-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="701f4-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="701f4-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="701f4-127">Jetgettableinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="701f4-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="701f4-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="701f4-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
