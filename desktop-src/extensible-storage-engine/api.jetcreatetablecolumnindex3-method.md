---
description: Weitere Informationen finden Sie in der API. JetCreateTableColumnIndex3-Methode.
title: API. JetCreateTableColumnIndex3-Methode
TOCTitle: 'JetCreateTableColumnIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetablecolumnindex3(v=EXCHG.10)
ms:contentKeyID: 55100678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a967db8f6a322ac29ba8a1e9352972ff1f4f4b76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484542"
---
# <a name="apijetcreatetablecolumnindex3-method"></a><span data-ttu-id="8049a-103">API. JetCreateTableColumnIndex3-Methode</span><span class="sxs-lookup"><span data-stu-id="8049a-103">Api.JetCreateTableColumnIndex3 method</span></span>

<span data-ttu-id="8049a-104">Erstellt eine Tabelle, fügt der Tabelle Spalten und Indizes hinzu.</span><span class="sxs-lookup"><span data-stu-id="8049a-104">Creates a table, adds columns, and indices on that table.</span></span>

<span data-ttu-id="8049a-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8049a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8049a-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8049a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8049a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8049a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex3 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEApi.JetCreateTableColumnIndex3(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex3(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="8049a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8049a-108">Parameters</span></span>

  - <span data-ttu-id="8049a-109">-sid</span><span class="sxs-lookup"><span data-stu-id="8049a-109">sesid</span></span>  
    <span data-ttu-id="8049a-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8049a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8049a-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="8049a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8049a-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8049a-112">dbid</span></span>  
    <span data-ttu-id="8049a-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8049a-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8049a-114">Die Datenbank, der die neue Tabelle hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8049a-114">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="8049a-115">tablecreate</span><span class="sxs-lookup"><span data-stu-id="8049a-115">tablecreate</span></span>  
    <span data-ttu-id="8049a-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="8049a-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="8049a-117">Objekt, das die zu erstellende Tabelle beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8049a-117">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="8049a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8049a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8049a-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="8049a-119">Reference</span></span>

[<span data-ttu-id="8049a-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="8049a-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8049a-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="8049a-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8049a-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="8049a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
