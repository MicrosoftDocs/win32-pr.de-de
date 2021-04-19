---
title: Geräte-e/a-Steuerungs Codes
description: Geräte-e/a-Steuerungs Codes
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, e/a-Steuerungs Codes für Geräte
- Windows Media Player, Steuerungs Codes
- Windows Media-Device Manager
- Geräte-e/a-Steuerungs Codes
- Steuerungs Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339218"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="94613-108">Geräte-e/a-Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="94613-108">Device I/O Control Codes</span></span>

<span data-ttu-id="94613-109">Windows Media Player 10 oder höher definiert Windows Media Device Manager Geräte-e/a-Steuerungs Codes.</span><span class="sxs-lookup"><span data-stu-id="94613-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="94613-110">Die folgende Tabelle enthält die Steuercodes und ihre Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="94613-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="94613-111">E/a-Steuerungs Code</span><span class="sxs-lookup"><span data-stu-id="94613-111">I/O control code</span></span>                      | <span data-ttu-id="94613-112">Wert</span><span class="sxs-lookup"><span data-stu-id="94613-112">Value</span></span>      | <span data-ttu-id="94613-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94613-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94613-114">**Roundtrip für IOCTL- \_ WMP- \_ Metadaten \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94613-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="94613-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="94613-115">0x31504d57</span></span> | <span data-ttu-id="94613-116">Verwaltet die Übertragung von Informationen zu Änderungen, die an Metadatenwerte aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="94613-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="94613-117">Siehe [Geräte Erweiterungen für die beschleunigte metadatenübertragung](device-extensions-for-accelerated-metadata-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="94613-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="94613-118">**IOCTL- \_ WMP- \_ Gerät \_ kann \_ synchronisiert werden**</span><span class="sxs-lookup"><span data-stu-id="94613-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="94613-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="94613-119">0x32504d57</span></span> | <span data-ttu-id="94613-120">Gibt an, ob ein tragbares Gerät automatische Synchronisierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94613-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="94613-121">Windows Media Player 10 oder höher bietet keinen Eingabepuffer. Der Ausgabepuffer muss einen **DWORD** -Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="94613-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="94613-122">Der Wert 1 bedeutet, dass das Gerät die Synchronisierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94613-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="94613-123">Der Wert 0 bedeutet, dass das Gerät die automatische Synchronisierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94613-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="94613-124">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="94613-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94613-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94613-125">Remarks</span></span>

<span data-ttu-id="94613-126">Diese Steuerungs Codes sind in wmpdevices. h definiert.</span><span class="sxs-lookup"><span data-stu-id="94613-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="94613-127">Wenn das Gerät das **IOCTL- \_ WMP- \_ Gerät \_ \_ synchronisieren kann**, wird von Windows Media Player 10 oder höher davon ausgegangen, dass das Gerät die automatische Synchronisierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94613-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="94613-128">Beachten Sie, dass bei diesem Wert die automatische Synchronisierung nicht zulässig ist. es gibt jedoch zusätzliche Kriterien, die bestimmen, ob das Gerät die automatische Synchronisierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94613-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94613-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94613-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94613-130">**Geräte Erweiterungen für die beschleunigte metadatenübertragung**</span><span class="sxs-lookup"><span data-stu-id="94613-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="94613-131">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="94613-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 





