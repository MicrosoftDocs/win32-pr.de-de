---
description: 'Weitere Informationen finden Sie unter: API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, JET_INDEXLIST)'
title: API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, JET_INDEXLIST)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
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
ms.openlocfilehash: 5a39fba54463f7a55fd6a8521f5c905da4afb4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214936"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a><span data-ttu-id="948ab-103">API. jetgettableindexinfo-Methode (JET_SESID, JET_TABLEID, Zeichenfolge, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="948ab-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="948ab-104">**Hinweis: Diese API ist mittlerweile veraltet.**</span><span class="sxs-lookup"><span data-stu-id="948ab-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="948ab-105">Ruft Informationen zu Indizes in einer Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="948ab-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="948ab-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="948ab-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="948ab-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="948ab-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="948ab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="948ab-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="948ab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="948ab-109">Parameters</span></span>

  - <span data-ttu-id="948ab-110">-sid</span><span class="sxs-lookup"><span data-stu-id="948ab-110">sesid</span></span>  
    <span data-ttu-id="948ab-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="948ab-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="948ab-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="948ab-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="948ab-113">TableID</span><span class="sxs-lookup"><span data-stu-id="948ab-113">tableid</span></span>  
    <span data-ttu-id="948ab-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="948ab-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="948ab-115">Die Tabelle, für die Indexinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="948ab-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="948ab-116">Indexname</span><span class="sxs-lookup"><span data-stu-id="948ab-116">indexname</span></span>  
    <span data-ttu-id="948ab-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="948ab-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="948ab-118">Konvertiert die Zeichenfolgendarstellung einer Zahl in einem angegebenen Stil und einem kulturspezifischen Format in die entsprechende 32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="948ab-118">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="948ab-119">indexlist</span><span class="sxs-lookup"><span data-stu-id="948ab-119">indexlist</span></span>  
    <span data-ttu-id="948ab-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="948ab-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="948ab-121">Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="948ab-121">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="948ab-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="948ab-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="948ab-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="948ab-123">Reference</span></span>

[<span data-ttu-id="948ab-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="948ab-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="948ab-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="948ab-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="948ab-126">Jetgettableindexinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="948ab-126">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="948ab-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="948ab-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
