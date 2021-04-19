---
description: Weitere Informationen finden Sie in der API. jetunregistercallback-Methode.
title: API. jetunregistercallback-Methode
TOCTitle: 'JetUnregisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetunregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100812
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db3f4a26803242f4ac9d3cb1de09805f9dd57012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355540"
---
# <a name="apijetunregistercallback-method"></a><span data-ttu-id="9a7b8-103">API. jetunregistercallback-Methode</span><span class="sxs-lookup"><span data-stu-id="9a7b8-103">Api.JetUnregisterCallback method</span></span>

<span data-ttu-id="9a7b8-104">Hiermit wird die Datenbank-Engine so konfiguriert, dass keine Benachrichtigungen mehr an die Anwendung gesendet werden, wie zuvor durch [jetregistercallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md)angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="9a7b8-104">Configures the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span></span>

<span data-ttu-id="9a7b8-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a7b8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9a7b8-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9a7b8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a7b8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUnregisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callbackId As JET_HANDLEApi.JetUnregisterCallback(sesid, _
    tableid, cbtyp, callbackId)
```

``` csharp
public static void JetUnregisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="9a7b8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a7b8-108">Parameters</span></span>

  - <span data-ttu-id="9a7b8-109">-sid</span><span class="sxs-lookup"><span data-stu-id="9a7b8-109">sesid</span></span>  
    <span data-ttu-id="9a7b8-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9a7b8-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9a7b8-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9a7b8-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a7b8-112">TableID</span><span class="sxs-lookup"><span data-stu-id="9a7b8-112">tableid</span></span>  
    <span data-ttu-id="9a7b8-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9a7b8-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9a7b8-114">Ein Cursor, der in der Tabelle geöffnet ist, bei der der Rückruf registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a7b8-114">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a7b8-115">cbyp</span><span class="sxs-lookup"><span data-stu-id="9a7b8-115">cbtyp</span></span>  
    <span data-ttu-id="9a7b8-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9a7b8-116">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="9a7b8-117">Die Rückruf Gründe, bei denen die Anwendung keine Benachrichtigungen mehr empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="9a7b8-117">The callback reasons for which the application no longer wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a7b8-118">callbackid</span><span class="sxs-lookup"><span data-stu-id="9a7b8-118">callbackId</span></span>  
    <span data-ttu-id="9a7b8-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9a7b8-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="9a7b8-120">Das Handle des registrierten Rückrufs, der von [jetregistercallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9a7b8-120">The handle of the registered callback that was returned by [JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a7b8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a7b8-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a7b8-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="9a7b8-122">Reference</span></span>

[<span data-ttu-id="9a7b8-123">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="9a7b8-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9a7b8-124">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="9a7b8-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9a7b8-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="9a7b8-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
