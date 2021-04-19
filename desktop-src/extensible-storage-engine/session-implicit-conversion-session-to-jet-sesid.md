---
description: 'Weitere Informationen finden Sie unter: implizite Sitzungs Konvertierung (Session to JET_SESID)'
title: Implizite Sitzungs Konvertierung (Sitzung zu JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356547"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a><span data-ttu-id="677d5-103">Implizite Sitzungs Konvertierung (Sitzung zu JET_SESID)</span><span class="sxs-lookup"><span data-stu-id="677d5-103">Session Implicit conversion (Session to JET_SESID)</span></span>

<span data-ttu-id="677d5-104">Impliziter Konvertierungs Operator von einer Sitzung zu einer JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="677d5-104">Implicit conversion operator from a Session to a JET_SESID.</span></span> <span data-ttu-id="677d5-105">Dadurch kann eine Sitzung mit APIs verwendet werden, die eine JET_SESID erwarten.</span><span class="sxs-lookup"><span data-stu-id="677d5-105">This allows a Session to be used with APIs which expect a JET_SESID.</span></span>

<span data-ttu-id="677d5-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="677d5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="677d5-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="677d5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="677d5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="677d5-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a><span data-ttu-id="677d5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="677d5-109">Parameters</span></span>

  - <span data-ttu-id="677d5-110">session</span><span class="sxs-lookup"><span data-stu-id="677d5-110">session</span></span>  
    <span data-ttu-id="677d5-111">Typ: [Microsoft. ISAM. ESENT. Interop. Session](./session-class.md)</span><span class="sxs-lookup"><span data-stu-id="677d5-111">Type: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)</span></span>  
    
    <span data-ttu-id="677d5-112">Die zu konvertierende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="677d5-112">The session to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="677d5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="677d5-113">Return value</span></span>

<span data-ttu-id="677d5-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="677d5-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
<span data-ttu-id="677d5-115">Der JET_SESID der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="677d5-115">The JET_SESID of the session.</span></span>  

## <a name="see-also"></a><span data-ttu-id="677d5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="677d5-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="677d5-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="677d5-117">Reference</span></span>

[<span data-ttu-id="677d5-118">Sitzungsklasse</span><span class="sxs-lookup"><span data-stu-id="677d5-118">Session class</span></span>](./session-class.md)

[<span data-ttu-id="677d5-119">Sitzungs Mitglieder</span><span class="sxs-lookup"><span data-stu-id="677d5-119">Session members</span></span>](./session-members.md)

[<span data-ttu-id="677d5-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="677d5-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
