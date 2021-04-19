---
title: Iwmpwiedergabe. AttributeName (VB und C)
description: Die AttributeName-Eigenschaft (die get \_ attributeName-Methode in C \) Ruft den Namen eines durch einen Index angegebenen Wiedergabelisten Attributs ab.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- Iwmpwiedergabe. AttributeName (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364414"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="d6410-104">Iwmpwiedergabe. AttributeName (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="d6410-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="d6410-105">Die **attributeName** -Eigenschaft (die **get \_ attributeName** -Methode in c#) Ruft den Namen eines durch einen Index angegebenen Wiedergabelisten Attributs ab.</span><span class="sxs-lookup"><span data-stu-id="d6410-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="d6410-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6410-106">Parameters</span></span>

<span data-ttu-id="d6410-107">*Lindex*</span><span class="sxs-lookup"><span data-stu-id="d6410-107">*lIndex*</span></span>

<span data-ttu-id="d6410-108">Ein **System. Int32** -Wert, der den Index des Wiedergabelisten Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="d6410-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6410-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6410-109">Return Value</span></span>

<span data-ttu-id="d6410-110">Ein **System. String** -Wert, der der Name des Wiedergabelisten Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="d6410-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6410-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6410-111">Remarks</span></span>

<span data-ttu-id="d6410-112">**Iwmpwiedergabe. AttributeName** ist eine schreibgeschützte Eigenschaft in Visual Basic, die einen-Parameter annimmt, während in c# als **iwmpwiedergabe. get \_ attributeName** -Methode bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d6410-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="d6410-113">Die Anzahl der einer Wiedergabeliste zugeordneten Attribute wird von der **iwmpwiedergabe. AttributeCount** -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d6410-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="d6410-114">Der Name, der von dieser Eigenschaft zurückgegeben wird, kann an die Methoden " **ctiteminfo** " oder " **getiteminfo** " übergeben werden, um einen Wert für das benannte Attribut anzugeben oder abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d6410-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="d6410-115">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="d6410-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="d6410-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d6410-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d6410-117">Weitere Informationen zu Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d6410-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d6410-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6410-118">Examples</span></span>

<span data-ttu-id="d6410-119">Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d6410-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6410-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6410-120">Requirements</span></span>



| <span data-ttu-id="d6410-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6410-121">Requirement</span></span> | <span data-ttu-id="d6410-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d6410-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6410-123">Version</span><span class="sxs-lookup"><span data-stu-id="d6410-123">Version</span></span><br/>   | <span data-ttu-id="d6410-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="d6410-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d6410-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6410-125">Namespace</span></span><br/> | <span data-ttu-id="d6410-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d6410-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d6410-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="d6410-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d6410-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d6410-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6410-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6410-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6410-130">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d6410-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d6410-131">**Iwmpwiedergabe. AttributeCount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d6410-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d6410-132">**Iwmpwiedergabe. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d6410-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d6410-133">**Iwmpwiedergabe. Einstellungs Verzeichnis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d6410-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





