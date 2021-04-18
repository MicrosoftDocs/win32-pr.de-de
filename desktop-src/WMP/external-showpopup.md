---
title: Extern. ShowPopup-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. ShowPopup-Methode
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- Windows-Media Player der ShowPopup-Methode
- ShowPopup-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, ShowPopup-Methode
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364619"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="1fc85-107">Extern. ShowPopup-Methode</span><span class="sxs-lookup"><span data-stu-id="1fc85-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="1fc85-108">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="1fc85-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1fc85-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fc85-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1fc85-110">Die **ShowPopup** -Methode weist Windows Media Player an, eine Popup Webseite anzuzeigen. Das heißt, eine Webseite, die in einem separaten Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc85-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc85-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fc85-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="1fc85-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fc85-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc85-113">*Popupindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc85-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc85-114">**Number** (**Long**), der den Index der Popup Webseite angibt.</span><span class="sxs-lookup"><span data-stu-id="1fc85-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="1fc85-115">*Parameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fc85-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc85-116">Die **Zeichenfolge** , die von Windows Media Player an die URL der Webseite angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc85-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc85-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fc85-117">Return value</span></span>

<span data-ttu-id="1fc85-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1fc85-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc85-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fc85-119">Remarks</span></span>

<span data-ttu-id="1fc85-120">Der Popup Index wird nicht von Windows Media Player interpretiert.</span><span class="sxs-lookup"><span data-stu-id="1fc85-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="1fc85-121">Indizes, die Popup Webseiten identifizieren, werden vom Online Shop erstellt und sind nur im Online Store gemeint.</span><span class="sxs-lookup"><span data-stu-id="1fc85-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="1fc85-122">Die folgenden Schritte zeigen, wie Windows Media Player die Parameter der **ShowPopup** -Methode verwendet, um eine URL für das Popup Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1fc85-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="1fc85-123">Skript auf einer Discovery-Seite ruft **ShowPopup** auf und übergibt eine Ganzzahl in *popupindex* und eine Zeichenfolge in *Parametern*.</span><span class="sxs-lookup"><span data-stu-id="1fc85-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="1fc85-124">Windows Media Player übergibt den Index an [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , um die URL der Webseite abzurufen, die angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fc85-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="1fc85-125">Windows Media Player fügt *Parameter* als Abfrage Zeichenfolge an die URL an.</span><span class="sxs-lookup"><span data-stu-id="1fc85-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="1fc85-126">Wenn **getiteminfo** z. b. " https://www.Proseware.com/Pages/Popup1.htm " zurückgibt und *Parameter* gleich "dlgx = 800&dlgy = 400&Gruß = Hi", erstellt Windows Media Player die folgende URL:</span><span class="sxs-lookup"><span data-stu-id="1fc85-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="1fc85-127">Sie können *Parameter* verwenden, um die Größe des Popup Fensters anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1fc85-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="1fc85-128">Wenn Sie z. b. *Parameter* auf "dlgx = 800&dlgy = 400" festlegen, hat das Popup Fenster eine Größe von 800 Pixel um 400 Pixel.</span><span class="sxs-lookup"><span data-stu-id="1fc85-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc85-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fc85-129">Requirements</span></span>



| <span data-ttu-id="1fc85-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fc85-130">Requirement</span></span> | <span data-ttu-id="1fc85-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1fc85-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc85-132">Version</span><span class="sxs-lookup"><span data-stu-id="1fc85-132">Version</span></span><br/> | <span data-ttu-id="1fc85-133">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="1fc85-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="1fc85-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1fc85-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="1fc85-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc85-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc85-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fc85-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc85-137">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="1fc85-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





