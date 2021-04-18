---
title: 'Idodownload:: Start-Methode'
description: Startet einen Download oder nimmt diesen wieder auf.
keywords:
- 'Idodownload:: Start-Methode'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106365025"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="29693-104">Idodownload:: Start-Methode</span><span class="sxs-lookup"><span data-stu-id="29693-104">IDODownload::Start method</span></span>

<span data-ttu-id="29693-105">Startet oder setzt einen Download fort und übergibt optionale Bereiche als Zeiger auf [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="29693-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="29693-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="29693-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="29693-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="29693-107">Parameters</span></span>

`ranges`

<span data-ttu-id="29693-108">Optional.</span><span class="sxs-lookup"><span data-stu-id="29693-108">Optional.</span></span> <span data-ttu-id="29693-109">Ein Zeiger auf eine [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) Struktur (um nur bestimmte Bereiche der Datei herunterzuladen).</span><span class="sxs-lookup"><span data-stu-id="29693-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="29693-110">Übergeben `nullptr` Sie, um die gesamte Datei herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="29693-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="29693-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29693-111">Return Value</span></span>

<span data-ttu-id="29693-112">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29693-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="29693-113">Andernfalls wird ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) - [Fehlercode](/windows/desktop/com/com-error-codes-10)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="29693-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="29693-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29693-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="29693-115">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="29693-115">**Minimum supported client**</span></span> | <span data-ttu-id="29693-116">Nur Windows 10, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="29693-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="29693-117">**Unterstützte Mindestversion (Server)**</span><span class="sxs-lookup"><span data-stu-id="29693-117">**Minimum supported server**</span></span> | <span data-ttu-id="29693-118">Nur Windows Server, Version 1809, \[ Win32-Anwendungen\]</span><span class="sxs-lookup"><span data-stu-id="29693-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="29693-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="29693-119">**Header**</span></span> | <span data-ttu-id="29693-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="29693-120">Do.h</span></span> |
