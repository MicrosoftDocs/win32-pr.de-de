---
title: Viewcontents-Enumeration
description: Wird von iresultsviewer-Inhalten verwendet, um anzugeben, wie der aktuelle Abfrage Rückgabe Satz angezeigt wird, oder legt ihn fest.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- Viewcontents-Enumeration Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364552"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="c3105-104">Viewcontents-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c3105-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="c3105-105">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="c3105-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c3105-106">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c3105-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c3105-107">Wird von [**iresultsviewer:: Contents**](-search-2x-iresultsviewer-contents.md) verwendet, um anzugeben, wie die aktuelle Abfrage Rückgabe Menge angezeigt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c3105-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3105-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3105-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="c3105-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c3105-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c3105-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**Ergebnis angezeigt**</span><span class="sxs-lookup"><span data-stu-id="c3105-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="c3105-111">Gibt den Typ des Inhalts an, der in der Ergebnis Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c3105-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="c3105-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**Shellviewanzeige**</span><span class="sxs-lookup"><span data-stu-id="c3105-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="c3105-113">Gibt an, welcher Typ von Inhalt, der in der Ergebnis Ansicht angezeigt wird, derzeit auf die shellansicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3105-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="c3105-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**Webbrowseranzeige**</span><span class="sxs-lookup"><span data-stu-id="c3105-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="c3105-115">Gibt an, welcher Typ von Inhalt, der in der Ergebnis Ansicht angezeigt wird, derzeit auf die Browseransicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3105-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3105-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3105-116">Requirements</span></span>



| <span data-ttu-id="c3105-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3105-117">Requirement</span></span> | <span data-ttu-id="c3105-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c3105-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3105-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c3105-119">IDL</span></span><br/> | <dl> <span data-ttu-id="c3105-120"><dt>Wdsview. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3105-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





