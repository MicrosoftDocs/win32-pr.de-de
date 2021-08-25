---
description: Das Filterdiagramm wird heruntergefahren, bevor es zerstört wird.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917a8f79b1a5201e50d0fcf2761a99b2801f75601f95ef866902492fb36065f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079110"
---
# <a name="ec_shutting_down"></a>EC \_ WIRD \_ HERUNTERGEFAHREN

Das Filterdiagramm wird heruntergefahren, bevor es zerstört wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Keinen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Dieses Ereignis wird nicht an die Anwendung gesendet. Der Filtergraph-Manager sendet ihn an Plug-In-Verteiler, um sie darüber zu informieren, dass der Graph heruntergefahren wird. Anwendungen können die Standardaktion dieses Ereignisses nicht überschreiben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




