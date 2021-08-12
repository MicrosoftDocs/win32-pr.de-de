---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Aufheben der Registrierung bei einer Benachrichtigung, für die Sie sich zuvor registriert haben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 64fb54226f1fad0d1d36f8f4260c9c9172b105dc6239ea5cb805c32b57a938ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278881"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>IDXCoreAdapterFactory::UnregisterEventNotification-Methode

Aufheben der Registrierung bei einer Benachrichtigung, für die Sie sich zuvor registriert haben. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="eventcookie"></a>eventCookie

Typ: **uint32_t**

Der Cookiewert (zurückgegeben, als Sie [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)aufgerufen haben), der eine vorherige Registrierung darstellt, für die Sie jetzt die Registrierung aufheben möchten.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|Beschreibung|
|-|-|
|E_INVALIDARG|Der Wert von *eventCookie* ist kein gültiges Cookie, das eine vorherige Registrierung darstellt.|

## <a name="remarks"></a>Hinweise

**UnregisterEventNotification** wird erst zurückgegeben, nachdem alle ausstehenden/laufenden Rückrufe für diese Registrierung abgeschlossen wurden. DXCore garantiert, dass für diese Registrierung keine neuen Rückrufe erfolgen, nachdem **UnregisterEventNotification** zurückgegeben wurde. Um jedoch einen Deadlock zu vermeiden, wartet **UnregisterEventNotification** nicht auf den Abschluss des aktiven Rückrufs, wenn Sie **UnregisterEventNotification** aus Ihrem Rückruf aufrufen.

> [!IMPORTANT]
> Bevor Sie das DXCore-Objekt zerstören, das durch das *dxCoreObject-Argument* dargestellt wird, das an [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)übergeben wird, müssen Sie den Cookiewert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen durch Aufrufen von **UnregisterEventNotification** aufheben. Wenn Sie dies nicht tun, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.

Nachdem Sie die Registrierung eines Cookiewerts aufgehoben haben, kann dieser Wert von einer nachfolgenden Registrierung zurückgegeben werden.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)