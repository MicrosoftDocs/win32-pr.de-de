---
title: Headerdisplaystyle-Enumeration
description: Wird von iresultviewer HeaderStyle verwendet, um den aktuellen Header Stil festzulegen oder zurückzugeben.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Headerdisplaystyle-Enumeration Legacy Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372373"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="a5358-104">Headerdisplaystyle-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a5358-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="a5358-105">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="a5358-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a5358-106">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="a5358-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a5358-107">Wird von [**iresultviewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) verwendet, um den aktuellen Header Stil festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a5358-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5358-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5358-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="a5358-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a5358-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a5358-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**Fullheader**</span><span class="sxs-lookup"><span data-stu-id="a5358-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a5358-111">Gibt die Verwendung von vollständigen Headern an oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a5358-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="a5358-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**Kompakter Ader**</span><span class="sxs-lookup"><span data-stu-id="a5358-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a5358-113">Gibt die Verwendung von kompakten Headern an oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a5358-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="a5358-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noheader**</span><span class="sxs-lookup"><span data-stu-id="a5358-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a5358-115">Gibt die Verwendung von No-Headern an oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="a5358-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5358-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5358-116">Requirements</span></span>



| <span data-ttu-id="a5358-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5358-117">Requirement</span></span> | <span data-ttu-id="a5358-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a5358-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5358-119">IDL</span><span class="sxs-lookup"><span data-stu-id="a5358-119">IDL</span></span><br/> | <dl> <span data-ttu-id="a5358-120"><dt>Wdsview. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5358-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





