---
description: Ruft Informationen über den aktuellen Wiedergabe Computer ab.
MS-HAID: vspixengine.IPixEngine2\_GetPlaybackMachine\_BSTR\_BOOL\_ptr\_BSTR\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2:: getplaybackmachine-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D6C3C391-F039-4A5A-AA88-87A3624ECAD2
api_name:
- IPixEngine2.GetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c572d1a87fb537fd53a7f3e8f8048d1046980b20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344579"
---
# <a name="span-idvspixengineipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptrspanipixengine2getplaybackmachine-method"></a><span data-ttu-id="02f19-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2:: getplaybackmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="02f19-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2::GetPlaybackMachine method</span></span>

<span data-ttu-id="02f19-104">Ruft Informationen über den aktuellen Wiedergabe Computer ab.</span><span class="sxs-lookup"><span data-stu-id="02f19-104">Gets information about the current playback machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02f19-105">Syntax</span></span>


```C++
HRESULT GetPlaybackMachine(
   BSTR   logFile,
   BOOL * pUseAuthentication,
   BSTR * pMachine
);
```

## <a name="parameters"></a><span data-ttu-id="02f19-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02f19-106">Parameters</span></span>

<span data-ttu-id="02f19-107">*Protokolldatei* </span><span class="sxs-lookup"><span data-stu-id="02f19-107">*logFile* </span></span>  
<span data-ttu-id="02f19-108">Eine com-Zeichenfolge, die den Namen des zugeordneten Grafik Protokolls enthält.</span><span class="sxs-lookup"><span data-stu-id="02f19-108">A COM string containing the name of the associated graphics log.</span></span>

<span data-ttu-id="02f19-109">*pudie Authentifizierung* </span><span class="sxs-lookup"><span data-stu-id="02f19-109">*pUseAuthentication* </span></span>  
<span data-ttu-id="02f19-110">Bei Rückgabe true, wenn die Verbindung die Authentifizierung verwendet; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="02f19-110">On return, true if the connection uses authentication; otherwise, false.</span></span>

<span data-ttu-id="02f19-111">*pmachine* </span><span class="sxs-lookup"><span data-stu-id="02f19-111">*pMachine* </span></span>  
<span data-ttu-id="02f19-112">Bei der Rückgabe eine com-Zeichenfolge, die den Namen des Wiedergabe Computers enthält.</span><span class="sxs-lookup"><span data-stu-id="02f19-112">On return, a COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="02f19-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02f19-113">Return value</span></span>

<span data-ttu-id="02f19-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="02f19-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02f19-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="02f19-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f19-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02f19-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02f19-117">Header</span><span class="sxs-lookup"><span data-stu-id="02f19-117">Header</span></span></p></td><td><span data-ttu-id="02f19-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="02f19-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="02f19-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02f19-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="02f19-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="02f19-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
