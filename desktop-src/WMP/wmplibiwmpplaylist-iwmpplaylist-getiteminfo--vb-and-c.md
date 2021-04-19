---
title: Iwmpwiedergabe getiteminfo-Methode
description: Die getiteminfo-Methode gibt den Wert eines durch den Namen angegebenen Wiedergabelisten Attributs zurück.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366814"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="cda20-106">Iwmpwiedergabe:: getiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="cda20-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="cda20-107">Die **getiteminfo** -Methode gibt den Wert eines durch den Namen angegebenen Wiedergabelisten Attributs zurück.</span><span class="sxs-lookup"><span data-stu-id="cda20-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda20-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cda20-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="cda20-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cda20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda20-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cda20-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda20-111">Ein **System. String** -Wert, der der Name des Wiedergabelisten Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="cda20-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda20-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cda20-112">Return value</span></span>

<span data-ttu-id="cda20-113">Ein **System. String** -Wert, der den Wert des Wiedergabelisten Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="cda20-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda20-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cda20-114">Remarks</span></span>

<span data-ttu-id="cda20-115">Vor der Verwendung dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="cda20-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="cda20-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cda20-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="cda20-117">Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cda20-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda20-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cda20-118">Requirements</span></span>



| <span data-ttu-id="cda20-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cda20-119">Requirement</span></span> | <span data-ttu-id="cda20-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cda20-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda20-121">Version</span><span class="sxs-lookup"><span data-stu-id="cda20-121">Version</span></span><br/>   | <span data-ttu-id="cda20-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="cda20-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cda20-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cda20-123">Namespace</span></span><br/> | <span data-ttu-id="cda20-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cda20-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cda20-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="cda20-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cda20-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cda20-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda20-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cda20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda20-128">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="cda20-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cda20-129">**Iwmpwiedergabe. Einstellungs Verzeichnis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="cda20-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





