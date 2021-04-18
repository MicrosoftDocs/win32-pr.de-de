---
title: Settings. mediaaccessrights
description: Die mediaaccessrights-Eigenschaft ruft einen Wert ab, der die Rechte angibt, die derzeit für den Bibliotheks Zugriff gewährt werden.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaaccessrights-Fenster Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368499"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="89d51-104">Settings. mediaaccessrights</span><span class="sxs-lookup"><span data-stu-id="89d51-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="89d51-105">Die **mediaaccessrights** -Eigenschaft ruft einen Wert ab, der die Rechte angibt, die derzeit für den Bibliotheks Zugriff gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="89d51-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d51-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="89d51-106">Syntax</span></span>

<span data-ttu-id="89d51-107">Player. Settings. mediaaccessrights</span><span class="sxs-lookup"><span data-stu-id="89d51-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="89d51-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="89d51-108">Possible Values</span></span>

<span data-ttu-id="89d51-109">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="89d51-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="89d51-110">Wert</span><span class="sxs-lookup"><span data-stu-id="89d51-110">Value</span></span> | <span data-ttu-id="89d51-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89d51-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="89d51-112">none</span><span class="sxs-lookup"><span data-stu-id="89d51-112">none</span></span>  | <span data-ttu-id="89d51-113">Nur die aktuellen Element Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="89d51-113">Current item access rights only.</span></span> |
| <span data-ttu-id="89d51-114">Lesen</span><span class="sxs-lookup"><span data-stu-id="89d51-114">read</span></span>  | <span data-ttu-id="89d51-115">Nur Lese Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="89d51-115">Read access rights only.</span></span>         |
| <span data-ttu-id="89d51-116">Voll</span><span class="sxs-lookup"><span data-stu-id="89d51-116">full</span></span>  | <span data-ttu-id="89d51-117">Lese-/Schreibzugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="89d51-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="89d51-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d51-118">Remarks</span></span>

<span data-ttu-id="89d51-119">Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="89d51-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="89d51-120">Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="89d51-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="89d51-121">Zum Abrufen von Zugriffsrechten Ruft die Anwendung *Einstellungen* auf. **requestmediaaccessrights**, wobei ein Parameter übergeben wird, der die gewünschte Zugriffsrechte Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="89d51-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="89d51-122">**Windows Media Player 10 Mobile**: Diese Eigenschaft gibt immer **Full** zurück.</span><span class="sxs-lookup"><span data-stu-id="89d51-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d51-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89d51-123">Requirements</span></span>



| <span data-ttu-id="89d51-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89d51-124">Requirement</span></span> | <span data-ttu-id="89d51-125">Wert</span><span class="sxs-lookup"><span data-stu-id="89d51-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89d51-126">Version</span><span class="sxs-lookup"><span data-stu-id="89d51-126">Version</span></span><br/> | <span data-ttu-id="89d51-127">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89d51-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="89d51-128">DLL</span><span class="sxs-lookup"><span data-stu-id="89d51-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="89d51-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d51-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d51-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89d51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d51-131">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="89d51-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="89d51-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="89d51-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





