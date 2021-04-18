---
title: Settings. requestmediaaccessrights-Methode
description: Die requestmediaaccessrights-Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an. | Settings. requestmediaaccessrights-Methode
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- requestmediaaccessrights-Methode, Windows Media Player
- requestmediaaccessrights-Methode, Windows Media Player, Settings-Klasse
- Einstellungs Klasse Windows Media Player, requestmediaaccessrights-Methode
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351297"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="2a47b-107">Settings. requestmediaaccessrights-Methode</span><span class="sxs-lookup"><span data-stu-id="2a47b-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="2a47b-108">Die **requestmediaaccessrights** -Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="2a47b-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a47b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a47b-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="2a47b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a47b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a47b-111">*Zugriff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a47b-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a47b-112">**Zeichenfolge** , die die gewünschte Zugriffsrechte Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="2a47b-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="2a47b-113">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="2a47b-113">Contains one of the following values.</span></span>



| <span data-ttu-id="2a47b-114">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2a47b-114">String</span></span> | <span data-ttu-id="2a47b-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a47b-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="2a47b-116">none</span><span class="sxs-lookup"><span data-stu-id="2a47b-116">none</span></span>   | <span data-ttu-id="2a47b-117">Nur die aktuellen Element Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="2a47b-117">Current item access rights only.</span></span> |
| <span data-ttu-id="2a47b-118">Lesen</span><span class="sxs-lookup"><span data-stu-id="2a47b-118">read</span></span>   | <span data-ttu-id="2a47b-119">Nur Lese Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="2a47b-119">Read access rights only.</span></span>         |
| <span data-ttu-id="2a47b-120">Voll</span><span class="sxs-lookup"><span data-stu-id="2a47b-120">full</span></span>   | <span data-ttu-id="2a47b-121">Lese-/Schreibzugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="2a47b-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a47b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a47b-122">Return value</span></span>

<span data-ttu-id="2a47b-123">Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob die angeforderten Zugriffsrechte erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="2a47b-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a47b-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a47b-124">Remarks</span></span>

<span data-ttu-id="2a47b-125">Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="2a47b-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="2a47b-126">Beim Aufrufen dieser Methode wird der Benutzer zu einem Dialogfeld aufgefordert, das die angegebene Berechtigungsebene anfordert.</span><span class="sxs-lookup"><span data-stu-id="2a47b-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="2a47b-127">Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="2a47b-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="2a47b-128">Die aktuelle Zugriffsrechte Ebene kann mithilfe von *Einstellungen* abgerufen werden. **mediaaccessrights**.</span><span class="sxs-lookup"><span data-stu-id="2a47b-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="2a47b-129">**Windows Media Player 10 Mobile**: Diese Methode gibt immer " **true**" zurück.</span><span class="sxs-lookup"><span data-stu-id="2a47b-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a47b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a47b-130">Requirements</span></span>



| <span data-ttu-id="2a47b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a47b-131">Requirement</span></span> | <span data-ttu-id="2a47b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2a47b-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a47b-133">Version</span><span class="sxs-lookup"><span data-stu-id="2a47b-133">Version</span></span><br/> | <span data-ttu-id="2a47b-134">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2a47b-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2a47b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2a47b-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="2a47b-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a47b-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a47b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a47b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a47b-138">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="2a47b-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="2a47b-139">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="2a47b-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





