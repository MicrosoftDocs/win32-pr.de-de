---
description: Weitere Informationen finden Sie in der API. JetCreateInstance2-Methode.
title: API. JetCreateInstance2-Methode
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348365"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="76cd6-103">API. JetCreateInstance2-Methode</span><span class="sxs-lookup"><span data-stu-id="76cd6-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="76cd6-104">Weisen Sie eine neue Instanz der Datenbank-Engine für die Verwendung in einem einzelnen Prozess mit einem angegebenen anzeigen Amen zu.</span><span class="sxs-lookup"><span data-stu-id="76cd6-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="76cd6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76cd6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76cd6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="76cd6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76cd6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="76cd6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="76cd6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76cd6-108">Parameters</span></span>

  - <span data-ttu-id="76cd6-109">instance</span><span class="sxs-lookup"><span data-stu-id="76cd6-109">instance</span></span>  
    <span data-ttu-id="76cd6-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76cd6-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="76cd6-111">Gibt die neu erstellte Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="76cd6-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="76cd6-112">name</span><span class="sxs-lookup"><span data-stu-id="76cd6-112">name</span></span>  
    <span data-ttu-id="76cd6-113">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="76cd6-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="76cd6-114">Gibt einen eindeutigen Zeichen folgen Bezeichner für die Instanz an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="76cd6-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="76cd6-115">Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="76cd6-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="76cd6-116">displayName</span><span class="sxs-lookup"><span data-stu-id="76cd6-116">displayName</span></span>  
    <span data-ttu-id="76cd6-117">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="76cd6-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="76cd6-118">Ein Anzeige Name für die zu erstellende-Instanz.</span><span class="sxs-lookup"><span data-stu-id="76cd6-118">A display name for the instance to be created.</span></span> <span data-ttu-id="76cd6-119">Diese wird in EventLog-Einträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="76cd6-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="76cd6-120">grbit</span><span class="sxs-lookup"><span data-stu-id="76cd6-120">grbit</span></span>  
    <span data-ttu-id="76cd6-121">Typ: [Microsoft. ISAM. ESENT. Interop. kreateinstancegrbit](./createinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="76cd6-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="76cd6-122">Erstellungsoptionen,</span><span class="sxs-lookup"><span data-stu-id="76cd6-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="76cd6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76cd6-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76cd6-124">Referenz</span><span class="sxs-lookup"><span data-stu-id="76cd6-124">Reference</span></span>

[<span data-ttu-id="76cd6-125">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="76cd6-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="76cd6-126">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="76cd6-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="76cd6-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="76cd6-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
