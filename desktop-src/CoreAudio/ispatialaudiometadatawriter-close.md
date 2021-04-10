---
description: Schließt alle erforderlichen Vorgänge für den metadatenpuffer ab und gibt das angegebene ispatialaudiometadataitems-Objekt frei.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Ispatialaudiometadatawriter:: Close-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127312"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="5dbf5-103">Ispatialaudiometadatawriter:: Close-Methode</span><span class="sxs-lookup"><span data-stu-id="5dbf5-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="5dbf5-104">Schließt alle erforderlichen Vorgänge für den metadatenpuffer ab und gibt das angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) -Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbf5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dbf5-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="5dbf5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dbf5-106">Parameters</span></span>

<span data-ttu-id="5dbf5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5dbf5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5dbf5-108">Return value</span></span>

<span data-ttu-id="5dbf5-109">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5dbf5-110">Wenn ein Fehler auftritt, enthalten mögliche Rückgabecodes die in der folgenden Tabelle aufgeführten Werte, sind jedoch nicht darauf beschränkt.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="5dbf5-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5dbf5-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="5dbf5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dbf5-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5dbf5-113"><dt>**sptlaud \_ MD \_ CLNT \_ E \_ keine \_ Elemente \_ geöffnet**</dt></span><span class="sxs-lookup"><span data-stu-id="5dbf5-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="5dbf5-114">Das angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) wurde nicht mit einem geöffneten [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open)-Befehl geöffnet.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="5dbf5-115"><dt>**sptlaud \_ MD \_ CLNT \_ E \_ keine \_ Elemente \_ geschrieben**</dt></span><span class="sxs-lookup"><span data-stu-id="5dbf5-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="5dbf5-116">Es wurden keine Metadatenelemente in das angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="5dbf5-117"><dt>**das Element "sptlaud \_ MD \_ CLNT \_ E" \_ \_ muss \_ über \_ Befehle verfügen.**</dt></span><span class="sxs-lookup"><span data-stu-id="5dbf5-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="5dbf5-118">Es wurden keine metadatenbefehle in die angegebene [**ispatialaudiometadataitems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5dbf5-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="5dbf5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dbf5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbf5-120">**Ispatialaudiometadatawriter**</span><span class="sxs-lookup"><span data-stu-id="5dbf5-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




