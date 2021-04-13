---
title: Wmkreatestreamforurl-Funktion
description: Die wmkreatestreamforurl-Funktion wird von der Anwendung implementiert, um ein COM-IStream-Objekt für eine bestimmte URL zu erstellen.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Wmkreatestreamforurl-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389210"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="4eef5-104">Wmkreatestreamforurl-Funktion</span><span class="sxs-lookup"><span data-stu-id="4eef5-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="4eef5-105">Die **wmkreatestreamforurl** -Funktion wird von der Anwendung implementiert, um ein com- **IStream** -Objekt für eine bestimmte URL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4eef5-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eef5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4eef5-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="4eef5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4eef5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eef5-108">*pwszurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4eef5-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eef5-109">Zeiger auf eine breit Zeichen-Zeichenfolge, die die URL enthält.</span><span class="sxs-lookup"><span data-stu-id="4eef5-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="4eef5-110">*pfcorrectsource* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4eef5-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4eef5-111">Zeiger auf ein Flag, "true" verhindert, dass das SDK andere Quell-Plug-Ins für diese URL ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="4eef5-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="4eef5-112">*PPStream* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4eef5-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4eef5-113">Zeiger auf einen Zeiger auf das **IStream** -Objekt, das von der-Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4eef5-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eef5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4eef5-114">Return value</span></span>

<span data-ttu-id="4eef5-115">Wenn die Funktion erfolgreich ausgeführt wird, muss Sie S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="4eef5-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="4eef5-116">Wenn dies nicht möglich ist, muss ein entsprechender **HRESULT** -Fehlercode zurückgegeben werden, und \* *PPStream* sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eef5-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4eef5-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eef5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eef5-118">**Quell-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="4eef5-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




