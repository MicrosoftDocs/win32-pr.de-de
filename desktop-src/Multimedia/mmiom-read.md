---
title: MMIOM_READ Meldung (MMSYSTEM. h)
description: Die mmiom- \_ Lese Meldung wird von der mmioread-Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine angegebene Anzahl von Bytes aus einer geöffneten Datei gelesen werden soll.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479374"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="b8df1-104">Mmiom- \_ Lese Meldung</span><span class="sxs-lookup"><span data-stu-id="b8df1-104">MMIOM\_READ message</span></span>

<span data-ttu-id="b8df1-105">Die **mmiom- \_ Lese** Meldung wird von der [**mmioread**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) -Funktion an eine e/a-Prozedur gesendet, um anzufordern, dass eine angegebene Anzahl von Bytes aus einer geöffneten Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8df1-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="b8df1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8df1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8df1-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lbuffer*</span><span class="sxs-lookup"><span data-stu-id="b8df1-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="b8df1-108">Zeiger auf den Puffer, der mit aus der Datei gelesenen Daten gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8df1-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="b8df1-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*CBRot*</span><span class="sxs-lookup"><span data-stu-id="b8df1-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="b8df1-110">Anzahl der aus der Datei gelesenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="b8df1-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8df1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8df1-111">Return Value</span></span>

<span data-ttu-id="b8df1-112">Gibt die Anzahl der tatsächlich aus der Datei gelesenen Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="b8df1-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="b8df1-113">Wenn keine weiteren Bytes gelesen werden können, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="b8df1-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="b8df1-114">Wenn ein Fehler auftritt, ist der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="b8df1-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8df1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8df1-115">Remarks</span></span>

<span data-ttu-id="b8df1-116">Die e/a-Prozedur ist dafür verantwortlich, den **ldiskoffset** -Member der [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur zu aktualisieren, um die neue Dateiposition nach dem Lesevorgang widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="b8df1-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8df1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8df1-117">Requirements</span></span>



| <span data-ttu-id="b8df1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8df1-118">Requirement</span></span> | <span data-ttu-id="b8df1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="b8df1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8df1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8df1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b8df1-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8df1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b8df1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8df1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b8df1-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8df1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b8df1-124">Header</span><span class="sxs-lookup"><span data-stu-id="b8df1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8df1-125"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8df1-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

