---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Hebt die Registrierung bei einer Benachrichtigung auf, die Sie zuvor für registriert haben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390808"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>Idxcoreadapterfactory:: unregistereventnotification-Methode

Hebt die Registrierung bei einer Benachrichtigung auf, die Sie zuvor für registriert haben. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="eventcookie"></a>eventcookie

Typ: **uint32_t**

Der Cookie-Wert (zurückgegeben, wenn Sie [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)aufgerufen haben), der eine vorherige Registrierung darstellt, für die die Registrierung aufgehoben werden soll.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|E_INVALIDARG|Der Wert von *eventcookie* ist kein gültiges Cookie, das eine vorherige Registrierung darstellt.|

## <a name="remarks"></a>Bemerkungen

**Unregistereventnotification** wird erst zurückgegeben, nachdem alle ausstehenden/in-Progress-Rückrufe für diese Registrierung abgeschlossen wurden. DXCore stellt sicher, dass für diese Registrierung keine neuen Rückrufe auftreten, nachdem **unregistereventnotification** zurückgegeben wurde. Um jedoch einen Deadlock zu vermeiden, wartet **unregistereventnotification** nicht auf den Abschluss des aktiven Rückrufs, wenn Sie **unregistereventnotification** innerhalb des Rückrufs aufrufen.

> [!IMPORTANT]
> Bevor Sie das DXCore-Objekt zerstören, das durch das *dxcoreobject* -Argument dargestellt wird, das an [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)übermittelt wird, müssen Sie den Cookie-Wert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen aufzuheben, indem Sie **unregistereventnotification** aufrufen. Wenn Sie dies nicht tun, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.

Nachdem Sie die Registrierung eines cookienwerts aufgehoben haben, kann dieser Wert von einer nachfolgenden Registrierung zurückgegeben werden.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)