---
description: 'Weitere Informationen finden Sie hier: JET_TABLEID Struktur'
title: JET_TABLEID Struktur
TOCTitle: JET_TABLEID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TABLEID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid(v=EXCHG.10)
ms:contentKeyID: 39516503
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72713007ace7fb93b3f01ec8e5fc25cbe127298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042729"
---
# <a name="jet_tableid-structure"></a><span data-ttu-id="9b652-103">JET_TABLEID Struktur</span><span class="sxs-lookup"><span data-stu-id="9b652-103">JET_TABLEID structure</span></span>

<span data-ttu-id="9b652-104">Ein JET_TABLEID das ein Handle für den Daten Bank Cursor enthält, der für einen aufzurufenden Jet-API-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b652-104">A JET_TABLEID contains a handle to the database cursor to use for a call to the JET API.</span></span> <span data-ttu-id="9b652-105">Ein Cursor kann nur mit der Sitzung verwendet werden, die zum Öffnen dieses Cursors verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9b652-105">A cursor can only be used with the session that was used to open that cursor.</span></span>

<span data-ttu-id="9b652-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b652-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b652-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9b652-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b652-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b652-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_TABLEID _
    Implements IEquatable(Of JET_TABLEID), IFormattable
'Usage
Dim instance As JET_TABLEID
```

``` csharp
public struct JET_TABLEID : IEquatable<JET_TABLEID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="9b652-109">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="9b652-109">Thread safety</span></span>

<span data-ttu-id="9b652-110">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="9b652-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9b652-111">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="9b652-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b652-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b652-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b652-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="9b652-113">Reference</span></span>

[<span data-ttu-id="9b652-114">Mitglieder JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9b652-114">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="9b652-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b652-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
