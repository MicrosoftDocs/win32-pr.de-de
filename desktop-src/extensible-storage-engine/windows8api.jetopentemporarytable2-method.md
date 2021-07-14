---
description: 'Weitere Informationen finden Sie unter: Windows8Api.JetOpenTemporaryTable2-Methode'
title: Windows8Api.JetOpenTemporaryTable2-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- DllExport
api_location:
- Microsoft.Isam.Esent.Interop.dll
- esent.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb01792608ec542918f4bd8ff6ec06ef27091bb1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691729"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="25b64-103">Windows8Api.JetOpenTemporaryTable2-Methode</span><span class="sxs-lookup"><span data-stu-id="25b64-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="25b64-104">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="25b64-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="25b64-105">Eine temporäre Tabelle speichert und ruft Datensätze genau wie eine normale Tabelle ab, die mit JetCreateTableColumnIndex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="25b64-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="25b64-106">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="25b64-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="25b64-107">Sie können auch verwendet werden, um sehr schnell zu sortieren und doppelte Entfernungen für Datensatzgruppen durchzuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="25b64-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="25b64-108">Siehe auch [JetOpenTempTable(JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] ) ,](./api.jetopentemptable-method.md)"Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="25b64-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="25b64-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="25b64-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="25b64-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25b64-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="25b64-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25b64-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25b64-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="25b64-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="25b64-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="25b64-113">Parameters</span></span>

  - <span data-ttu-id="25b64-114">sesid</span><span class="sxs-lookup"><span data-stu-id="25b64-114">sesid</span></span>  
    <span data-ttu-id="25b64-115">Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25b64-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25b64-116">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="25b64-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="25b64-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="25b64-117">temporarytable</span></span>  
    <span data-ttu-id="25b64-118">Typ: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="25b64-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="25b64-119">Beschreibung der temporären Tabelle, die bei der Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25b64-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="25b64-120">Nach einem erfolgreichen Aufruf enthält die -Struktur das Handle für die temporäre Tabelle und die Spaltenidentifikationen.</span><span class="sxs-lookup"><span data-stu-id="25b64-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="25b64-121">Verwenden [Sie JetCloseTable(JET_SESID, JET_TABLEID),](./api.jetclosetable-method.md) um die temporäre Tabelle frei zu geben, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="25b64-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="25b64-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25b64-122">Remarks</span></span>

<span data-ttu-id="25b64-123">Verwenden [Sie JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) für frühere Versionen von Esent.</span><span class="sxs-lookup"><span data-stu-id="25b64-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="25b64-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25b64-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25b64-125">Verweis</span><span class="sxs-lookup"><span data-stu-id="25b64-125">Reference</span></span>

[<span data-ttu-id="25b64-126">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="25b64-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="25b64-127">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="25b64-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="25b64-128">Microsoft.Isam.Esent.Interop.Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="25b64-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
