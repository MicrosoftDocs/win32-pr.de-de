---
description: Speichert das Grafik Protokoll an der angegebenen Position.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixengine:: SaveFile-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522723"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="a41b8-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>Ipixengine:: SaveFile-Methode</span><span class="sxs-lookup"><span data-stu-id="a41b8-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="a41b8-104">Speichert das Grafik Protokoll an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="a41b8-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a41b8-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="a41b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a41b8-106">Parameters</span></span>

<span data-ttu-id="a41b8-107">*Einfügen* </span><span class="sxs-lookup"><span data-stu-id="a41b8-107">*FileName* </span></span>  
<span data-ttu-id="a41b8-108">Eine com-Zeichenfolge, die den Pfadnamen des gespeicherten Grafik Protokolls enthält.</span><span class="sxs-lookup"><span data-stu-id="a41b8-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="a41b8-109">*pfileiocallback* </span><span class="sxs-lookup"><span data-stu-id="a41b8-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="a41b8-110">Die Adresse eines funktons, mit dem der Host von Datei-e/a-Fehlern beim Speichern benachrichtigt wird</span><span class="sxs-lookup"><span data-stu-id="a41b8-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="a41b8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a41b8-111">Return value</span></span>

<span data-ttu-id="a41b8-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a41b8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a41b8-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a41b8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a41b8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a41b8-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a41b8-115">Header</span><span class="sxs-lookup"><span data-stu-id="a41b8-115">Header</span></span></p></td><td><span data-ttu-id="a41b8-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a41b8-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a41b8-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a41b8-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a41b8-118">**Ipixengine**</span><span class="sxs-lookup"><span data-stu-id="a41b8-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
