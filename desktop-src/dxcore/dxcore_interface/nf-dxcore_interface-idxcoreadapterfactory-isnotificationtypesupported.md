---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Bestimmt, ob ein angegebener Benachrichtigungstyp vom Betriebssystem unterstützt wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315968"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>Idxcoreadapterfactory:: isnotificationtypesupportiert-Methode

Bestimmt, ob ein angegebener Benachrichtigungstyp vom Betriebssystem unterstützt wird. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="notificationtype"></a>notificationType

Typ: **[dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md)**

Der Typ der Benachrichtigung, die Sie für die Unterstützung von Abfragen. Informationen zu den Benachrichtigungs Typen finden Sie in der Tabelle unter [dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md) .

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt zurück,  `true`   Wenn der Benachrichtigungstyp vom System unterstützt wird. Andernfalls wird zurückgegeben  `false` .

## <a name="remarks"></a>Bemerkungen

Sie können **isnotificationtypesupportiert** anrufen, um zu bestimmen, ob ein bestimmter Benachrichtigungstyp dieser Version des Betriebssystems bekannt ist. Beispielsweise ist ein Benachrichtigungstyp, der in einer bestimmten Version von Windows eingeführt wurde, in früheren Versionen von Windows unbekannt.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)