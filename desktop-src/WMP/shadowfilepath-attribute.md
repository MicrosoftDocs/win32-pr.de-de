---
title: Shadowfilepath-Attribut
description: Das shadowfilepath-Attribut ist der voll qualifizierte Pfad zu einer Schattendatei.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Shadowfilepath-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366040"
---
# <a name="shadowfilepath-attribute"></a><span data-ttu-id="dcc4a-104">Shadowfilepath-Attribut</span><span class="sxs-lookup"><span data-stu-id="dcc4a-104">ShadowFilePath Attribute</span></span>

<span data-ttu-id="dcc4a-105">Das **shadowfilepath** -Attribut ist der voll qualifizierte Pfad zu einer Schattendatei.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-105">The **ShadowFilePath** attribute is the fully qualified path to a shadow file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="dcc4a-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="dcc4a-106">Applies To</span></span>

-   [<span data-ttu-id="dcc4a-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="dcc4a-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="dcc4a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcc4a-108">Remarks</span></span>

<span data-ttu-id="dcc4a-109">Eine *Schattendatei* wird als Teil einer Dateiformat Konvertierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-109">A *shadow file* is created as part of a file format conversion.</span></span> <span data-ttu-id="dcc4a-110">Dabei handelt es sich um die Kopie einer Datei, die der Player verwendet, wenn der Benutzerinhalte vom Computer mit einem Gerät synchronisiert, für das der Inhalt im ursprünglichen Dateiformat erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-110">It is the copy of a file that the Player uses when the user syncs content from the computer to a device that requires the content to be in the original file format.</span></span> <span data-ttu-id="dcc4a-111">Dieses Attribut wird für die konvertierte Datei festgelegt, um auf den Speicherort der Schattendatei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-111">This attribute is set for the converted file to point to the location of the shadow file.</span></span>

<span data-ttu-id="dcc4a-112">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc4a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcc4a-113">Requirements</span></span>



| <span data-ttu-id="dcc4a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcc4a-114">Requirement</span></span> | <span data-ttu-id="dcc4a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="dcc4a-115">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="dcc4a-116">Version</span><span class="sxs-lookup"><span data-stu-id="dcc4a-116">Version</span></span><br/> | <span data-ttu-id="dcc4a-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="dcc4a-117">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcc4a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcc4a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc4a-119">**Informationen zum Konvertierungsprozess**</span><span class="sxs-lookup"><span data-stu-id="dcc4a-119">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="dcc4a-120">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="dcc4a-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





