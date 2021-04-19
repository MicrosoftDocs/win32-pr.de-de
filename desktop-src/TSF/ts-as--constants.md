---
title: TS_AS_ Konstanten (textstor. h)
description: Die folgenden Flags geben die Ereignisse an, die die AdviseSink-Methoden aufzurufen.
ms.assetid: 8f406b67-f846-4712-b4be-811dbcc6ad55
topic_type:
- apiref
api_name:
- TS_AS_TEXT_CHANGE
- TS_AS_SEL_CHANGE
- TS_AS_LAYOUT_CHANGE
- TS_AS_ATTR_CHANGE
- TS_AS_STATUS_CHANGE
- TS_AS_ALL_SINKS
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7b36bdc2c3b559693503b2a8e408a0782855f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346322"
---
# <a name="ts_as_-constants"></a><span data-ttu-id="67c81-103">TS \_ als \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="67c81-103">TS\_AS\_\* Constants</span></span>

<span data-ttu-id="67c81-104">Die folgenden Flags geben die Ereignisse an, die die **AdviseSink** -Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="67c81-104">The following flags specify the events that call the **AdviseSink** methods.</span></span>



| <span data-ttu-id="67c81-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="67c81-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="67c81-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67c81-106">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| <span id="TS_AS_TEXT_CHANGE"></span><span id="ts_as_text_change"></span><dl> <span data-ttu-id="67c81-107"><dt>**TS \_ Als \_ Text \_ Änderung**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-107"><dt>**TS\_AS\_TEXT\_CHANGE**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="67c81-108">Der Text wird im Dokument geändert.</span><span class="sxs-lookup"><span data-stu-id="67c81-108">Text is changed in the document.</span></span><br/>                          |
| <span id="TS_AS_SEL_CHANGE"></span><span id="ts_as_sel_change"></span><dl> <span data-ttu-id="67c81-109"><dt>**TS \_ AS \_ - \_ Änderung**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-109"><dt>**TS\_AS\_SEL\_CHANGE**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="67c81-110">Im Dokument ist Text ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="67c81-110">Text is selected in the document.</span></span><br/>                         |
| <span id="TS_AS_LAYOUT_CHANGE"></span><span id="ts_as_layout_change"></span><dl> <span data-ttu-id="67c81-111"><dt>**TS \_ Bei \_ \_ Änderung des Layouts**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-111"><dt>**TS\_AS\_LAYOUT\_CHANGE**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="67c81-112">Das Layout des Dokuments wird geändert.</span><span class="sxs-lookup"><span data-stu-id="67c81-112">The layout of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ATTR_CHANGE"></span><span id="ts_as_attr_change"></span><dl> <span data-ttu-id="67c81-113"><dt>**TS \_ Als \_ attr- \_ Änderung**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-113"><dt>**TS\_AS\_ATTR\_CHANGE**</dt> <dt>( 0x8 )</dt></span></span> </dl>                                                                                                               | <span data-ttu-id="67c81-114">Die Attribute des Dokuments werden geändert.</span><span class="sxs-lookup"><span data-stu-id="67c81-114">The attributes of the document is changed.</span></span><br/>                |
| <span id="TS_AS_STATUS_CHANGE"></span><span id="ts_as_status_change"></span><dl> <span data-ttu-id="67c81-115"><dt>**TS \_ Als \_ Status \_ Änderung**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-115"><dt>**TS\_AS\_STATUS\_CHANGE**</dt> <dt>( 0x10 )</dt></span></span> </dl>                                                                                                        | <span data-ttu-id="67c81-116">Der Status des Dokuments wird geändert.</span><span class="sxs-lookup"><span data-stu-id="67c81-116">The status of the document is changed.</span></span><br/>                    |
| <span id="TS_AS_ALL_SINKS"></span><span id="ts_as_all_sinks"></span><dl> <span data-ttu-id="67c81-117"><dt>**TS \_ \_alle \_ senken**</dt> <dt>(TS \_ As Text Change TS as \_ \_ \| \_ \_ SEL \_ Change TS as Layout Change TS as \| \_ \_ \_ \| \_ \_ attr Change TS as \_ \| \_ \_ Status \_ Change)</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-117"><dt>**TS\_AS\_ALL\_SINKS**</dt> <dt>( TS\_AS\_TEXT\_CHANGE \| TS\_AS\_SEL\_CHANGE \| TS\_AS\_LAYOUT\_CHANGE \| TS\_AS\_ATTR\_CHANGE \| TS\_AS\_STATUS\_CHANGE )</dt></span></span> </dl> | <span data-ttu-id="67c81-118">Eines der vorherigen vier Ereignisse ist im Dokument aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="67c81-118">One of the previous four events occurred in the document.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="67c81-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67c81-119">Requirements</span></span>



| <span data-ttu-id="67c81-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67c81-120">Requirement</span></span> | <span data-ttu-id="67c81-121">Wert</span><span class="sxs-lookup"><span data-stu-id="67c81-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67c81-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67c81-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67c81-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67c81-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="67c81-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67c81-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67c81-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67c81-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67c81-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="67c81-126">Redistributable</span></span><br/>          | <span data-ttu-id="67c81-127">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="67c81-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="67c81-128">Header</span><span class="sxs-lookup"><span data-stu-id="67c81-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c81-129"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-129"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="67c81-130">IDL</span><span class="sxs-lookup"><span data-stu-id="67c81-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67c81-131"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67c81-131"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





