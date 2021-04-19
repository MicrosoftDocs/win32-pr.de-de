---
description: 'Weitere Informationen finden Sie unter: API. jetgetobjectinfo-Methode (JET_SESID, JET_DBID, JET_objtyp, Zeichenfolge, JET_OBJECTINFO)'
title: API. jetgetobjectinfo-Methode (JET_SESID, JET_DBID, JET_objtyp, Zeichenfolge, JET_OBJECTINFO)
TOCTitle: JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_objtyp,System.String,Microsoft.Isam.Esent.Interop.JET_OBJECTINFO@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetobjectinfo(v=EXCHG.10)
ms:contentKeyID: 55100733
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetObjectInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01311dcfbba226405a3c46c1be4c4553eac4eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348756"
---
# <a name="apijetgetobjectinfo-method-jet_sesid-jet_dbid-jet_objtyp-string-jet_objectinfo"></a><span data-ttu-id="79ea7-103">API. jetgetobjectinfo-Methode (JET_SESID, JET_DBID, JET_objtyp, Zeichenfolge, JET_OBJECTINFO)</span><span class="sxs-lookup"><span data-stu-id="79ea7-103">Api.JetGetObjectInfo method (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</span></span>

<span data-ttu-id="79ea7-104">Ruft Informationen zu Datenbankobjekten ab.</span><span class="sxs-lookup"><span data-stu-id="79ea7-104">Retrieves information about database objects.</span></span>

<span data-ttu-id="79ea7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79ea7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79ea7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="79ea7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79ea7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79ea7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetObjectInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    objtyp As JET_objtyp, _
    objectName As String, _
    <OutAttribute> ByRef objectinfo As JET_OBJECTINFO _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim objtyp As JET_objtyp
Dim objectName As String
Dim objectinfo As JET_OBJECTINFOApi.JetGetObjectInfo(sesid, dbid, _
    objtyp, objectName, objectinfo)
```

``` csharp
public static void JetGetObjectInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_objtyp objtyp,
    string objectName,
    out JET_OBJECTINFO objectinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="79ea7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="79ea7-108">Parameters</span></span>

  - <span data-ttu-id="79ea7-109">-sid</span><span class="sxs-lookup"><span data-stu-id="79ea7-109">sesid</span></span>  
    <span data-ttu-id="79ea7-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79ea7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="79ea7-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="79ea7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="79ea7-112">dbid</span><span class="sxs-lookup"><span data-stu-id="79ea7-112">dbid</span></span>  
    <span data-ttu-id="79ea7-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79ea7-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="79ea7-114">Die zu verwendende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="79ea7-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="79ea7-115">objyp</span><span class="sxs-lookup"><span data-stu-id="79ea7-115">objtyp</span></span>  
    <span data-ttu-id="79ea7-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="79ea7-116">Type: [Microsoft.Isam.Esent.Interop.JET_objtyp](./jet-objtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="79ea7-117">Der Typ des Objekts.</span><span class="sxs-lookup"><span data-stu-id="79ea7-117">The type of the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="79ea7-118">objectName</span><span class="sxs-lookup"><span data-stu-id="79ea7-118">objectName</span></span>  
    <span data-ttu-id="79ea7-119">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="79ea7-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="79ea7-120">Der Name des Objekts, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79ea7-120">The object name about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="79ea7-121">objectinfo</span><span class="sxs-lookup"><span data-stu-id="79ea7-121">objectinfo</span></span>  
    <span data-ttu-id="79ea7-122">Typ: [Microsoft.ISAM.ESENT.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="79ea7-122">Type: [Microsoft.Isam.Esent.Interop.JET_OBJECTINFO](./jet-objectinfo-class.md)</span></span>  
    
    <span data-ttu-id="79ea7-123">Wird mit Informationen zu den Objekten in der Datenbank ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="79ea7-123">Filled in with information about the objects in the database.</span></span>

## <a name="see-also"></a><span data-ttu-id="79ea7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79ea7-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79ea7-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="79ea7-125">Reference</span></span>

[<span data-ttu-id="79ea7-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="79ea7-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="79ea7-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="79ea7-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="79ea7-128">Jetgetobjectinfo-Überladung</span><span class="sxs-lookup"><span data-stu-id="79ea7-128">JetGetObjectInfo overload</span></span>](./api.jetgetobjectinfo-method.md)

[<span data-ttu-id="79ea7-129">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="79ea7-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
