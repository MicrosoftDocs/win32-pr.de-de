---
title: Iconfigasfwriter setindexmode-Methode
description: Die setindexmode-Methode ermöglicht der Anwendung, zu steuern, ob die Datei temporell indiziert wird.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Setindexmode-Methode Windows Media-Format
- Setindexmode-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, setindexmode-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039036"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="64583-106">Iconfigasfwriter:: setindexmode-Methode</span><span class="sxs-lookup"><span data-stu-id="64583-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="64583-107">Die **setindexmode** -Methode ermöglicht der Anwendung, zu steuern, ob die Datei temporell indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="64583-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="64583-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64583-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="64583-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="64583-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64583-110">*bindexfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64583-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64583-111">Variable vom Typ **bool**; **True** gibt an, dass die Datei temporell indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="64583-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64583-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64583-112">Return value</span></span>

<span data-ttu-id="64583-113">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="64583-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="64583-114">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64583-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64583-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64583-115">Remarks</span></span>

<span data-ttu-id="64583-116">Standardmäßig erstellt der [WM-ASF-Writer](wm-asf-writer-filter.md) Temporale indizierte ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="64583-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="64583-117">Die Indizierung wird durchführt, wenn das Diagramm angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="64583-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="64583-118">Sie können dieses Verhalten deaktivieren, wenn Sie eine eigene Frame basierte Indizierung als nach Verarbeitungsschritt ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="64583-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="64583-119">Um eine Frame indizierte Datei zu erstellen, rufen Sie **setindexmode**(false) auf, erstellen Sie die Datei, und verwenden Sie dann die SDK-Methoden des Windows Media-Formats direkt, um einen Frame basierten Index für die Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64583-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="64583-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64583-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="64583-121">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64583-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 