---
description: 'Weitere Informationen finden Sie unter: API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)'
title: API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100747
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a5e1f5e6908f33d211c5a32a3b9d34e55098101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352655"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-uint16-jet_idxinfo"></a><span data-ttu-id="f7ec6-103">API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="f7ec6-104">Ruft Informationen zu Indizes in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="f7ec6-105">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="f7ec6-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7ec6-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ec6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7ec6-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="f7ec6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7ec6-109">Parameters</span></span>

  - <span data-ttu-id="f7ec6-110">-sid</span><span class="sxs-lookup"><span data-stu-id="f7ec6-110">sesid</span></span>  
    <span data-ttu-id="f7ec6-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f7ec6-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7ec6-113">TableID</span><span class="sxs-lookup"><span data-stu-id="f7ec6-113">tableid</span></span>  
    <span data-ttu-id="f7ec6-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f7ec6-115">Die Tabelle, für die Indexinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7ec6-116">Indexname</span><span class="sxs-lookup"><span data-stu-id="f7ec6-116">indexname</span></span>  
    <span data-ttu-id="f7ec6-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f7ec6-118">Der Name des Index.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-118">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7ec6-119">result</span><span class="sxs-lookup"><span data-stu-id="f7ec6-119">result</span></span>  
    <span data-ttu-id="f7ec6-120">Typ: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-120">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="f7ec6-121">Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-121">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7ec6-122">infolevel</span><span class="sxs-lookup"><span data-stu-id="f7ec6-122">infoLevel</span></span>  
    <span data-ttu-id="f7ec6-123">Typ: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f7ec6-123">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="f7ec6-124">Der Typ der abzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="f7ec6-124">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7ec6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7ec6-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7ec6-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="f7ec6-126">Reference</span></span>

[<span data-ttu-id="f7ec6-127">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="f7ec6-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f7ec6-128">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="f7ec6-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f7ec6-129">Jetgettableindexinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="f7ec6-129">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="f7ec6-130">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f7ec6-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
