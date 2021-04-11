---
description: 'Weitere Informationen finden Sie hier: API. jetattachdatabase-Methode'
title: API. jetattachdatabase-Methode
TOCTitle: 'JetAttachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100652
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0447d4e6c5e8474c4d82340e35a23692096305bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128060"
---
# <a name="apijetattachdatabase-method"></a><span data-ttu-id="f05ce-103">API. jetattachdatabase-Methode</span><span class="sxs-lookup"><span data-stu-id="f05ce-103">Api.JetAttachDatabase method</span></span>

<span data-ttu-id="f05ce-104">Fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an.</span><span class="sxs-lookup"><span data-stu-id="f05ce-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="f05ce-105">Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopendatabase (JET_SESID, String, String, JET_DBID, opendatabasegrbit)](./api.jetopendatabase-method.md)geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f05ce-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="f05ce-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f05ce-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f05ce-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f05ce-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f05ce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f05ce-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase ( _
    sesid As JET_SESID, _
    database As String, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase(sesid, _
    database, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase(
    JET_SESID sesid,
    string database,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f05ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f05ce-109">Parameters</span></span>

  - <span data-ttu-id="f05ce-110">-sid</span><span class="sxs-lookup"><span data-stu-id="f05ce-110">sesid</span></span>  
    <span data-ttu-id="f05ce-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f05ce-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f05ce-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f05ce-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f05ce-113">database</span><span class="sxs-lookup"><span data-stu-id="f05ce-113">database</span></span>  
    <span data-ttu-id="f05ce-114">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f05ce-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f05ce-115">Die anzufügende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f05ce-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="f05ce-116">grbit</span><span class="sxs-lookup"><span data-stu-id="f05ce-116">grbit</span></span>  
    <span data-ttu-id="f05ce-117">Typ: [Microsoft. ISAM. ESENT. Interop. attachdatabasegrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f05ce-117">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f05ce-118">Optionen anfügen.</span><span class="sxs-lookup"><span data-stu-id="f05ce-118">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f05ce-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f05ce-119">Return value</span></span>

<span data-ttu-id="f05ce-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f05ce-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="f05ce-121">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="f05ce-121">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f05ce-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f05ce-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f05ce-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="f05ce-123">Reference</span></span>

[<span data-ttu-id="f05ce-124">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="f05ce-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f05ce-125">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="f05ce-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f05ce-126">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f05ce-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
