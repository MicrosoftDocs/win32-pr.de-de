---
title: AutoBackup (channelloggingtype)-Element
description: Bestimmt, ob eine neue Protokolldatei erstellt wird, wenn die aktuelle Protokolldatei die maximale Größe erreicht.
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- AutoBackup-Element (EventLog)
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519084"
---
# <a name="autobackup-channelloggingtype-element"></a><span data-ttu-id="a44c4-104">AutoBackup (channelloggingtype)-Element</span><span class="sxs-lookup"><span data-stu-id="a44c4-104">autoBackup (ChannelLoggingType) Element</span></span>

<span data-ttu-id="a44c4-105">Bestimmt, ob eine neue Protokolldatei erstellt wird, wenn die aktuelle Protokolldatei die maximale Größe erreicht.</span><span class="sxs-lookup"><span data-stu-id="a44c4-105">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span>

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

<span data-ttu-id="a44c4-106">Das **AutoBackup** -Element wird durch den komplexen Typ [**channelloggingtype**](eventmanifestschema-channelloggingtype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="a44c4-106">The **autoBackup** element is defined by the [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a44c4-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a44c4-107">Requirements</span></span>



| <span data-ttu-id="a44c4-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a44c4-108">Requirement</span></span> | <span data-ttu-id="a44c4-109">Wert</span><span class="sxs-lookup"><span data-stu-id="a44c4-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a44c4-110">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a44c4-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a44c4-111">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a44c4-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a44c4-112">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a44c4-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a44c4-113">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a44c4-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a44c4-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a44c4-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a44c4-115">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="a44c4-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a44c4-116">**Protokollierung (channelType)**</span><span class="sxs-lookup"><span data-stu-id="a44c4-116">**logging (ChannelType)**</span></span>](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





