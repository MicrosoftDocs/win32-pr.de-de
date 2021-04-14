---
description: Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Devicedialogdata-Struktur (wiadefd. h)
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
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529156"
---
# <a name="devicedialogdata-structure"></a><span data-ttu-id="9c843-103">Devicedialogdata-Struktur</span><span class="sxs-lookup"><span data-stu-id="9c843-103">DEVICEDIALOGDATA structure</span></span>

<span data-ttu-id="9c843-104">Definiert die Daten, die zum Abrufen eines Geräte Dialogfelds erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9c843-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c843-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c843-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="9c843-106">Member</span><span class="sxs-lookup"><span data-stu-id="9c843-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c843-107">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="9c843-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-108">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9c843-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9c843-109">Gibt die Größe dieser Struktur in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="9c843-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9c843-110">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="9c843-110">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-111">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="9c843-111">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="9c843-112">Gibt das Handle für das übergeordnete Fenster des Dialog Felds an.</span><span class="sxs-lookup"><span data-stu-id="9c843-112">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="9c843-113">**piwiaitemroot**</span><span class="sxs-lookup"><span data-stu-id="9c843-113">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-114">Typ: \**[**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _</span><span class="sxs-lookup"><span data-stu-id="9c843-114">Type: \**[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\** _</span></span>

</dd> <dd>

<span data-ttu-id="9c843-115">Verweist auf eine [_ *iwiaitem* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle, die das gültige Stamm Element in der Anwendungs Elementstruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="9c843-115">Points to an [_ *IWiaItem*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="9c843-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="9c843-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-117">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="9c843-117">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="9c843-118">Gibt einen Satz von Flags an, die den Vorgang des Dialog Felds steuern.</span><span class="sxs-lookup"><span data-stu-id="9c843-118">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="9c843-119">Kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="9c843-119">Can be set to any of the following values:</span></span>



| <span data-ttu-id="9c843-120">Flag</span><span class="sxs-lookup"><span data-stu-id="9c843-120">Flag</span></span>                                 | <span data-ttu-id="9c843-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9c843-121">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c843-122">0</span><span class="sxs-lookup"><span data-stu-id="9c843-122">0</span></span>                                    | <span data-ttu-id="9c843-123">Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="9c843-123">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="9c843-124">WIA- \_ Geräte \_ Dialogfeld, \_ einzelnes \_ Bild</span><span class="sxs-lookup"><span data-stu-id="9c843-124">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="9c843-125">Beschränken Sie die Bildauswahl auf ein einzelnes Bild im Dialogfeld Geräte Abbild Erfassung.</span><span class="sxs-lookup"><span data-stu-id="9c843-125">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="9c843-126">Dialog Feld "WIA- \_ Gerät" \_ \_ verwenden \_ allgemeine \_ Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="9c843-126">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="9c843-127">Verwenden Sie die Benutzeroberfläche des Systems, falls verfügbar, anstelle der vom Hersteller bereitgestellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="9c843-127">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="9c843-128">Wenn die Benutzeroberfläche des Systems nicht verfügbar ist, wird die Benutzeroberfläche des Anbieters verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c843-128">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="9c843-129">Wenn keine Benutzeroberfläche verfügbar ist, gibt die Funktion E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="9c843-129">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="9c843-130">**lintent**</span><span class="sxs-lookup"><span data-stu-id="9c843-130">**lIntent**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-131">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="9c843-131">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="9c843-132">Gibt an, welche Art von Daten das Image darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="9c843-132">Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="9c843-133">Eine Liste der Abbild Intent-Werte finden Sie unter [**Bild beabsichtigte Konstanten**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="9c843-133">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c843-134">**litemcount**</span><span class="sxs-lookup"><span data-stu-id="9c843-134">**lItemCount**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-135">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="9c843-135">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="9c843-136">Empfängt die Anzahl von Elementen im Array, die durch den **ppwiaitem** -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9c843-136">Receives the number of items in the array indicated by the **ppWiaItem** parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9c843-137">**ppwiaitem**</span><span class="sxs-lookup"><span data-stu-id="9c843-137">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="9c843-138">Typ: **[ **iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span><span class="sxs-lookup"><span data-stu-id="9c843-138">Type: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***</span></span>

</dd> <dd>

<span data-ttu-id="9c843-139">Empfängt die Adresse eines Arrays von Zeigern auf [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9c843-139">Receives the address of an array of pointers to [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c843-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c843-140">Requirements</span></span>



| <span data-ttu-id="9c843-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c843-141">Requirement</span></span> | <span data-ttu-id="9c843-142">Wert</span><span class="sxs-lookup"><span data-stu-id="9c843-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c843-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c843-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9c843-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c843-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9c843-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c843-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9c843-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c843-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c843-147">Header</span><span class="sxs-lookup"><span data-stu-id="9c843-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c843-148"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c843-148"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




