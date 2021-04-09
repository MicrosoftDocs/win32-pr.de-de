---
title: Festlegen des Zeit Formats
description: Festlegen des Zeit Formats
ms.assetid: c670d47e-30fc-4637-b468-b6a415605dca
keywords:
- MCI_SET Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6bc48faa36fea49b0aba749476c998572ebf400
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858201"
---
# <a name="setting-the-time-format"></a><span data-ttu-id="ae2ce-104">Festlegen des Zeit Formats</span><span class="sxs-lookup"><span data-stu-id="ae2ce-104">Setting the Time Format</span></span>

<span data-ttu-id="ae2ce-105">Verwenden Sie die [**MCI \_**](mci-set.md) -Befehlszeile, um [**das Zeit \_ \_**](mci-set-parms.md) Format für ein geöffnetes Gerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae2ce-105">Use the [**MCI\_SET**](mci-set.md) command message along with the [**MCI\_SET\_PARMS**](mci-set-parms.md) structure to set the time format for an open device.</span></span> <span data-ttu-id="ae2ce-106">Legen Sie den **dwtimeformat** -Member auf eine der folgenden Konstanten fest.</span><span class="sxs-lookup"><span data-stu-id="ae2ce-106">Set the **dwTimeFormat** member to one of the following constants.</span></span>



| <span data-ttu-id="ae2ce-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="ae2ce-107">Constant</span></span>                   | <span data-ttu-id="ae2ce-108">Zeitformat</span><span class="sxs-lookup"><span data-stu-id="ae2ce-108">Time format</span></span>                                          |
|----------------------------|------------------------------------------------------|
| <span data-ttu-id="ae2ce-109">MCI- \_ Format ( \_ Bytes)</span><span class="sxs-lookup"><span data-stu-id="ae2ce-109">MCI\_FORMAT\_BYTES</span></span>         | <span data-ttu-id="ae2ce-110">Bytes (in den PCM-Format Dateien mit Pulse Code-Modul \[ \] )</span><span class="sxs-lookup"><span data-stu-id="ae2ce-110">Bytes (in pulse code modulated \[PCM\] format files)</span></span> |
| <span data-ttu-id="ae2ce-111">MCI- \_ Format ( \_ Millisekunden)</span><span class="sxs-lookup"><span data-stu-id="ae2ce-111">MCI\_FORMAT\_MILLISECONDS</span></span>  | <span data-ttu-id="ae2ce-112">Millisekunden</span><span class="sxs-lookup"><span data-stu-id="ae2ce-112">Milliseconds</span></span>                                         |
| <span data-ttu-id="ae2ce-113">MCI- \_ Format \_ MSF</span><span class="sxs-lookup"><span data-stu-id="ae2ce-113">MCI\_FORMAT\_MSF</span></span>           | <span data-ttu-id="ae2ce-114">Minute/Sekunde/Frame</span><span class="sxs-lookup"><span data-stu-id="ae2ce-114">Minute/second/frame</span></span>                                  |
| <span data-ttu-id="ae2ce-115">MCI- \_ Format \_ Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae2ce-115">MCI\_FORMAT\_SAMPLES</span></span>       | <span data-ttu-id="ae2ce-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae2ce-116">Samples</span></span>                                              |
| <span data-ttu-id="ae2ce-117">MCI- \_ Format, \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="ae2ce-117">MCI\_FORMAT\_SMPTE\_24</span></span>     | <span data-ttu-id="ae2ce-118">SMPTE, 24 Frame</span><span class="sxs-lookup"><span data-stu-id="ae2ce-118">SMPTE, 24 frame</span></span>                                      |
| <span data-ttu-id="ae2ce-119">MCI- \_ Format, \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="ae2ce-119">MCI\_FORMAT\_SMPTE\_25</span></span>     | <span data-ttu-id="ae2ce-120">SMPTE, 25 Frame</span><span class="sxs-lookup"><span data-stu-id="ae2ce-120">SMPTE, 25 frame</span></span>                                      |
| <span data-ttu-id="ae2ce-121">MCI- \_ Format \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="ae2ce-121">MCI\_FORMAT\_SMPTE\_30</span></span>     | <span data-ttu-id="ae2ce-122">SMPTE, 30 Frame</span><span class="sxs-lookup"><span data-stu-id="ae2ce-122">SMPTE, 30 frame</span></span>                                      |
| <span data-ttu-id="ae2ce-123">MCI- \_ Format \_ SMPTE \_ 30drop</span><span class="sxs-lookup"><span data-stu-id="ae2ce-123">MCI\_FORMAT\_SMPTE\_30DROP</span></span> | <span data-ttu-id="ae2ce-124">SMPTE, 30-Frame-Drop</span><span class="sxs-lookup"><span data-stu-id="ae2ce-124">SMPTE, 30 frame drop</span></span>                                 |
| <span data-ttu-id="ae2ce-125">MCI- \_ Format- \_ TMSF</span><span class="sxs-lookup"><span data-stu-id="ae2ce-125">MCI\_FORMAT\_TMSF</span></span>          | <span data-ttu-id="ae2ce-126">Nachverfolgung/Minute/Sekunde/Frame</span><span class="sxs-lookup"><span data-stu-id="ae2ce-126">Track/minute/second/frame</span></span>                            |
| <span data-ttu-id="ae2ce-127">MCI-Format für das Setup- \_ \_ Format \_</span><span class="sxs-lookup"><span data-stu-id="ae2ce-127">MCI\_SEQ\_FORMAT\_SONGPTR</span></span>  | <span data-ttu-id="ae2ce-128">MIDI-Song Zeiger</span><span class="sxs-lookup"><span data-stu-id="ae2ce-128">MIDI song pointer</span></span>                                    |



 

<span data-ttu-id="ae2ce-129">Im folgenden Beispiel wird das Zeitformat auf dem Gerät, das durch die wdeviceid-Variable angegeben wird, mithilfe der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion auf Millisekunden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae2ce-129">The following example sets the time format to milliseconds on the device specified by the wDeviceID variable using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID; 
MCI_SET_PARMS mciSetParms; 

// Set time format to milliseconds. 

mciSetParms.dwTimeFormat = MCI_FORMAT_MILLISECONDS; 
if( mciSendCommand(wDeviceID, MCI_SET, MCI_SET_TIME_FORMAT, 
                  (DWORD) &mciSetParms)) 
{
    // Error, unable to set time format. 
    return FALSE; 
}
else 
{
    // Time format set successfully. 
    return TRUE; 
}
```



 

 