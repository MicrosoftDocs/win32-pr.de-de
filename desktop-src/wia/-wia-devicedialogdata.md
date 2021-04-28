---
description: 'DEVICEDIALOGDATA-Struktur: Definiert die Daten, die zum Aufrufen eines Gerätedialogs erforderlich sind.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: DEVICEDIALOGDATA-Struktur (Wiadefd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: ad7b08f5396a7a6e9b1f74df3dd409303b2d548d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104268"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="7c32f-103">DEVICEDIALOGDATA-Struktur</span><span class="sxs-lookup"><span data-stu-id="7c32f-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="7c32f-104">Definiert die Daten, die zum Aufrufen eines Gerätedialogfelds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c32f-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c32f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c32f-105">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a><span data-ttu-id="7c32f-106">Member</span><span class="sxs-lookup"><span data-stu-id="7c32f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c32f-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="7c32f-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7c32f-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-109">Gibt die Größe dieser Struktur in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="7c32f-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7c32f-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="7c32f-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-111">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="7c32f-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-112">Gibt das Handle für das übergeordnete Fenster des Dialogfelds an.</span><span class="sxs-lookup"><span data-stu-id="7c32f-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="7c32f-113">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="7c32f-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-114">Typ: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span><span class="sxs-lookup"><span data-stu-id="7c32f-114">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-115">Zeigt auf eine [**IWiaItem-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) die das gültige Stammelement in der Anwendungselementstruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c32f-115">Points to an [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="7c32f-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="7c32f-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-117">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7c32f-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-118">Gibt einen Satz von Flags an, die den Vorgang des Dialogfelds steuern.</span><span class="sxs-lookup"><span data-stu-id="7c32f-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="7c32f-119">Kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7c32f-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="7c32f-120">Flag</span><span class="sxs-lookup"><span data-stu-id="7c32f-120">Flag</span></span>                                 | <span data-ttu-id="7c32f-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c32f-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-122">0</span><span class="sxs-lookup"><span data-stu-id="7c32f-122">0</span></span>                                    | <span data-ttu-id="7c32f-123">Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="7c32f-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="7c32f-124">\_WIA-GERÄTEDIALOGFELD \_ \_ – \_ EINZELNES IMAGE</span><span class="sxs-lookup"><span data-stu-id="7c32f-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="7c32f-125">Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld "Gerätebilderfassung".</span><span class="sxs-lookup"><span data-stu-id="7c32f-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="7c32f-126">DIALOGFELD \_ "WIA-GERÄT" \_ VERWENDEN DER ALLGEMEINEN \_ \_ \_ BENUTZEROBERFLÄCHE</span><span class="sxs-lookup"><span data-stu-id="7c32f-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="7c32f-127">Verwenden Sie die Systembenutzeroberfläche (falls verfügbar) anstelle der vom Anbieter bereitgestellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="7c32f-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="7c32f-128">Wenn die Systembenutzeroberfläche nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c32f-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="7c32f-129">Wenn keine der Benutzeroberflächen verfügbar ist, gibt die Funktion E \_ NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="7c32f-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7c32f-130">**lIntent**</span><span class="sxs-lookup"><span data-stu-id="7c32f-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-131">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="7c32f-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-132">Gibt an, welche Art von Daten das Bild darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="7c32f-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="7c32f-133">Eine Liste der Bildabsichtwerte finden Sie unter [**Bildabsichtkonstanten.**](-wia-imageintentconstants.md)</span><span class="sxs-lookup"><span data-stu-id="7c32f-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c32f-134">**lItemCount**</span><span class="sxs-lookup"><span data-stu-id="7c32f-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-135">Typ: **LONG**</span><span class="sxs-lookup"><span data-stu-id="7c32f-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-136">Empfängt die Anzahl der Elemente im Array, die durch den **ppWiaItem-Parameter** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7c32f-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7c32f-137">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="7c32f-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="7c32f-138">Typ: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="7c32f-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="7c32f-139">Empfängt die Adresse eines Arrays von Zeigern auf [**IWiaItem-Schnittstellen.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)</span><span class="sxs-lookup"><span data-stu-id="7c32f-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c32f-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c32f-140">Requirements</span></span>



| <span data-ttu-id="7c32f-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c32f-141">Requirement</span></span> | <span data-ttu-id="7c32f-142">Wert</span><span class="sxs-lookup"><span data-stu-id="7c32f-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7c32f-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c32f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7c32f-144">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c32f-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7c32f-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c32f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7c32f-146">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c32f-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7c32f-147">Header</span><span class="sxs-lookup"><span data-stu-id="7c32f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c32f-148"><dt>Wiadefd.h</dt></span><span class="sxs-lookup"><span data-stu-id="7c32f-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




