---
title: IWMPSettings2 requestmediaaccessrights-Methode
description: Die requestmediaaccessrights-Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an. | IWMPSettings2 requestmediaaccessrights-Methode
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- requestmediaaccessrights-Methode, Windows Media Player
- requestmediaaccessrights-Methode, Windows Media Player, IWMPSettings2-Schnittstelle
- IWMPSettings2 Interface Windows Media Player, requestmediaaccessrights-Methode
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352998"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="ce068-107">IWMPSettings2:: requestmediaaccessrights-Methode</span><span class="sxs-lookup"><span data-stu-id="ce068-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="ce068-108">Die **requestmediaaccessrights** -Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="ce068-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce068-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce068-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="ce068-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce068-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce068-111">*bstraudesiredaccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce068-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce068-112">Ein **System. String** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="ce068-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="ce068-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ce068-113">Value</span></span> | <span data-ttu-id="ce068-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce068-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="ce068-115">none</span><span class="sxs-lookup"><span data-stu-id="ce068-115">none</span></span>  | <span data-ttu-id="ce068-116">Nur die aktuellen Element Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="ce068-116">Current item access rights only.</span></span> |
| <span data-ttu-id="ce068-117">Lesen</span><span class="sxs-lookup"><span data-stu-id="ce068-117">read</span></span>  | <span data-ttu-id="ce068-118">Nur Lese Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="ce068-118">Read access rights only.</span></span>         |
| <span data-ttu-id="ce068-119">Voll</span><span class="sxs-lookup"><span data-stu-id="ce068-119">full</span></span>  | <span data-ttu-id="ce068-120">Lese-/Schreibzugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="ce068-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce068-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce068-121">Return value</span></span>

<span data-ttu-id="ce068-122">Ein **System. boolescher** Wert, der angibt, ob die angeforderten Zugriffsrechte erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="ce068-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce068-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce068-123">Remarks</span></span>

<span data-ttu-id="ce068-124">Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ce068-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="ce068-125">Beim Aufrufen dieser Methode wird der Benutzer zu einem Dialogfeld aufgefordert, das die angegebene Berechtigungsebene anfordert.</span><span class="sxs-lookup"><span data-stu-id="ce068-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="ce068-126">Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="ce068-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="ce068-127">Die aktuelle Zugriffsrechte Ebene kann mithilfe von **IWMPSettings2. mediaaccessrights** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ce068-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="ce068-128">Anwendungen, die auf dem Computer des Benutzers ausgeführt werden, müssen diese Methode nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce068-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce068-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce068-129">Requirements</span></span>



| <span data-ttu-id="ce068-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce068-130">Requirement</span></span> | <span data-ttu-id="ce068-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ce068-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce068-132">Version</span><span class="sxs-lookup"><span data-stu-id="ce068-132">Version</span></span><br/>   | <span data-ttu-id="ce068-133">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ce068-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ce068-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce068-134">Namespace</span></span><br/> | <span data-ttu-id="ce068-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ce068-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ce068-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="ce068-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce068-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce068-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce068-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce068-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce068-139">**IWMPSettings2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ce068-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce068-140">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ce068-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





