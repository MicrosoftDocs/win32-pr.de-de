---
description: 'Weitere Informationen finden Sie hier: JET_RECSIZE Struktur'
title: JET_RECSIZE Struktur (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: JET_RECSIZE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize(v=EXCHG.10)
ms:contentKeyID: 39509765
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e741d91187a138d7b8d9a57d0c4e76f54979d99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346679"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="62a76-103">JET_RECSIZE Struktur</span><span class="sxs-lookup"><span data-stu-id="62a76-103">JET_RECSIZE structure</span></span>

<span data-ttu-id="62a76-104">Wird von [jetgetrecordsize (JET_SESID, JET_TABLEID, JET_RECSIZE, getrecordsizegrbit)](./vistaapi.jetgetrecordsize-method.md) verwendet, um Informationen über die Verwendungs Anforderungen eines Datensatzes im Benutzerdaten Bereich, die Anzahl der Mengen Spalten, die Anzahl der Werte und den mehr Aufwand für die ESENT-Daten Satzstruktur zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="62a76-104">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="62a76-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="62a76-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="62a76-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="62a76-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="62a76-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62a76-107">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_RECSIZE _
    Implements IEquatable(Of JET_RECSIZE)
'Usage
Dim instance As JET_RECSIZE
```

``` csharp
[SerializableAttribute]
public struct JET_RECSIZE : IEquatable<JET_RECSIZE>
```

## <a name="thread-safety"></a><span data-ttu-id="62a76-108">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="62a76-108">Thread safety</span></span>

<span data-ttu-id="62a76-109">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="62a76-109">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="62a76-110">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="62a76-110">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="62a76-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62a76-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="62a76-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="62a76-112">Reference</span></span>

[<span data-ttu-id="62a76-113">Mitglieder JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="62a76-113">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="62a76-114">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="62a76-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
