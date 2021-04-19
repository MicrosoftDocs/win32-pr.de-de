---
title: Player. playerapplication
description: Die playerapplication-Eigenschaft ruft das playerapplication-Objekt ab, wenn ein Remotes Windows Media Player-Steuerelement ausgeführt wird.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player. playerapplication-Windows-Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369517"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="54d1f-104">Player. playerapplication</span><span class="sxs-lookup"><span data-stu-id="54d1f-104">Player.playerApplication</span></span>

<span data-ttu-id="54d1f-105">Die **playerapplication** -Eigenschaft ruft das **playerapplication** -Objekt ab, wenn ein Remotes Windows Media Player-Steuerelement ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54d1f-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d1f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54d1f-106">Syntax</span></span>

<span data-ttu-id="54d1f-107">**playerapplication**</span><span class="sxs-lookup"><span data-stu-id="54d1f-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="54d1f-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="54d1f-108">Possible Values</span></span>

<span data-ttu-id="54d1f-109">Diese Eigenschaft ist ein Schreib geschütztes **playerapplication** -Objekt oder der NULL-Wert.</span><span class="sxs-lookup"><span data-stu-id="54d1f-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54d1f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54d1f-110">Remarks</span></span>

<span data-ttu-id="54d1f-111">Diese Eigenschaft wird nur verwendet, wenn das Windows Media playercontrol-Element Remoting verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="54d1f-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="54d1f-112">Wenn der Wert NULL ist, wird das Windows Media playercontrol nicht in den Remote Modus eingebettet.</span><span class="sxs-lookup"><span data-stu-id="54d1f-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="54d1f-113">Auf diese Eigenschaft kann nur in C++-Code oder in Skriptcode in Skins über die globale Variable playerapplication zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="54d1f-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d1f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54d1f-114">Requirements</span></span>



| <span data-ttu-id="54d1f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54d1f-115">Requirement</span></span> | <span data-ttu-id="54d1f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="54d1f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54d1f-117">Version</span><span class="sxs-lookup"><span data-stu-id="54d1f-117">Version</span></span><br/> | <span data-ttu-id="54d1f-118">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="54d1f-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="54d1f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="54d1f-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="54d1f-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54d1f-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d1f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54d1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d1f-122">**Globale Attribute**</span><span class="sxs-lookup"><span data-stu-id="54d1f-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="54d1f-123">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="54d1f-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="54d1f-124">**Playerapplication-Objekt**</span><span class="sxs-lookup"><span data-stu-id="54d1f-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="54d1f-125">**Remoting des Windows Media Player-Steuerelements**</span><span class="sxs-lookup"><span data-stu-id="54d1f-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





