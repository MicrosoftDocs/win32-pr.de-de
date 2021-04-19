---
description: Ruft das isearchitem-Objekt ab, wenn die URL eine tatsächliche shelldatenquelle darstellt (wird auch als Shellnamespace-Erweiterung bezeichnet).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'Isearchitem:: getParser Folder-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345020"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="b1575-103">Isearchitem:: getParser Folder-Methode</span><span class="sxs-lookup"><span data-stu-id="b1575-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="b1575-104">Ruft das [**isearchitem**](-search-isearchitem.md) -Objekt ab, wenn die URL eine tatsächliche shelldatenquelle darstellt (wird auch als Shellnamespace-Erweiterung bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="b1575-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1575-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1575-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="b1575-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1575-107">*IShellFolder* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b1575-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1575-108">Typ: **ppshellfolder \* \***</span><span class="sxs-lookup"><span data-stu-id="b1575-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="b1575-109">Enthält bei der Rückgabe die Adresse eines Zeigers auf den Ordner, der die aktuelle URL enthält.</span><span class="sxs-lookup"><span data-stu-id="b1575-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="b1575-110">Die [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) wird von allen Shell-Namespace-Ordner Objekten bereitgestellt, und die zugehörigen Methoden werden zum Verwalten von Ordnern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1575-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="b1575-111">*Lpitemittellist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b1575-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1575-112">Typ: \**ppidl \** _</span><span class="sxs-lookup"><span data-stu-id="b1575-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="b1575-113">Enthält bei der Rückgabe die Adresse eines Zeigers auf eine Element Bezeichner Liste (PIDL), die den übergeordneten Ordner identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b1575-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="b1575-114">Der Parameter "_LPITEMIDLIST \*" kann auf ein Objekt auf jeder Ebene unterhalb des übergeordneten Ordners in der Namespace Hierarchie verweisen. Daher kann es sich um einen mehrstufigen Zeiger auf eine **PIDL** relativ zum übergeordneten Ordner handeln.</span><span class="sxs-lookup"><span data-stu-id="b1575-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1575-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1575-115">Return value</span></span>

<span data-ttu-id="b1575-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b1575-116">Type: **HRESULT**</span></span>

<span data-ttu-id="b1575-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b1575-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b1575-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b1575-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1575-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1575-119">Remarks</span></span>

<span data-ttu-id="b1575-120">Die **isearchitem:: getParser Folder** -Methode wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1575-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b1575-121">Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die [**isearchitem**](-search-isearchitem.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md)und [**isearchprotocolui**](-search-isearchprotocolui.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)</span><span class="sxs-lookup"><span data-stu-id="b1575-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1575-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1575-122">Requirements</span></span>



| <span data-ttu-id="b1575-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1575-123">Requirement</span></span> | <span data-ttu-id="b1575-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b1575-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b1575-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1575-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b1575-126">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1575-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1575-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1575-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b1575-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1575-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b1575-129">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b1575-129">Redistributable</span></span><br/>          | <span data-ttu-id="b1575-130">Windows-Desktop Suche (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b1575-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b1575-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1575-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1575-132">**Isearchitem**</span><span class="sxs-lookup"><span data-stu-id="b1575-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
