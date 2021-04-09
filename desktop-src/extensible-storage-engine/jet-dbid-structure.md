---
description: 'Weitere Informationen finden Sie hier: JET_DBID Struktur'
title: JET_DBID Struktur
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865872"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="fdc7e-103">JET_DBID Struktur</span><span class="sxs-lookup"><span data-stu-id="fdc7e-103">JET_DBID structure</span></span>

<span data-ttu-id="fdc7e-104">Ein JET_DBID der das Handle für die Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="fdc7e-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="fdc7e-105">Ein Daten Bank Handle wird zum Verwalten des Schemas einer Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="fdc7e-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="fdc7e-106">Sie kann auch verwendet werden, um die Tabellen in der Datenbank zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="fdc7e-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="fdc7e-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fdc7e-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fdc7e-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fdc7e-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc7e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdc7e-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="fdc7e-110">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="fdc7e-110">Thread safety</span></span>

<span data-ttu-id="fdc7e-111">Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher.</span><span class="sxs-lookup"><span data-stu-id="fdc7e-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fdc7e-112">Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="fdc7e-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdc7e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdc7e-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fdc7e-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="fdc7e-114">Reference</span></span>

[<span data-ttu-id="fdc7e-115">Mitglieder JET_DBID</span><span class="sxs-lookup"><span data-stu-id="fdc7e-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="fdc7e-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fdc7e-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
