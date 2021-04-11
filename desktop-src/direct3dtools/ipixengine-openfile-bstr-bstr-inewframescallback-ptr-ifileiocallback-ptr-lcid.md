---
description: Öffnet ein Grafik Protokoll.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixengine:: OpenFile-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124339"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="6b823-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Ipixengine:: OpenFile-Methode</span><span class="sxs-lookup"><span data-stu-id="6b823-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="6b823-104">Öffnet ein Grafik Protokoll.</span><span class="sxs-lookup"><span data-stu-id="6b823-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b823-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b823-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="6b823-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b823-106">Parameters</span></span>

<span data-ttu-id="6b823-107">*Einfügen* </span><span class="sxs-lookup"><span data-stu-id="6b823-107">*FileName* </span></span>  
<span data-ttu-id="6b823-108">Eine com-Zeichenfolge, die den Namen des Grafik Protokolls enthält.</span><span class="sxs-lookup"><span data-stu-id="6b823-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="6b823-109">*registryboot* </span><span class="sxs-lookup"><span data-stu-id="6b823-109">*registryBoot* </span></span>  
<span data-ttu-id="6b823-110">Eine com-Zeichenfolge, die den Registrierungs Stamm enthält.</span><span class="sxs-lookup"><span data-stu-id="6b823-110">A COM string containing the registry root.</span></span> <span data-ttu-id="6b823-111">Die Engine sucht hier nach Dia und anderen Registrierungs Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="6b823-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="6b823-112">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="6b823-112">*callbacks* </span></span>  
<span data-ttu-id="6b823-113">Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass neue Frames analysiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6b823-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="6b823-114">*pfileiocallback* </span><span class="sxs-lookup"><span data-stu-id="6b823-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="6b823-115">Die Adresse einer Funktion, die verwendet wird, um den Host von Datei-e/a-Fehlern beim Parsen zu Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="6b823-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="6b823-116">*uilocale* </span><span class="sxs-lookup"><span data-stu-id="6b823-116">*uiLocale* </span></span>  
<span data-ttu-id="6b823-117">Die Gebiets Schema-ID, die zum Darstellen von Fehlermeldungen gemäß Gebiets Schema Einstellungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b823-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b823-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b823-118">Return value</span></span>

<span data-ttu-id="6b823-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b823-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b823-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b823-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b823-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b823-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6b823-122">Header</span><span class="sxs-lookup"><span data-stu-id="6b823-122">Header</span></span></p></td><td><span data-ttu-id="6b823-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6b823-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6b823-124"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b823-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6b823-125">**Ipixengine**</span><span class="sxs-lookup"><span data-stu-id="6b823-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
