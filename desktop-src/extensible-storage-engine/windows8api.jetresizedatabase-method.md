---
description: 'Weitere Informationen finden Sie hier: Windows8Api. jetresizedatabase-Methode'
title: Windows8Api. jetresizedatabase-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetResizeDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetresizedatabase(v=EXCHG.10)
ms:contentKeyID: 55104462
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcca9a4006f8c8da1758a85d12d716b5ce1bba23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527713"
---
# <a name="windows8apijetresizedatabase-method"></a><span data-ttu-id="1d1eb-103">Windows8Api. jetresizedatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="1d1eb-103">Windows8Api.JetResizeDatabase method</span></span>

<span data-ttu-id="1d1eb-104">Ändert die Größe einer aktuell geöffneten Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-104">Resizes a currently open database.</span></span>

<span data-ttu-id="1d1eb-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="1d1eb-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1d1eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d1eb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResizeDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer, _
    grbit As ResizeDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As Integer
Dim grbit As ResizeDatabaseGrbitWindows8Api.JetResizeDatabase(sesid, dbid, _
    desiredPages, actualPages, grbit)
```

``` csharp
public static void JetResizeDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages,
    ResizeDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1d1eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d1eb-108">Parameters</span></span>

  - <span data-ttu-id="1d1eb-109">-sid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-109">sesid</span></span>  
    <span data-ttu-id="1d1eb-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1d1eb-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d1eb-112">dbid</span><span class="sxs-lookup"><span data-stu-id="1d1eb-112">dbid</span></span>  
    <span data-ttu-id="1d1eb-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1d1eb-114">Die Datenbank, die vergrößert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d1eb-115">desiredpages</span><span class="sxs-lookup"><span data-stu-id="1d1eb-115">desiredPages</span></span>  
    <span data-ttu-id="1d1eb-116">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1d1eb-117">Die gewünschte Größe der Datenbank in Seiten.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d1eb-118">actualpages</span><span class="sxs-lookup"><span data-stu-id="1d1eb-118">actualPages</span></span>  
    <span data-ttu-id="1d1eb-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1d1eb-120">Die Größe der Datenbank in Seiten nach dem-Befehl.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-120">The size of the database, in pages, after the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d1eb-121">grbit</span><span class="sxs-lookup"><span data-stu-id="1d1eb-121">grbit</span></span>  
    <span data-ttu-id="1d1eb-122">Typ: [Microsoft. ISAM. ESENT. Interop. Windows8. resizedatabasegrbit](./resizedatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1d1eb-122">Type: [Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1d1eb-123">Optionen für die Größenänderung.</span><span class="sxs-lookup"><span data-stu-id="1d1eb-123">Resize options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d1eb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d1eb-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1d1eb-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="1d1eb-125">Reference</span></span>

[<span data-ttu-id="1d1eb-126">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="1d1eb-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="1d1eb-127">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="1d1eb-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="1d1eb-128">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d1eb-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
