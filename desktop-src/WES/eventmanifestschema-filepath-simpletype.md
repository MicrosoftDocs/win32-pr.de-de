---
title: Dateipfad simple-Typ
description: Definiert eine Zeichenfolge, die einen voll qualifizierten Pfad zu einer Datei enthält.
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- Dateipfad für einfachen Ereignisprotokoll
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475609"
---
# <a name="filepath-simple-type"></a><span data-ttu-id="c7720-104">Dateipfad simple-Typ</span><span class="sxs-lookup"><span data-stu-id="c7720-104">filePath Simple Type</span></span>

<span data-ttu-id="c7720-105">Definiert eine Zeichenfolge, die einen voll qualifizierten Pfad zu einer Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="c7720-105">Defines a string that contains a fully qualified path to a file.</span></span> <span data-ttu-id="c7720-106">Der Pfad kann Umgebungsvariablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7720-106">The path may contain environment variables.</span></span>

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="c7720-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7720-107">Requirements</span></span>



| <span data-ttu-id="c7720-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7720-108">Requirement</span></span> | <span data-ttu-id="c7720-109">Wert</span><span class="sxs-lookup"><span data-stu-id="c7720-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c7720-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7720-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c7720-111">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7720-111">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c7720-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7720-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c7720-113">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7720-113">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





