---
description: 'Weitere Informationen finden Sie in den folgenden Artikeln: vistaapi. jetopumtemporarytable-Methode'
title: Vistaapi. jetopentemporarytable-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360155"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="fb1be-103">Vistaapi. jetopumtemporarytable-Methode</span><span class="sxs-lookup"><span data-stu-id="fb1be-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="fb1be-104">Erstellt eine temporäre Tabelle mit einem einzelnen Index.</span><span class="sxs-lookup"><span data-stu-id="fb1be-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="fb1be-105">Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb1be-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="fb1be-106">Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen.</span><span class="sxs-lookup"><span data-stu-id="fb1be-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="fb1be-107">Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="fb1be-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="fb1be-108">Siehe auch [jetopentemptable (JET_SESID, \[ \] , Int32, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="fb1be-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="fb1be-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb1be-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="fb1be-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fb1be-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1be-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb1be-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="fb1be-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb1be-112">Parameters</span></span>

  - <span data-ttu-id="fb1be-113">-sid</span><span class="sxs-lookup"><span data-stu-id="fb1be-113">sesid</span></span>  
    <span data-ttu-id="fb1be-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb1be-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fb1be-115">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="fb1be-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fb1be-116">temporarytable</span><span class="sxs-lookup"><span data-stu-id="fb1be-116">temporarytable</span></span>  
    <span data-ttu-id="fb1be-117">Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="fb1be-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="fb1be-118">Die Beschreibung der temporären Tabelle, die bei der Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb1be-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="fb1be-119">Nach einem erfolgreichen-Vorgang enthält die-Struktur das Handle für die temporären Tabellen-und Spalten Identifizierungen.</span><span class="sxs-lookup"><span data-stu-id="fb1be-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="fb1be-120">Verwenden Sie [jetclosetable (JET_SESID JET_TABLEID)](./api.jetclosetable-method.md) , um die temporäre Tabelle zu verwenden, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="fb1be-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb1be-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb1be-121">Remarks</span></span>

<span data-ttu-id="fb1be-122">Eingeführt in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fb1be-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="fb1be-123">Verwenden Sie für frühere Versionen von ESENT [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) .</span><span class="sxs-lookup"><span data-stu-id="fb1be-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb1be-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb1be-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb1be-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="fb1be-125">Reference</span></span>

[<span data-ttu-id="fb1be-126">Vistaapi-Klasse</span><span class="sxs-lookup"><span data-stu-id="fb1be-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="fb1be-127">Vistaapi-Member</span><span class="sxs-lookup"><span data-stu-id="fb1be-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="fb1be-128">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="fb1be-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
