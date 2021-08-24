---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Eine Rückruffunktion (implementiert von Ihrer Anwendung), die von einem DXCore-Objekt für Benachrichtigungsereignisse aufgerufen wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787100"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>PFN_DXCORE_NOTIFICATION_CALLBACK Rückruf

Eine Rückruffunktion (implementiert von Ihrer Anwendung), die von einem DXCore-Objekt für Benachrichtigungsereignisse aufgerufen wird.

## <a name="syntax"></a>Syntax

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Parameter

### <a name="notificationtype"></a>notificationType

Typ: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Der Typ der Benachrichtigung, die diesen Aufruf darstellt. Informationen dazu, welche Typen mit welchen Objekttypen gültig sind, finden Sie in der Tabelle in [DXCoreNotificationType.](./ne-dxcore_interface-dxcorenotificationtype.md)

### <a name="object"></a>Objekt (object)

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Das [IDXCoreAdapter- oder](./nn-dxcore_interface-idxcoreadapter.md) [IDXCoreAdapterList-Objekt,](./nn-dxcore_interface-idxcoreadapterlist.md) das die Benachrichtigung anfing.

### <a name="context-in"></a>context [in]

Typ: **\* void**

Ein Zeiger, der sein `nullptr` kann, auf ein Objekt, das Kontextinformationen enthält.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), Verwenden von DXCore zum [Auflisten von Adaptern](../dxcore-enum-adapters.md)