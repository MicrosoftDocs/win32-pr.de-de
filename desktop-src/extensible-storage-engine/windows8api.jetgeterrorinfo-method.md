---
description: 'Weitere Informationen finden Sie hier: Windows8Api. jetgeterrorinfo-Methode'
title: Windows8Api. jetgeterrorinfo-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetGetErrorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo(Microsoft.Isam.Esent.Interop.JET_err,Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetgeterrorinfo(v=EXCHG.10)
ms:contentKeyID: 55104459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e6594c2d52769f5034bdf1c7253bee838edaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355554"
---
# <a name="windows8apijetgeterrorinfo-method"></a><span data-ttu-id="28a0b-103">Windows8Api. jetgeterrorinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="28a0b-103">Windows8Api.JetGetErrorInfo method</span></span>

<span data-ttu-id="28a0b-104">Ruft erweiterte Informationen zu einem Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="28a0b-104">Gets extended information about an error.</span></span>

<span data-ttu-id="28a0b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28a0b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="28a0b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="28a0b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28a0b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28a0b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetErrorInfo ( _
    error As JET_err, _
    <OutAttribute> ByRef errinfo As JET_ERRINFOBASIC _
)
'Usage
Dim error As JET_err
Dim errinfo As JET_ERRINFOBASICWindows8Api.JetGetErrorInfo(error, errinfo)
```

``` csharp
public static void JetGetErrorInfo(
    JET_err error,
    out JET_ERRINFOBASIC errinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="28a0b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28a0b-108">Parameters</span></span>

  - <span data-ttu-id="28a0b-109">error</span><span class="sxs-lookup"><span data-stu-id="28a0b-109">error</span></span>  
    <span data-ttu-id="28a0b-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="28a0b-110">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="28a0b-111">Der Fehlercode, über den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="28a0b-111">The error code about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="28a0b-112">errinfo</span><span class="sxs-lookup"><span data-stu-id="28a0b-112">errinfo</span></span>  
    <span data-ttu-id="28a0b-113">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span><span class="sxs-lookup"><span data-stu-id="28a0b-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span></span>  
    
    <span data-ttu-id="28a0b-114">Informationen zum angegebenen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="28a0b-114">Information about the specified error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="28a0b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a0b-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28a0b-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="28a0b-116">Reference</span></span>

[<span data-ttu-id="28a0b-117">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="28a0b-117">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="28a0b-118">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="28a0b-118">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="28a0b-119">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="28a0b-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
