---
title: Previewdisplaystyle-Enumeration
description: Wird von iresultviewer PreviewStyle verwendet, um den derzeit verwendeten Anzeige Stil festzulegen oder zu bestimmen.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Previewdisplaystyle-Enumeration Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364461"
---
# <a name="previewdisplaystyle-enumeration"></a><span data-ttu-id="8eb9a-104">Previewdisplaystyle-Enumeration</span><span class="sxs-lookup"><span data-stu-id="8eb9a-104">PreviewDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="8eb9a-105">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8eb9a-106">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8eb9a-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8eb9a-107">Wird von [**iresultviewer verwendet::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) , um den derzeit verwendeten Anzeige Stil festzulegen oder zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-107">Used by [**IResultsViewer::PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md) to set or determine the display style currently being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb9a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eb9a-108">Syntax</span></span>


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="8eb9a-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8eb9a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8eb9a-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**</span><span class="sxs-lookup"><span data-stu-id="8eb9a-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="8eb9a-111">Gibt die AutoPreview an.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-111">Indicates AutoPreview.</span></span>

</dd> <dt>

<span data-ttu-id="8eb9a-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**Rechte Vorschau**</span><span class="sxs-lookup"><span data-stu-id="8eb9a-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span></span>
</dt> <dd>

<span data-ttu-id="8eb9a-113">Gibt rightpreview an.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-113">Indicates RightPreview.</span></span>

</dd> <dt>

<span data-ttu-id="8eb9a-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**Bottompreview**</span><span class="sxs-lookup"><span data-stu-id="8eb9a-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span></span>
</dt> <dd>

<span data-ttu-id="8eb9a-115">Gibt bottompreview an.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-115">Indicates BottomPreview.</span></span>

</dd> <dt>

<span data-ttu-id="8eb9a-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Nopreview**</span><span class="sxs-lookup"><span data-stu-id="8eb9a-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="8eb9a-117">Gibt nopreview an.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-117">Indicates NoPreview.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8eb9a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eb9a-118">Requirements</span></span>



| <span data-ttu-id="8eb9a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eb9a-119">Requirement</span></span> | <span data-ttu-id="8eb9a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8eb9a-120">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb9a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="8eb9a-121">IDL</span></span><br/> | <dl> <span data-ttu-id="8eb9a-122"><dt>Wdsview. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8eb9a-122"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





