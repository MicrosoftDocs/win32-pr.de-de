---
title: IWMPSettings2 mediaaccessrights (Eigenschaft)
description: Die mediaaccessrights-Eigenschaft ruft einen Wert ab, der die Berechtigungen angibt, die derzeit für den Bibliotheks Zugriff erteilt werden
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Media Access Rights-Eigenschaften Fenster Media Player
- mediaaccessrights-Eigenschaft, Windows Media Player, IWMPSettings2-Schnittstelle
- IWMPSettings2 Interface Windows Media Player, mediaaccessrights-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354435"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="a442b-106">IWMPSettings2:: mediaaccessrights (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a442b-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="a442b-107">Die **mediaaccessrights** -Eigenschaft ruft einen Wert ab, der die Berechtigungen angibt, die derzeit für den Bibliotheks Zugriff erteilt werden</span><span class="sxs-lookup"><span data-stu-id="a442b-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="a442b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a442b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a442b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a442b-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="a442b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a442b-110">Property value</span></span>

<span data-ttu-id="a442b-111">Ein **System. String** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="a442b-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="a442b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a442b-112">Value</span></span> | <span data-ttu-id="a442b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a442b-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="a442b-114">none</span><span class="sxs-lookup"><span data-stu-id="a442b-114">none</span></span>  | <span data-ttu-id="a442b-115">Nur die aktuellen Element Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="a442b-115">Current item access rights only.</span></span> |
| <span data-ttu-id="a442b-116">Lesen</span><span class="sxs-lookup"><span data-stu-id="a442b-116">read</span></span>  | <span data-ttu-id="a442b-117">Nur Lese Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="a442b-117">Read access rights only.</span></span>         |
| <span data-ttu-id="a442b-118">Voll</span><span class="sxs-lookup"><span data-stu-id="a442b-118">full</span></span>  | <span data-ttu-id="a442b-119">Lese-/Schreibzugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="a442b-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="a442b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a442b-120">Remarks</span></span>

<span data-ttu-id="a442b-121">Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="a442b-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="a442b-122">Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="a442b-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="a442b-123">Zum Abrufen von Zugriffsrechten Ruft die Anwendung **IWMPSettings2. get \_ requestmediaaccessrights** auf und übergibt einen Parameter, der die gewünschte Zugriffsrechte Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="a442b-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="a442b-124">Anwendungen, die auf dem Computer des Benutzers ausgeführt werden, haben immer vollständige Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="a442b-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="a442b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a442b-125">Requirements</span></span>



| <span data-ttu-id="a442b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a442b-126">Requirement</span></span> | <span data-ttu-id="a442b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a442b-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a442b-128">Version</span><span class="sxs-lookup"><span data-stu-id="a442b-128">Version</span></span><br/>   | <span data-ttu-id="a442b-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a442b-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a442b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a442b-130">Namespace</span></span><br/> | <span data-ttu-id="a442b-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a442b-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a442b-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="a442b-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a442b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a442b-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a442b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a442b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a442b-135">**IWMPSettings2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a442b-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a442b-136">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a442b-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





