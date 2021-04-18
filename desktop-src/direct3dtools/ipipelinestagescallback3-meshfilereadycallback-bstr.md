---
description: Ein Rückruf, der den Host der von der zugeordneten Anforderung geschriebenen Gitter Informationen benachrichtigt.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback3:: meshfilereadycallback-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344164"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="40ef6-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3:: meshfilereadycallback-Methode</span><span class="sxs-lookup"><span data-stu-id="40ef6-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="40ef6-104">Ein Rückruf, der den Host der von der zugeordneten Anforderung geschriebenen Gitter Informationen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="40ef6-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ef6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40ef6-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="40ef6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40ef6-106">Parameters</span></span>

<span data-ttu-id="40ef6-107">*meshfilename* </span><span class="sxs-lookup"><span data-stu-id="40ef6-107">*meshFilename* </span></span>  
<span data-ttu-id="40ef6-108">Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die Mesh-Daten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="40ef6-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="40ef6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40ef6-109">Return value</span></span>

<span data-ttu-id="40ef6-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="40ef6-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40ef6-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40ef6-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ef6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40ef6-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="40ef6-113">Header</span><span class="sxs-lookup"><span data-stu-id="40ef6-113">Header</span></span></p></td><td><span data-ttu-id="40ef6-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="40ef6-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="40ef6-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40ef6-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="40ef6-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="40ef6-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
