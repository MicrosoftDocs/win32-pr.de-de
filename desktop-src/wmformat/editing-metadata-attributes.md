---
title: Bearbeiten von Metadatenattributen
description: Bearbeiten von Metadatenattributen
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media-Format-SDK, Bearbeiten von Metadatenattributen
- Advanced Systems Format (ASF), Bearbeiten von Metadatenattributen
- ASF (Advanced Systems Format), Bearbeiten von Metadatenattributen
- Metadaten, Bearbeiten von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389921"
---
# <a name="editing-metadata-attributes"></a><span data-ttu-id="813ce-107">Bearbeiten von Metadatenattributen</span><span class="sxs-lookup"><span data-stu-id="813ce-107">Editing Metadata Attributes</span></span>

<span data-ttu-id="813ce-108">Das Bearbeiten von Metadatenattributen ähnelt dem Festlegen neuer Werte.</span><span class="sxs-lookup"><span data-stu-id="813ce-108">Editing metadata attributes is very similar to setting new ones.</span></span> <span data-ttu-id="813ce-109">Verwenden Sie anstelle von [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)das [**IWMHeaderInfo3:: modifyattribute-Attribut**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span><span class="sxs-lookup"><span data-stu-id="813ce-109">Instead of using [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span></span> <span data-ttu-id="813ce-110">**Modifyattribute** ist mit **AddAttribute** identisch, mit dem Unterschied, dass Sie keinen Attributnamen angeben und die Indexnummer anstelle einer Ausgabe ein Eingabeparameter ist.</span><span class="sxs-lookup"><span data-stu-id="813ce-110">**ModifyAttribute** is identical to **AddAttribute** except that you do not specify an attribute name, and the index number is an input parameter instead of an output.</span></span>

<span data-ttu-id="813ce-111">Mit der Stream-Nummer 0xFFFF können Sie ein Attribut angeben, das mit dem globalen Index geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="813ce-111">You can use stream number 0xFFFF to specify an attribute to modify using its global index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="813ce-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="813ce-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="813ce-113">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="813ce-113">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




