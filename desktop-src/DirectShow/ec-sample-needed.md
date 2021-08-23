---
description: Fordert ein neues Eingabebeispiel vom EvR-Filter (Enhanced Video Renderer) an.
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0058f8d0b7f8404a59f8c7e4fc5a4029c5ebaf4bc4f5c1b2678b1ed8c0f4f90c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686120"
---
# <a name="ec_sample_needed"></a>EC \_ SAMPLE \_ NEEDED

Fordert ein neues Eingabebeispiel vom EVR-Filter [**(Enhanced Video Renderer)**](enhanced-video-renderer-filter.md) an.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Bezeichner des Eingabestreams, der eine neue Eingabe benötigt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Der Mixer für den EVR-Filter sendet diese Nachricht, wenn er ein neues Eingabebeispiel benötigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> </dl>

 

 




