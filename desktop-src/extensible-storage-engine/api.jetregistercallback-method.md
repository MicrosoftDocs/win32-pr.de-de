---
description: Weitere Informationen finden Sie in der API. jetregistercallback-Methode.
title: API. jetregistercallback-Methode
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369050"
---
# <a name="apijetregistercallback-method"></a><span data-ttu-id="0d01d-103">API. jetregistercallback-Methode</span><span class="sxs-lookup"><span data-stu-id="0d01d-103">Api.JetRegisterCallback method</span></span>

<span data-ttu-id="0d01d-104">Ermöglicht der Anwendung, die Datenbank-Engine so zu konfigurieren, dass Benachrichtigungen für bestimmte Ereignisse an die Anwendung ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d01d-104">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="0d01d-105">Diese Benachrichtigungen sind einer bestimmten Tabelle zugeordnet und bleiben nur wirksam, bis die Instanz, die die Tabelle enthält, mithilfe von [jetterm (JET_INSTANCE)](./api.jetterm-method.md)heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="0d01d-105">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm(JET_INSTANCE)](./api.jetterm-method.md).</span></span>

<span data-ttu-id="0d01d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d01d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d01d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0d01d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d01d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d01d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="0d01d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d01d-109">Parameters</span></span>

  - <span data-ttu-id="0d01d-110">-sid</span><span class="sxs-lookup"><span data-stu-id="0d01d-110">sesid</span></span>  
    <span data-ttu-id="0d01d-111">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0d01d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0d01d-112">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0d01d-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d01d-113">TableID</span><span class="sxs-lookup"><span data-stu-id="0d01d-113">tableid</span></span>  
    <span data-ttu-id="0d01d-114">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0d01d-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0d01d-115">Ein Cursor, der in der Tabelle geöffnet ist, bei der der Rückruf registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d01d-115">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d01d-116">cbyp</span><span class="sxs-lookup"><span data-stu-id="0d01d-116">cbtyp</span></span>  
    <span data-ttu-id="0d01d-117">Typ: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0d01d-117">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="0d01d-118">Die Rückruf Gründe, für die die Anwendung Benachrichtigungen empfangen möchte.</span><span class="sxs-lookup"><span data-stu-id="0d01d-118">The callback reasons for which the application wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d01d-119">Rückruf</span><span class="sxs-lookup"><span data-stu-id="0d01d-119">callback</span></span>  
    <span data-ttu-id="0d01d-120">Typ: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="0d01d-120">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="0d01d-121">Die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="0d01d-121">The callback function.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d01d-122">context</span><span class="sxs-lookup"><span data-stu-id="0d01d-122">context</span></span>  
    <span data-ttu-id="0d01d-123">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="0d01d-123">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="0d01d-124">Ein Kontext, der an den Rückruf übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d01d-124">A context that will be given to the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d01d-125">callbackid</span><span class="sxs-lookup"><span data-stu-id="0d01d-125">callbackId</span></span>  
    <span data-ttu-id="0d01d-126">Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0d01d-126">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="0d01d-127">Ein Handle, das später verwendet werden kann, um die Registrierung der angegebenen Rückruffunktion mit [jetunregistercallback (JET_SESID, JET_TABLEID JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md)abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="0d01d-127">A handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0d01d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d01d-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d01d-129">Referenz</span><span class="sxs-lookup"><span data-stu-id="0d01d-129">Reference</span></span>

[<span data-ttu-id="0d01d-130">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="0d01d-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0d01d-131">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="0d01d-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0d01d-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="0d01d-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
