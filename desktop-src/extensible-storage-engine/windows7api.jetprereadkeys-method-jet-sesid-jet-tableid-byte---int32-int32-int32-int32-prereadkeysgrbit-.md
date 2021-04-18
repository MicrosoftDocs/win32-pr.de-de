---
description: 'Weitere Informationen finden Sie unter: Windows7Api. jetprereadkeys-Methode (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, prereadkeysgrbit)'
title: Windows7Api. jetprereadkeys-Methode (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, prereadkeysgrbit) (Microsoft. ISAM. ESENT. Interop. Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214891"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a><span data-ttu-id="6d7c6-103">Windows7Api. jetprereadkeys-Methode (JET_SESID, JET_TABLEID, Byte \[ \] \[ \] , Int32, Int32, Int32, Int32, prereadkeysgrbit)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-103">Windows7Api.JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte\[\]\[\], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)</span></span>

<span data-ttu-id="6d7c6-104">Wenn sich die Datensätze mit den angegebenen Schlüsseln nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-104">If the records with the specified keys are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="6d7c6-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="6d7c6-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d7c6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6d7c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d7c6-108">Parameters</span></span>

  - <span data-ttu-id="6d7c6-109">-sid</span><span class="sxs-lookup"><span data-stu-id="6d7c6-109">sesid</span></span>  
    <span data-ttu-id="6d7c6-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6d7c6-111">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-112">TableID</span><span class="sxs-lookup"><span data-stu-id="6d7c6-112">tableid</span></span>  
    <span data-ttu-id="6d7c6-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6d7c6-114">Die Tabelle, für die die prereads ausgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-115">keys</span><span class="sxs-lookup"><span data-stu-id="6d7c6-115">keys</span></span>  
    <span data-ttu-id="6d7c6-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="6d7c6-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="6d7c6-117">Die Schlüssel für die voraus Anzeige.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-117">The keys to preread.</span></span> <span data-ttu-id="6d7c6-118">Die Schlüssel müssen sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-118">The keys must be sorted.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-119">keylängen</span><span class="sxs-lookup"><span data-stu-id="6d7c6-119">keyLengths</span></span>  
    <span data-ttu-id="6d7c6-120">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="6d7c6-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="6d7c6-121">Die Längen der Schlüssel für die Voraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-121">The lengths of the keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-122">keyIndex</span><span class="sxs-lookup"><span data-stu-id="6d7c6-122">keyIndex</span></span>  
    <span data-ttu-id="6d7c6-123">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6d7c6-124">Der Index des ersten Schlüssels im Schlüssel Array, der gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-124">The index of the first key in the keys array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-125">keycount</span><span class="sxs-lookup"><span data-stu-id="6d7c6-125">keyCount</span></span>  
    <span data-ttu-id="6d7c6-126">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6d7c6-127">Die maximal zulässige Anzahl von Schlüsseln, die Voraussetzungen für die Anzeige sind.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-127">The maximum number of keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-128">keyspreread</span><span class="sxs-lookup"><span data-stu-id="6d7c6-128">keysPreread</span></span>  
    <span data-ttu-id="6d7c6-129">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6d7c6-130">Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorab registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-130">Returns the number of keys to actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="6d7c6-131">grbit</span><span class="sxs-lookup"><span data-stu-id="6d7c6-131">grbit</span></span>  
    <span data-ttu-id="6d7c6-132">Geben Sie Folgendes ein: [Microsoft. ISAM. ESENT. Interop. Windows7. prereadkeysgrbit](./prereadkeysgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6d7c6-132">Type: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6d7c6-133">Preread-Optionen.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-133">Preread options.</span></span> <span data-ttu-id="6d7c6-134">Wird verwendet, um die Richtung der Preread anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6d7c6-134">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d7c6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d7c6-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6d7c6-136">Referenz</span><span class="sxs-lookup"><span data-stu-id="6d7c6-136">Reference</span></span>

[<span data-ttu-id="6d7c6-137">Windows7Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="6d7c6-137">Windows7Api class</span></span>](./windows7api-class.md)

[<span data-ttu-id="6d7c6-138">Windows7Api-Member</span><span class="sxs-lookup"><span data-stu-id="6d7c6-138">Windows7Api members</span></span>](./windows7api-members.md)

[<span data-ttu-id="6d7c6-139">Jetprereadkeys-Überladung</span><span class="sxs-lookup"><span data-stu-id="6d7c6-139">JetPrereadKeys overload</span></span>](./windows7api.jetprereadkeys-method.md)

[<span data-ttu-id="6d7c6-140">Microsoft. ISAM. ESENT. Interop. Windows7-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d7c6-140">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
