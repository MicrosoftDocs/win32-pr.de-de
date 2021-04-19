---
description: Weitere Informationen finden Sie in der Update. Save-Methode.
title: Update. Save-Methode
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389029"
---
# <a name="updatesave-method"></a><span data-ttu-id="d0ae3-103">Update. Save-Methode</span><span class="sxs-lookup"><span data-stu-id="d0ae3-103">Update.Save method</span></span>

<span data-ttu-id="d0ae3-104">Aktualisieren Sie TableID.</span><span class="sxs-lookup"><span data-stu-id="d0ae3-104">Update the tableid.</span></span>

<span data-ttu-id="d0ae3-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0ae3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0ae3-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0ae3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ae3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0ae3-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="d0ae3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0ae3-108">Remarks</span></span>

<span data-ttu-id="d0ae3-109">Speichern ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="d0ae3-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="d0ae3-110">Das Update wird zunächst durch Aufrufen eines Update Objekts und anschließendes Aufrufen von jetsetcolumn oder jetsetcolumns gestartet, um den Daten Satz Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d0ae3-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="d0ae3-111">Zum Schluss wird das Update aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d0ae3-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="d0ae3-112">Indizes werden nur durch Update oder nicht von jetsetcolumn oder jetsetcolumns aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d0ae3-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0ae3-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0ae3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0ae3-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="d0ae3-114">Reference</span></span>

[<span data-ttu-id="d0ae3-115">Update-Klasse</span><span class="sxs-lookup"><span data-stu-id="d0ae3-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="d0ae3-116">Mitglieder aktualisieren</span><span class="sxs-lookup"><span data-stu-id="d0ae3-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="d0ae3-117">Überladung speichern</span><span class="sxs-lookup"><span data-stu-id="d0ae3-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="d0ae3-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0ae3-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
