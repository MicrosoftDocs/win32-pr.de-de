---
description: 'Weitere Informationen: Sitzungskonstruktor'
title: Sitzungskonstruktor
TOCTitle: 'Session constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.session(v=EXCHG.10)
ms:contentKeyID: 55107728
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Session
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73d19d5ae1ba422969cd5b11f5b59ceb2811a89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216285"
---
# <a name="session-constructor"></a><span data-ttu-id="2a8d9-103">Sitzungskonstruktor</span><span class="sxs-lookup"><span data-stu-id="2a8d9-103">Session constructor</span></span>

<span data-ttu-id="2a8d9-104">Initialisiert eine neue Instanz der Session-Klasse.</span><span class="sxs-lookup"><span data-stu-id="2a8d9-104">Initializes a new instance of the Session class.</span></span> <span data-ttu-id="2a8d9-105">Eine neue JET_SESSION wird von der angegebenen-Instanz zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2a8d9-105">A new JET_SESSION is allocated from the given instance.</span></span>

<span data-ttu-id="2a8d9-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a8d9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2a8d9-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2a8d9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a8d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a8d9-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New Session(instance)
```

``` csharp
public Session(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="2a8d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a8d9-109">Parameters</span></span>

  - <span data-ttu-id="2a8d9-110">instance</span><span class="sxs-lookup"><span data-stu-id="2a8d9-110">instance</span></span>  
    <span data-ttu-id="2a8d9-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2a8d9-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2a8d9-112">Die-Instanz, in der die Sitzung gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a8d9-112">The instance to start the session in.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a8d9-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a8d9-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a8d9-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="2a8d9-114">Reference</span></span>

[<span data-ttu-id="2a8d9-115">Sitzungsklasse</span><span class="sxs-lookup"><span data-stu-id="2a8d9-115">Session class</span></span>](./session-class.md)

[<span data-ttu-id="2a8d9-116">Sitzungs Mitglieder</span><span class="sxs-lookup"><span data-stu-id="2a8d9-116">Session members</span></span>](./session-members.md)

[<span data-ttu-id="2a8d9-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2a8d9-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
