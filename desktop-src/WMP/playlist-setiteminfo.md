---
title: Wiedergabemethode.
description: Die Methode "stiteminfo" gibt den Wert eines Wiedergabelisten Attributs an.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Media Player der Methode "stiteminfo"
- Methode "stiteminfo", Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, Methode "stiteminfo"
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369302"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="63d4b-106">Wiedergabemethode.</span><span class="sxs-lookup"><span data-stu-id="63d4b-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="63d4b-107">Die Methode " **stiteminfo** " gibt den Wert eines Wiedergabelisten Attributs an.</span><span class="sxs-lookup"><span data-stu-id="63d4b-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d4b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="63d4b-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="63d4b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63d4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d4b-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63d4b-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63d4b-111">Eine **Zeichenfolge** mit dem Namen des festzulegenden Attributs.</span><span class="sxs-lookup"><span data-stu-id="63d4b-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="63d4b-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="63d4b-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="63d4b-113">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63d4b-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63d4b-114">**Zeichenfolge** , die den neuen Wert für das Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="63d4b-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d4b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63d4b-115">Return value</span></span>

<span data-ttu-id="63d4b-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="63d4b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63d4b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63d4b-117">Remarks</span></span>

<span data-ttu-id="63d4b-118">Eine besondere Verwendung der Methode "Methode" **ist das Sortieren** der Elemente in der Wiedergabeliste mithilfe des SortAttribute-Attributs.</span><span class="sxs-lookup"><span data-stu-id="63d4b-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="63d4b-119">Im folgenden JScript-Beispiel wird eine Wiedergabeliste nach den Werten des userlastplayedtime-Attributs sortiert.</span><span class="sxs-lookup"><span data-stu-id="63d4b-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="63d4b-120">Die Variablen Wiedergabeliste ist ein Verweis auf ein **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="63d4b-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="63d4b-121">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63d4b-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="63d4b-122">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="63d4b-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="63d4b-123">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="63d4b-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="63d4b-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63d4b-124">Examples</span></span>

<span data-ttu-id="63d4b-125">Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](playlist-attributecount.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="63d4b-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d4b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63d4b-126">Requirements</span></span>



| <span data-ttu-id="63d4b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63d4b-127">Requirement</span></span> | <span data-ttu-id="63d4b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="63d4b-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63d4b-129">Version</span><span class="sxs-lookup"><span data-stu-id="63d4b-129">Version</span></span><br/> | <span data-ttu-id="63d4b-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="63d4b-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="63d4b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="63d4b-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="63d4b-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63d4b-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63d4b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63d4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d4b-134">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="63d4b-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="63d4b-135">**Wiedergabeliste. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="63d4b-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="63d4b-136">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="63d4b-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="63d4b-137">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="63d4b-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





