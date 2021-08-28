---
description: Fehler bei einem asynchronen Befehl zum Ausführen des Graphen.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82383c541f2ba5294cf4d45844f096ff510f25444ce87a54b956d0a777a7fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051780"
---
# <a name="ec_error_stillplaying"></a>EC \_ ERROR \_ STILLPLAYING

Fehler bei einem asynchronen Befehl zum Ausführen des Graphen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Fehlercode des fehlgeschlagenen Vorgangs.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Wenn der Filterdiagramm-Manager einen asynchronen Ausführungsbefehl aus gibt, der fehlschlägt, sendet er dieses Ereignis an die Anwendung. Das Diagramm verbleibt in einem ausgeführten Zustand. Der Zustand der zugrunde liegenden Filter ist unbestimmt. Einige Filter werden möglicherweise ausgeführt, andere nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




