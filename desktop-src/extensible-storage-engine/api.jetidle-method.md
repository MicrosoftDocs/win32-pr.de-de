---
description: Weitere Informationen finden Sie in der API. jetidle-Methode.
title: API. jetidle-Methode
TOCTitle: 'JetIdle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIdle(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.IdleGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetidle(v=EXCHG.10)
ms:contentKeyID: 55100757
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIdle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e524a23d5e8fb20b1b6db1fb7e82fbb07bf3df0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960792"
---
# <a name="apijetidle-method"></a><span data-ttu-id="f3e45-103">API. jetidle-Methode</span><span class="sxs-lookup"><span data-stu-id="f3e45-103">Api.JetIdle method</span></span>

<span data-ttu-id="f3e45-104">Führt Cleanuptasks im Leerlauf aus oder überprüft den Versionsspeicher Status in ESE.</span><span class="sxs-lookup"><span data-stu-id="f3e45-104">Performs idle cleanup tasks or checks the version store status in ESE.</span></span>

<span data-ttu-id="f3e45-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3e45-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3e45-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f3e45-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e45-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3e45-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetIdle ( _
    sesid As JET_SESID, _
    grbit As IdleGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim grbit As IdleGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetIdle(sesid, _
    grbit)
```

``` csharp
public static JET_wrn JetIdle(
    JET_SESID sesid,
    IdleGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f3e45-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3e45-108">Parameters</span></span>

  - <span data-ttu-id="f3e45-109">-sid</span><span class="sxs-lookup"><span data-stu-id="f3e45-109">sesid</span></span>  
    <span data-ttu-id="f3e45-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f3e45-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f3e45-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f3e45-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f3e45-112">grbit</span><span class="sxs-lookup"><span data-stu-id="f3e45-112">grbit</span></span>  
    <span data-ttu-id="f3e45-113">Typ: [Microsoft. ISAM. ESENT. Interop. idlegrbit](./idlegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f3e45-113">Type: [Microsoft.Isam.Esent.Interop.IdleGrbit](./idlegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f3e45-114">Eine Kombination aus jetidlegrbit-Flags.</span><span class="sxs-lookup"><span data-stu-id="f3e45-114">A combination of JetIdleGrbit flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f3e45-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3e45-115">Return value</span></span>

<span data-ttu-id="f3e45-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f3e45-116">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="f3e45-117">Ein Fehlercode, wenn der Vorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f3e45-117">An error code if the operation fails.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3e45-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3e45-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3e45-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="f3e45-119">Reference</span></span>

[<span data-ttu-id="f3e45-120">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="f3e45-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f3e45-121">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="f3e45-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f3e45-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f3e45-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
