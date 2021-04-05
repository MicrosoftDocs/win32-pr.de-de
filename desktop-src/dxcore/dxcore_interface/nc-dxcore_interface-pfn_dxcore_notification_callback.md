---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Eine Rückruffunktion (implementiert von Ihrer Anwendung), die von einem DXCore-Objekt für Benachrichtigungs Ereignisse aufgerufen wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948993"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>PFN_DXCORE_NOTIFICATION_CALLBACK Rückruf

Eine Rückruffunktion (implementiert von Ihrer Anwendung), die von einem DXCore-Objekt für Benachrichtigungs Ereignisse aufgerufen wird.

## <a name="syntax"></a>Syntax

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Parameter

### <a name="notificationtype"></a>notificationType

Typ: **[dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md)**

Der Typ der Benachrichtigung, die diesen Aufruf darstellt. Informationen zu den Typen, die für welche Arten von Objekten gültig sind, finden Sie in der Tabelle unter [dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md) .

### <a name="object"></a>Objekt (object)

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Das [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -oder [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Objekt, das die Benachrichtigung erhöht.

### <a name="context-in"></a>Kontext [in]

Typ: **void \***

Ein Zeiger `nullptr` auf ein Objekt, das Kontextinformationen enthält.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)