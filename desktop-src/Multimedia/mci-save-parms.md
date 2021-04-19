---
title: MCI_SAVE_PARMS-Struktur (mciapi. h)
description: Die MCI \_ - \_ Struktur zum Speichern von Parametern enthält die Dateinamen Informationen für den MCI- \_ Befehl "Save".
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- MCI_SAVE_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341781"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="74ae2-104">MCI- \_ Struktur zum Speichern von \_ Parametern</span><span class="sxs-lookup"><span data-stu-id="74ae2-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="74ae2-105">Die **MCI-Struktur zum \_ Speichern von \_ Parametern** enthält die Dateinamen Informationen für den MCI-Befehl " [**\_ Save**](mci-save.md) ".</span><span class="sxs-lookup"><span data-stu-id="74ae2-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="74ae2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="74ae2-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="74ae2-107">Member</span><span class="sxs-lookup"><span data-stu-id="74ae2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="74ae2-108">**dwcallback**</span><span class="sxs-lookup"><span data-stu-id="74ae2-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="74ae2-109">Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="74ae2-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="74ae2-110">**lpFileName**</span><span class="sxs-lookup"><span data-stu-id="74ae2-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="74ae2-111">Der Name der zu speichernden Datei.</span><span class="sxs-lookup"><span data-stu-id="74ae2-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74ae2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74ae2-112">Remarks</span></span>

<span data-ttu-id="74ae2-113">Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="74ae2-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ae2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74ae2-114">Requirements</span></span>



| <span data-ttu-id="74ae2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74ae2-115">Requirement</span></span> | <span data-ttu-id="74ae2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="74ae2-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74ae2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74ae2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74ae2-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74ae2-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74ae2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74ae2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74ae2-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74ae2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74ae2-121">Header</span><span class="sxs-lookup"><span data-stu-id="74ae2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ae2-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ae2-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ae2-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74ae2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ae2-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="74ae2-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="74ae2-125">**MCI-Strukturen**</span><span class="sxs-lookup"><span data-stu-id="74ae2-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="74ae2-126">**MCI- \_ Speicherung**</span><span class="sxs-lookup"><span data-stu-id="74ae2-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="74ae2-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="74ae2-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

