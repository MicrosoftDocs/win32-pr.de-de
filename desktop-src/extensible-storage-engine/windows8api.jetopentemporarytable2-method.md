---
description: 'Weitere Informationen über: Windows8Api. JetOpenTemporaryTable2-Methode'
title: Windows8Api. JetOpenTemporaryTable2-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
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
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360113"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="97c88-103">Windows8Api. JetOpenTemporaryTable2-Methode</span><span class="sxs-lookup"><span data-stu-id="97c88-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="97c88-104">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="97c88-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="97c88-105">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="97c88-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="97c88-106">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="97c88-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="97c88-107">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="97c88-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="97c88-108">Siehe auch [jetopentemptable (JET_SESID, \[ \] , Int32, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="97c88-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="97c88-109">[Jetopumtemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="97c88-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="97c88-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97c88-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="97c88-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97c88-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97c88-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="97c88-112">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="97c88-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="97c88-113">Parameters</span></span>

  - <span data-ttu-id="97c88-114">-sid</span><span class="sxs-lookup"><span data-stu-id="97c88-114">sesid</span></span>  
    <span data-ttu-id="97c88-115">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="97c88-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="97c88-116">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="97c88-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="97c88-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="97c88-117">temporarytable</span></span>  
    <span data-ttu-id="97c88-118">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="97c88-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="97c88-119">Die Beschreibung der temporären Tabelle, die bei der Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="97c88-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="97c88-120">Nach einem erfolgreichen-Vorgang enthält die-Struktur das Handle für die temporären Tabellen-und Spalten Identifizierungen.</span><span class="sxs-lookup"><span data-stu-id="97c88-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="97c88-121">Verwenden Sie [jetclosetable (JET_SESID JET_TABLEID)](./api.jetclosetable-method.md) , um die temporäre Tabelle zu verwenden, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="97c88-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c88-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97c88-122">Remarks</span></span>

<span data-ttu-id="97c88-123">Verwenden Sie [jetopentemporarytable (JET_SESID JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) für frühere Versionen von ESENT.</span><span class="sxs-lookup"><span data-stu-id="97c88-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="97c88-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97c88-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97c88-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="97c88-125">Reference</span></span>

[<span data-ttu-id="97c88-126">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="97c88-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="97c88-127">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="97c88-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="97c88-128">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="97c88-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
