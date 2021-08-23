---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Registriert , um Benachrichtigungen über bestimmte Bedingungen von einem DXCore-Adapter oder einer Adapterliste zu empfangen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b97b51f7c4359526317647b62241e37063243a56f45014c28ba2f2cd897706ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042898"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>IDXCoreAdapterFactory::RegisterEventNotification-Methode

Registriert , um Benachrichtigungen über bestimmte Bedingungen von einem DXCore-Adapter oder einer Adapterliste zu empfangen. Programmierleitfäden und Codebeispiele finden Sie unter [Verwenden von DXCore zum Aufzählen von Adaptern.](../dxcore-enum-adapters.md)

## <a name="syntax"></a>Syntax

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="dxcoreobject-in"></a>dxCoreObject [in]

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Das DXCore-Objekt ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) oder [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)), dessen Benachrichtigungen Sie abonnieren.

### <a name="notificationtype"></a>notificationType

Typ: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Der Typ der Benachrichtigung, für die Sie sich registrieren. Informationen dazu, welche Typen für welche Objekttypen gültig sind, finden Sie in der Tabelle in [DXCoreNotificationType.](./ne-dxcore_interface-dxcorenotificationtype.md)

### <a name="callbackfunction-in"></a>callbackFunction [in]

Typ: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Ein Zeiger auf eine Rückruffunktion (von Ihrer Anwendung implementiert), die vom DXCore-Objekt für Benachrichtigungsereignisse aufgerufen wird. Die Signatur der Funktion finden Sie unter [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackContext [in]

Typ: **\* void**

Ein optionaler Zeiger auf ein Objekt, das Kontextinformationen enthält. Dieses Objekt wird an Ihre Rückruffunktion übergeben, wenn die Benachrichtigung ausgelöst wird.

### <a name="eventcookie-out"></a>eventCookie [out]

Typ: **uint32_t \***

Ein Zeiger auf einen **uint32_t** Wert. Bei Erfolg dereferenziert die Funktion den Zeiger und legt den Wert auf einen Cookiewert ungleich 0 (null) fest, der diese Registrierung darstellt. Verwenden Sie diesen Cookiewert, um die Registrierung bei der Benachrichtigung durch Aufrufen von [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)zu aufheben. Siehe **Hinweise**.

Wenn der Wert nicht erfolgreich ist, dereferenziert die Funktion den Zeiger und legt den Wert auf 0 (null) fest, was einen ungültigen Cookiewert darstellt.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT-Fehlercode**](../../com/structure-of-com-error-codes.md) [](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|Beschreibung|
|-|-|
|DXGI_ERROR_INVALID_CALL|*notificationType* wird vom Betriebssystem nicht unterstützt.|
|E_INVALIDARG|`nullptr` wurde für *dxCoreObject* bereitgestellt, oder , wenn eine ungültige *NotificationType-* und *dxCoreObject-Kombination* bereitgestellt wurde.|
|E_POINTER|`nullptr` wurde entweder für *callbackFunction* oder *eventCookie* bereitgestellt.|

## <a name="remarks"></a>Hinweise

Sie verwenden **RegisterEventNotification,** um sich für Ereignisse zu registrieren, die von [den Schnittstellen IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) und [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ausgelöst werden. Diese Benachrichtigungstypen werden unterstützt.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|Unterstützt *dxCoreObject*|Hinweise|
|-|-|-|
|AdapterList State|**IDXCoreAdapterList**|Gibt an, dass sich die Liste der Adapter, die Ihre Filterkriterien erfüllen, geändert hat. Wenn die Adapterliste zum Zeitpunkt der Registrierung veraltet ist, wird der Rückruf sofort aufgerufen. Dieser Rückruf erfolgt höchstens einmal pro Registrierung.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Gibt an, dass der Adapter nicht mehr gültig ist. Wenn der Adapter zur Registrierungszeit ungültig ist, wird der Rückruf sofort aufgerufen.|
|AdapterBudgetChange|**IDXCoreAdapter**|Gibt an, dass ein Speicherbudgetereignis aufgetreten ist und Dass Sie [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (mit [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) aufrufen sollten, um den aktuellen Speicherbudgetstatus auszuwerten. Bei der Registrierung erfolgt immer ein erster Rückruf, mit dem Sie den Anfangszustand abfragen können.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Gibt an, dass Sie den aktuellen Status der Kryptositzung neu auswerten sollten. Beispielsweise durch Aufrufen von [ID3D11VideoContext1::CheckCryptoSessionStatus,](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) um die Auswirkungen der Hardwareentschlüsselung für eine bestimmte [ID3D11CryptoSession-Schnittstelle](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) zu bestimmen. Bei der Registrierung erfolgt immer ein erster Rückruf, mit dem Sie den Anfangszustand abfragen können.|

Ein Aufruf der Funktion, die Sie in *callbackFunction* bereitstellen, wird von DXCore asynchron in einem Hintergrundthread ausgeführt, wenn das erkannte Ereignis auftritt. Es wird keine Garantie hinsichtlich der Reihenfolge oder des Zeitlichen Ablaufs von Rückrufen übernommen, dass &mdash; mehrere Rückrufe in beliebiger Reihenfolge oder sogar gleichzeitig auftreten können. Es ist sogar möglich, dass Ihr Rückruf aufgerufen wird, bevor **RegisterEventNotification** abgeschlossen ist. In diesem Fall garantiert DXCore, dass *EventCookie* festgelegt ist, bevor Der Rückruf aufgerufen wird. Mehrere Rückrufe für eine bestimmte Registrierung werden in der reihenfolge serialisiert.

Rückrufe können jederzeit auftreten, bis Sie [UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen und abgeschlossen sind. Rückrufe erfolgen in ihren eigenen Threads, und Sie können Aufrufe an die DXCore-API für diese Threads durchführen, einschließlich **UnregisterEventNotification.** Sie dürfen jedoch nicht den letzten Verweis auf *dxCoreObject* in diesem Thread freigeben.

> [!IMPORTANT]
> Bevor Sie das DXCore-Objekt zerstören, das durch das *dxCoreObject-Argument* dargestellt wird, das an **RegisterEventNotification** übergeben wird, müssen Sie den Cookiewert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen durch Aufrufen von [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufheben. Wenn Sie dies nicht tun, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)