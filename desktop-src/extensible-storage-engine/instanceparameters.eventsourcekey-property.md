---
description: 'Weitere Informationen finden Sie unter: instanceparameters. EventSourceKey (Eigenschaft)'
title: Instanceparameters. EventSourceKey (Eigenschaft)
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1dc80943095611737d0c9704bcc0e82ffee506f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959243"
---
# <a name="instanceparameterseventsourcekey-property"></a><span data-ttu-id="fdd32-103">Instanceparameters. EventSourceKey (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fdd32-103">InstanceParameters.EventSourceKey property</span></span>

<span data-ttu-id="fdd32-104">Ruft den Namen des Ereignis Protokolls ab, das von der Datenbank-Engine für seine Ereignisprotokoll Meldungen verwendet wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fdd32-104">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="fdd32-105">Standardmäßig werden alle Ereignisprotokoll Meldungen an das Anwendungs Ereignisprotokoll gesendet.</span><span class="sxs-lookup"><span data-stu-id="fdd32-105">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="fdd32-106">Wenn der Registrierungsschlüssel Name für ein anderes Ereignisprotokoll konfiguriert ist, werden stattdessen die Ereignisprotokoll Meldungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdd32-106">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<span data-ttu-id="fdd32-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fdd32-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fdd32-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fdd32-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd32-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdd32-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="fdd32-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fdd32-110">Property value</span></span>

<span data-ttu-id="fdd32-111">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="fdd32-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fdd32-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdd32-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fdd32-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="fdd32-113">Reference</span></span>

[<span data-ttu-id="fdd32-114">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="fdd32-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="fdd32-115">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="fdd32-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="fdd32-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="fdd32-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
