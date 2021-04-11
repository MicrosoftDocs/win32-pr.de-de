---
description: Weitere Informationen finden Sie in der API. jetsetls-Methode.
title: API. jetsetls-Methode
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217738"
---
# <a name="apijetsetls-method"></a><span data-ttu-id="44cbb-103">API. jetsetls-Methode</span><span class="sxs-lookup"><span data-stu-id="44cbb-103">Api.JetSetLS method</span></span>

<span data-ttu-id="44cbb-104">Ermöglicht der Anwendung, ein Kontext Handle, das als lokaler Speicher bezeichnet wird, einem Cursor oder der diesem Cursor zugeordneten Tabelle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="44cbb-104">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="44cbb-105">Dieses Kontext Handle kann von der Anwendung verwendet werden, um zusätzliche Daten zu speichern, die einem Cursor oder einer Tabelle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="44cbb-105">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="44cbb-106">Die Anwendung wird später mithilfe eines Lauf Zeit Rückrufs benachrichtigt, wenn das Kontext Handle freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="44cbb-106">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="44cbb-107">Dadurch ist es möglich, einem Cursor oder einer Tabelle dynamisch zugeordneten Zustand zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="44cbb-107">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="44cbb-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44cbb-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44cbb-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44cbb-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44cbb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="44cbb-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="44cbb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="44cbb-111">Parameters</span></span>

  - <span data-ttu-id="44cbb-112">-sid</span><span class="sxs-lookup"><span data-stu-id="44cbb-112">sesid</span></span>  
    <span data-ttu-id="44cbb-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44cbb-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="44cbb-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="44cbb-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="44cbb-115">TableID</span><span class="sxs-lookup"><span data-stu-id="44cbb-115">tableid</span></span>  
    <span data-ttu-id="44cbb-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44cbb-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="44cbb-117">Der zu verwendende Cursor.</span><span class="sxs-lookup"><span data-stu-id="44cbb-117">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="44cbb-118">ls</span><span class="sxs-lookup"><span data-stu-id="44cbb-118">ls</span></span>  
    <span data-ttu-id="44cbb-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44cbb-119">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="44cbb-120">Das Kontext Handle, das der Sitzung oder dem Cursor zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44cbb-120">The context handle to be associated with the session or cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="44cbb-121">grbit</span><span class="sxs-lookup"><span data-stu-id="44cbb-121">grbit</span></span>  
    <span data-ttu-id="44cbb-122">Typ: [Microsoft. ISAM. ESENT. Interop. lsgrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="44cbb-122">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="44cbb-123">Legen Sie Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="44cbb-123">Set options.</span></span>

## <a name="see-also"></a><span data-ttu-id="44cbb-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44cbb-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44cbb-125">Referenz</span><span class="sxs-lookup"><span data-stu-id="44cbb-125">Reference</span></span>

[<span data-ttu-id="44cbb-126">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="44cbb-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="44cbb-127">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="44cbb-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="44cbb-128">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="44cbb-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
