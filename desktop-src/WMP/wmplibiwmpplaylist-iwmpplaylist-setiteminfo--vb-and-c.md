---
title: Iwmpwiedergabe-Methode
description: Mit der setiteminfo-Methode wird der Wert eines Attributs der aktuellen Wiedergabeliste festgelegt.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo", Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, Methode "stiteminfo"
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365687"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="51fce-106">Iwmpwiedergabe:: abtiteminfo-Methode</span><span class="sxs-lookup"><span data-stu-id="51fce-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="51fce-107">Mit der **setiteminfo** -Methode wird der Wert eines Attributs der aktuellen Wiedergabeliste festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51fce-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fce-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51fce-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="51fce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="51fce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51fce-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51fce-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51fce-111">Ein **System. String** -Wert, der der Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="51fce-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="51fce-112">*bstrauvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51fce-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51fce-113">Ein **System. String** -Wert, der der Attribut Wert ist.</span><span class="sxs-lookup"><span data-stu-id="51fce-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51fce-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51fce-114">Return value</span></span>

<span data-ttu-id="51fce-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="51fce-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fce-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51fce-116">Remarks</span></span>

<span data-ttu-id="51fce-117">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="51fce-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="51fce-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="51fce-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="51fce-119">Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51fce-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fce-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51fce-120">Requirements</span></span>



| <span data-ttu-id="51fce-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51fce-121">Requirement</span></span> | <span data-ttu-id="51fce-122">Wert</span><span class="sxs-lookup"><span data-stu-id="51fce-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fce-123">Version</span><span class="sxs-lookup"><span data-stu-id="51fce-123">Version</span></span><br/>   | <span data-ttu-id="51fce-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="51fce-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="51fce-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="51fce-125">Namespace</span></span><br/> | <span data-ttu-id="51fce-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="51fce-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="51fce-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="51fce-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="51fce-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="51fce-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fce-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51fce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fce-130">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51fce-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51fce-131">**Iwmpwiedergabe. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51fce-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51fce-132">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51fce-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51fce-133">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51fce-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





