---
title: DRM_Flags
description: Die DRM- \_ Flags-Eigenschaft wird nur mit DRM-Inhalt der Version 1 verwendet, um die Rechte anzugeben, die in der lokalen Lizenz enthalten sein werden.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948429"
---
# <a name="drm_flags"></a><span data-ttu-id="70448-104">DRM- \_ Flags</span><span class="sxs-lookup"><span data-stu-id="70448-104">DRM\_Flags</span></span>

<span data-ttu-id="70448-105">Die **DRM- \_ Flags** -Eigenschaft wird nur mit DRM-Inhalt der Version 1 verwendet, um die Rechte anzugeben, die in der lokalen Lizenz enthalten sein werden.</span><span class="sxs-lookup"><span data-stu-id="70448-105">The **DRM\_Flags** property is used with DRM version 1 content only to specify the rights that will be contained in the local license.</span></span> <span data-ttu-id="70448-106">Rechte werden mit Werten angegeben, die durch den Enumerationstyp **WMT- \_ Rechte** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="70448-106">Rights are specified with values defined by the **WMT\_RIGHTS** enumeration type.</span></span> <span data-ttu-id="70448-107">Es können mehrere Werte ausgewählt werden, indem Sie mit dem bitweisen **or** -Operator kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="70448-107">More than one value can be selected by combining them with the bitwise **OR** operator.</span></span>

## <a name="global-constant"></a><span data-ttu-id="70448-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="70448-108">Global Constant</span></span>

<span data-ttu-id="70448-109">g \_ wszwmdrm- \_ Flags</span><span class="sxs-lookup"><span data-stu-id="70448-109">g\_wszWMDRM\_Flags</span></span>

## <a name="data-type"></a><span data-ttu-id="70448-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="70448-110">Data Type</span></span>

<span data-ttu-id="70448-111">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="70448-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="70448-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70448-112">Remarks</span></span>

<span data-ttu-id="70448-113">Beim Zugriff auf die **IWMHeaderInfo3** -Schnittstelle des Writer-Objekts können Sie diesen Wert hinzufügen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="70448-113">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="70448-114">In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="70448-114">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span> <span data-ttu-id="70448-115">Verwenden Sie [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , um diese Eigenschaft beim Erstellen von DRM-Version 1-Inhalten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="70448-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when creating DRM version 1 content.</span></span>

## <a name="see-also"></a><span data-ttu-id="70448-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70448-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70448-117">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="70448-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




