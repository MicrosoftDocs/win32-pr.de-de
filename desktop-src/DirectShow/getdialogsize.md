---
description: Die getdialogsize-Funktion Ruft die Größe eines Ressourcen Dialogfelds ab.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Getdialogsize-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371455"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="58d21-103">Getdialogsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="58d21-103">GetDialogSize function</span></span>

<span data-ttu-id="58d21-104">Die **getdialogsize** -Funktion Ruft die Größe eines Ressourcen Dialogfelds ab.</span><span class="sxs-lookup"><span data-stu-id="58d21-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58d21-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="58d21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58d21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d21-107">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="58d21-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="58d21-108">Der Ressourcen Bezeichner des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="58d21-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="58d21-109">*pdlgproc*</span><span class="sxs-lookup"><span data-stu-id="58d21-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="58d21-110">Zeiger auf die Dialogfeld Prozedur.</span><span class="sxs-lookup"><span data-stu-id="58d21-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="58d21-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58d21-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58d21-112">Der Wert, der in der "WM \_ InitDialog"-Meldung übergeben wird, die nach der Erstellung an das temporäre Dialogfeld gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="58d21-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="58d21-113">*pResult*</span><span class="sxs-lookup"><span data-stu-id="58d21-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="58d21-114">Ein Zeiger auf eine **Größen** Struktur, die die Abmessungen des Dialog Felds in Bildschirm Pixel empfängt.</span><span class="sxs-lookup"><span data-stu-id="58d21-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58d21-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58d21-115">Return value</span></span>

<span data-ttu-id="58d21-116">Gibt **true** zurück, wenn die Dialogfeld Ressource gefunden wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="58d21-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="58d21-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58d21-117">Remarks</span></span>

<span data-ttu-id="58d21-118">Eigenschaften Seiten können diese Funktion verwenden, um die tatsächliche Anzeige Größe zurückzugeben, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="58d21-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="58d21-119">Die meisten Eigenschaften Seiten sind Dialogfelder und verfügen daher über Dialogfeld Vorlagen, die in Ressourcen Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="58d21-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="58d21-120">Vorlagen verwenden Dialogfeld Einheiten, die nicht direkt auf Bildschirm Pixel zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="58d21-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="58d21-121">Allerdings muss die [**GetPageInfo**](cbasepropertypage-getpageinfo.md) -Funktion einer Eigenschaften Seite die tatsächliche Anzeige Größe in Pixel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="58d21-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="58d21-122">Die Eigenschaften Seite kann aufrufen `GetDialogSize` , um die Anzeige Größe zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="58d21-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="58d21-123">Diese Funktion erstellt eine temporäre Instanz des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="58d21-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="58d21-124">Um zu vermeiden, dass das Dialogfeld auf dem Bildschirm angezeigt wird, sollte die Dialogfeld Vorlage in der Ressourcen Datei nicht über eine Eigenschaft vom Typ "WS Visible" verfügen \_ .</span><span class="sxs-lookup"><span data-stu-id="58d21-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d21-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58d21-125">Requirements</span></span>



| <span data-ttu-id="58d21-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58d21-126">Requirement</span></span> | <span data-ttu-id="58d21-127">Wert</span><span class="sxs-lookup"><span data-stu-id="58d21-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d21-128">Header</span><span class="sxs-lookup"><span data-stu-id="58d21-128">Header</span></span><br/>  | <dl> <span data-ttu-id="58d21-129"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58d21-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="58d21-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58d21-130">Library</span></span><br/> | <dl> <span data-ttu-id="58d21-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="58d21-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d21-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58d21-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d21-133">Hilfsfunktionen für Eigenschaften Seiten</span><span class="sxs-lookup"><span data-stu-id="58d21-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




