---
description: 'Weitere Informationen finden Sie hier: JET_LS Struktur'
title: JET_LS Struktur
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d32c1a6815cfa7552fed0d8f1a01376ae0eacaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217069"
---
# <a name="jet_ls-structure"></a><span data-ttu-id="f9fc0-103">JET_LS Struktur</span><span class="sxs-lookup"><span data-stu-id="f9fc0-103">JET_LS structure</span></span>

<span data-ttu-id="f9fc0-104">Lokaler Speicher für einen ESENT-handle.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-104">Local storage for an ESENT handle.</span></span> <span data-ttu-id="f9fc0-105">Wird von [jetgetls (JET_SESID, JET_TABLEID, JET_LS, lsgrbit)](./api.jetgetls-method.md) und [jetsetls (JET_SESID, JET_TABLEID, JET_LS, lsgrbit)](./api.jetsetls-method.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-105">Used by [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) and [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span>

<span data-ttu-id="f9fc0-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9fc0-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fc0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9fc0-108">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="f9fc0-109">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="f9fc0-109">Thread safety</span></span>

<span data-ttu-id="f9fc0-110">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f9fc0-111">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9fc0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9fc0-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9fc0-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="f9fc0-113">Reference</span></span>

[<span data-ttu-id="f9fc0-114">Mitglieder JET_LS</span><span class="sxs-lookup"><span data-stu-id="f9fc0-114">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="f9fc0-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9fc0-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
