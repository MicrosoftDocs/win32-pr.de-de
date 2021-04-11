---
description: 'Weitere Informationen finden Sie hier: legacyfile Ames-Enumeration'
title: Legacyfile Ames-Enumeration (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f3cade11450bcfbad13dcdd114dca6701c5369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959031"
---
# <a name="legacyfilenames-enumeration"></a><span data-ttu-id="0f347-103">Legacyfile Ames-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0f347-103">LegacyFileNames enumeration</span></span>

<span data-ttu-id="0f347-104">Optionen für "legacyfile"-Namen</span><span class="sxs-lookup"><span data-stu-id="0f347-104">Options for LegacyFileNames</span></span>

<span data-ttu-id="0f347-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f347-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0f347-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f347-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f347-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f347-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
```

## <a name="members"></a><span data-ttu-id="0f347-108">Member</span><span class="sxs-lookup"><span data-stu-id="0f347-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0f347-109">Membername</span><span class="sxs-lookup"><span data-stu-id="0f347-109">Member name</span></span></th>
<th><span data-ttu-id="0f347-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f347-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0f347-111">ESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="0f347-111">ESE98FileNames</span></span></td>
<td><span data-ttu-id="0f347-112">Wenn diese Option vorhanden ist, verwendet die Datenbank-Engine die folgenden Benennungs Konventionen für die zugehörigen Dateien: o Transaktionsprotokoll Dateien werden verwendet. Protokoll für ihre Dateierweiterung o-Prüf Punkt Dateien werden verwendet. CHK für die Dateierweiterung</span><span class="sxs-lookup"><span data-stu-id="0f347-112">When this option is present then the database engine will use the following naming conventions for its files: o Transaction Log files will use .LOG for their file extension o Checkpoint files will use .CHK for their file extension</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0f347-113">Eightdotthreesoftcompat</span><span class="sxs-lookup"><span data-stu-id="0f347-113">EightDotThreeSoftCompat</span></span></td>
<td><span data-ttu-id="0f347-114">Behalten Sie die 8,3-Benennungs Syntax so lange wie möglich bei.</span><span class="sxs-lookup"><span data-stu-id="0f347-114">Preserve the 8.3 naming syntax for as long as possible.</span></span> <span data-ttu-id="0f347-115">(Dies sollte nicht geändert werden, und es wird sichergestellt, dass keine Protokolldateien vorhanden sind.)</span><span class="sxs-lookup"><span data-stu-id="0f347-115">(this should not be changed, w/o ensuring there are no log files)</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0f347-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f347-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f347-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="0f347-117">Reference</span></span>

[<span data-ttu-id="0f347-118">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="0f347-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
