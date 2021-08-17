---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Bestimmt, ob ein angegebener Benachrichtigungstyp vom Betriebssystem unterstützt wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0c5097f89583f0f6b04e0e8fb033446aae45743a8fb5a7fe9134f34bcc5e05fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118704"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>IDXCoreAdapterFactory::IsNotificationTypeSupported-Methode

Bestimmt, ob ein angegebener Benachrichtigungstyp vom Betriebssystem unterstützt wird. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="notificationtype"></a>notificationType

Typ: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Der Typ der Benachrichtigung, für die Sie Unterstützung abfragen. Informationen zu den Benachrichtigungstypen finden Sie in der Tabelle in [DXCoreNotificationType.](./ne-dxcore_interface-dxcorenotificationtype.md)

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt `true` zurück, wenn der Benachrichtigungstyp vom System unterstützt wird. Andernfalls wird `false`zurückgegeben.

## <a name="remarks"></a>Hinweise

Sie können **IsNotificationTypeSupported** aufrufen, um zu bestimmen, ob dieser Version des Betriebssystems ein bestimmter Benachrichtigungstyp bekannt ist. Beispielsweise ist ein Benachrichtigungstyp, der in einer bestimmten Version von Windows eingeführt wurde, für frühere Versionen von Windows unbekannt.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) [DXCore-Referenz,](../dxcore-reference.md) [DXCore-Adapterattribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)