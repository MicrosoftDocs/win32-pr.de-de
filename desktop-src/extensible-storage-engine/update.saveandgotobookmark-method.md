---
description: 'Weitere Informationen finden Sie hier: Update. saveandgodebookmark-Methode'
title: Update. saveandgodebookmark-Methode
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356512"
---
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="5de7f-103">Update. saveandgodebookmark-Methode</span><span class="sxs-lookup"><span data-stu-id="5de7f-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="5de7f-104">Aktualisieren Sie TableID, und positionieren Sie TableID für den geänderten Datensatz.</span><span class="sxs-lookup"><span data-stu-id="5de7f-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="5de7f-105">Dies kann hilfreich sein, wenn ein Datensatz eingefügt wird, da die TableID standardmäßig an der alten Position verbleibt.</span><span class="sxs-lookup"><span data-stu-id="5de7f-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="5de7f-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5de7f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5de7f-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5de7f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5de7f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5de7f-108">Syntax</span></span>

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a><span data-ttu-id="5de7f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5de7f-109">Remarks</span></span>

<span data-ttu-id="5de7f-110">Speichern ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="5de7f-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="5de7f-111">Das Update wird zunächst durch Aufrufen eines Update Objekts und anschließendes Aufrufen von jetsetcolumn oder jetsetcolumns gestartet, um den Daten Satz Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="5de7f-112">Zum Schluss wird das Update aufgerufen, um den Aktualisierungs Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5de7f-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="5de7f-113">Indizes werden nur durch Update oder nicht von jetsetcolumn oder jetsetcolumns aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5de7f-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="5de7f-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5de7f-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5de7f-115">Referenz</span><span class="sxs-lookup"><span data-stu-id="5de7f-115">Reference</span></span>

[<span data-ttu-id="5de7f-116">Update-Klasse</span><span class="sxs-lookup"><span data-stu-id="5de7f-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="5de7f-117">Mitglieder aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5de7f-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="5de7f-118">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5de7f-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
