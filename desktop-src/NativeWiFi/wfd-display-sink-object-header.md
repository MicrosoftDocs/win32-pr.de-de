---
description: Beschreibt die in einem Benachrichtigungs-oder Benachrichtigungs Ergebnis enthaltenen Daten der Senke-Objektdaten.
ms.assetid: 40D931F6-C068-48EB-A968-9CBAA3F9FAD8
title: WFD_DISPLAY_SINK_OBJECT_HEADER-Struktur (WF-Sink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: cdefd6b0b91fefb0f42a6e37e7584f7cd966884b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864808"
---
# <a name="wfd_display_sink_object_header-structure"></a><span data-ttu-id="75e19-103">WFD- \_ Anzeige \_ Sink- \_ Objekt \_ Header Struktur</span><span class="sxs-lookup"><span data-stu-id="75e19-103">WFD\_DISPLAY\_SINK\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="75e19-104">Die **WFD- \_ Anzeige Sink-Objekt \_ \_ \_ Header** Struktur beschreibt die in einem Benachrichtigungs-oder Benachrichtigungs Ergebnis enthaltenen Daten der Senke-Objektdaten.</span><span class="sxs-lookup"><span data-stu-id="75e19-104">The **WFD\_DISPLAY\_SINK\_OBJECT\_HEADER** structure describes the display sink object data included in a notification or notification result.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75e19-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Length;
} WFD_DISPLAY_SINK_OBJECT_HEADER, *PWFD_DISPLAY_SINK_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="75e19-106">Member</span><span class="sxs-lookup"><span data-stu-id="75e19-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="75e19-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="75e19-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="75e19-108">Der Typ des anzeigesenkjektobjekts.</span><span class="sxs-lookup"><span data-stu-id="75e19-108">The type of the display sink object.</span></span> <span data-ttu-id="75e19-109">Sie können den Bezeichner **WFD \_ Display \_ Sink \_ Object \_ Type \_ default** verwenden, der als Wert 1 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="75e19-109">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_TYPE\_DEFAULT** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="75e19-110">**Novel**</span><span class="sxs-lookup"><span data-stu-id="75e19-110">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="75e19-111">Die Revisions Version des Objekts für die Anzeige Senke.</span><span class="sxs-lookup"><span data-stu-id="75e19-111">The revision version of the display sink object.</span></span> <span data-ttu-id="75e19-112">Sie können den Bezeichner **WFD \_ Display \_ Sink \_ Object \_ Revision \_ Version \_ 1** verwenden, der als Wert 1 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="75e19-112">You can use the identifier **WFD\_DISPLAY\_SINK\_OBJECT\_REVISION\_VERSION\_1** which is defined as the value 1.</span></span>

</dd> <dt>

<span data-ttu-id="75e19-113">**Länge**</span><span class="sxs-lookup"><span data-stu-id="75e19-113">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="75e19-114">Die Länge der Daten im Benachrichtigungs-oder Benachrichtigungs Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="75e19-114">The length of the data in the notification or notification result.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75e19-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75e19-115">Requirements</span></span>



| <span data-ttu-id="75e19-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75e19-116">Requirement</span></span> | <span data-ttu-id="75e19-117">Wert</span><span class="sxs-lookup"><span data-stu-id="75e19-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75e19-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75e19-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75e19-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="75e19-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="75e19-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75e19-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75e19-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75e19-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="75e19-122">Header</span><span class="sxs-lookup"><span data-stu-id="75e19-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="75e19-123"><dt>WF-Senke. h</dt></span><span class="sxs-lookup"><span data-stu-id="75e19-123"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




