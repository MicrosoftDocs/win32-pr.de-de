---
title: Iconfigasfwriter getindexmode-Methode
description: Die getindexmode-Methode ruft den aktuellen temporalen Index Modus ab.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Getindexmode-Methode Windows Media-Format
- Getindexmode-Methode, Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getindexmode-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390572"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="fa3fe-106">Iconfigasfwriter:: getindexmode-Methode</span><span class="sxs-lookup"><span data-stu-id="fa3fe-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="fa3fe-107">Die **getindexmode** -Methode ruft den aktuellen temporalen Index Modus ab.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3fe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa3fe-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="fa3fe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa3fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa3fe-110">*pbindexfile* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fa3fe-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa3fe-111">Ein Zeiger auf eine Variable vom Typ **bool** , der die Einstellung für den temporalen Indexmodus empfängt.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="fa3fe-112">Der Wert **true** gibt an, dass der WM-ASF-Writer so konfiguriert ist, dass Temporale indizierte Dateien geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa3fe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa3fe-113">Return value</span></span>

<span data-ttu-id="fa3fe-114">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="fa3fe-115">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3fe-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa3fe-116">Remarks</span></span>

<span data-ttu-id="fa3fe-117">Verwenden Sie diese Methode, um zu bestimmen, ob der [WM-ASF-Writer](wm-asf-writer-filter.md) momentan zum Schreiben temporärindizierter ASF-Dateien konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="fa3fe-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="fa3fe-118">Weitere Informationen über Temporale indizierte und Frame indizierte Dateien finden Sie in den Hinweisen zu [**iconfigasfwriter:: setindexmode**](iconfigasfwriter-setindexmode.md).</span><span class="sxs-lookup"><span data-stu-id="fa3fe-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fa3fe-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa3fe-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa3fe-120">[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa3fe-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 