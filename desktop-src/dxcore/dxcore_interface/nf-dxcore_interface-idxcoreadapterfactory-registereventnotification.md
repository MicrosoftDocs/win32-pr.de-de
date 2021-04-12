---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: Registriert den Empfang von Benachrichtigungen über bestimmte Bedingungen aus einer DXCore-Adapter-oder-Adapter Liste.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3643fbb01fc955049c297a577f18d4d276e73f46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473844"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>Idxcoreadapterfactory:: registereventnotification-Methode

Registriert den Empfang von Benachrichtigungen über bestimmte Bedingungen aus einer DXCore-Adapter-oder-Adapter Liste. Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).

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

### <a name="dxcoreobject-in"></a>dxcoreobject [in]

Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Das DXCore-Objekt ([idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) oder [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md)), dessen Benachrichtigungen Sie abonnieren.

### <a name="notificationtype"></a>notificationType

Typ: **[dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md)**

Der Benachrichtigungstyp, für den Sie sich registrieren. Informationen zu den Typen, die für welche Arten von Objekten gültig sind, finden Sie in der Tabelle unter [dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md) .

### <a name="callbackfunction-in"></a>callbackFunction [in]

Typ: **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Ein Zeiger auf eine Rückruffunktion (implementiert von Ihrer Anwendung), die vom DXCore-Objekt für Benachrichtigungs Ereignisse aufgerufen wird. Die Signatur der Funktion finden Sie unter [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackcontext [in]

Typ: **void \***

Ein optionaler Zeiger auf ein Objekt, das Kontextinformationen enthält. Dieses Objekt wird an Ihre Rückruffunktion übermittelt, wenn die Benachrichtigung ausgelöst wird.

### <a name="eventcookie-out"></a>eventcookie [out]

Typ: **uint32_t \***

Ein Zeiger auf einen **uint32_t** Wert. Wenn der Vorgang erfolgreich ist, dereferenziert die Funktion den Zeiger und legt den Wert auf einen Cookie-Wert ungleich 0 (null) fest, der diese Registrierung darstellt. Verwenden Sie diesen Cookie-Wert, um die Registrierung bei der Benachrichtigung aufzuheben, indem Sie [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen. Siehe **Hinweise**.

Wenn die Funktion nicht erfolgreich ist, wird der Zeiger dereferenziert und der Wert auf 0 (null) festgelegt, was einen ungültigen Cookie-Wert darstellt.

## <a name="returns"></a>Gibt zurück

Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.

|Rückgabewert|BESCHREIBUNG|
|-|-|
|DXGI_ERROR_INVALID_CALL|*NOTIFICATIONTYPE* wird vom Betriebssystem nicht unterstützt.|
|E_INVALIDARG|`nullptr` wurde für *dxcoreobject* bereitgestellt, oder, wenn eine ungültige Kombination aus *NOTIFICATIONTYPE* und *dxcoreobject* angegeben wurde.|
|E_POINTER|`nullptr` wurde für *callbackFunction* oder *eventcookie* bereitgestellt.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **registereventnotification** , um Ereignisse zu registrieren, die von [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -und [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -Schnittstellen ausgelöst werden. Diese Benachrichtigungs Typen werden unterstützt.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|Unterstütztes *dxcoreobject*|Notizen|
|-|-|-|
|Adapterliststale|**IDXCoreAdapterList**|Gibt an, dass die Liste der Adapter, die den Filterkriterien entsprechen, geändert wurde. Wenn die Adapter Liste zum Zeitpunkt der Registrierung veraltet ist, wird Ihr Rückruf sofort aufgerufen. Dieser Rückruf tritt höchstens einmal pro Registrierung auf.|
|Adapternolongervalid|**IDXCoreAdapter**|Gibt an, dass der Adapter nicht mehr gültig ist. Wenn der Adapter beim Registrierungs Zeitpunkt ungültig ist, wird der Rückruf sofort aufgerufen.|
|Adapterbudgetchange|**IDXCoreAdapter**|Gibt an, dass ein Speicher budgetierungsereignis aufgetreten ist, und dass Sie [idxcoreadapter:: querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md) (mit [dxcoreadapterstate:: adaptermemorybudget](./ne-dxcore_interface-dxcoreadapterstate.md)) zum Auswerten des aktuellen Arbeitsspeicher-Budget Zustands aufruft. Bei der Registrierung wird immer ein anfänglicher Rückruf ausgeführt, damit Sie den Anfangszustand Abfragen können.|
|Adapterhardwarecontentschutzteardown|**IDXCoreAdapter**|Gibt an, dass Sie den aktuellen Status der Kryptografiesitzung neu auswerten sollten. beispielsweise durch Aufrufen von [ID3D11VideoContext1:: checkcryptosessionstatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) , um die Auswirkung der Hardware Löschung für eine bestimmte [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) -Schnittstelle zu bestimmen. Bei der Registrierung wird immer ein anfänglicher Rückruf ausgeführt, damit Sie den Anfangszustand Abfragen können.|

Ein Aufruf der Funktion, die Sie in *callbackFunction* bereitstellen, erfolgt asynchron in einem Hintergrund Thread durch DXCore, wenn das erkannte Ereignis auftritt. Es erfolgt keine Garantie hinsichtlich der Reihenfolge oder der zeitlichen Steuerung &mdash; , in der mehrere Rückrufe in beliebiger Reihenfolge oder sogar gleichzeitig auftreten können. Es ist sogar möglich, dass ihr Rückruf aufgerufen wird, bevor **registereventnotification** abgeschlossen wurde. In diesem Fall gewährleistet DXCore, dass Ihr *eventcookie* festgelegt wird, bevor ihr Rückruf aufgerufen wird. Mehrere Rückrufe für eine bestimmte Registrierung werden in der angegebenen Reihenfolge serialisiert.

Rückrufe können jederzeit erfolgen, bis Sie [unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen und abgeschlossen sind. Rückrufe erfolgen in ihren eigenen Threads, und Sie können Aufrufe der DXCore-API für diese Threads ausführen, einschließlich **unregistereventnotification**. Allerdings darf der letzte Verweis auf das *dxcoreobject-Objekt* in diesem Thread nicht freigegeben werden.

> [!IMPORTANT]
> Bevor Sie das DXCore-Objekt zerstören, das durch das *dxcoreobject* -Argument dargestellt wird, das an **registereventnotification** übermittelt wird, müssen Sie den Cookie-Wert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen aufzuheben, indem Sie [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen. Wenn Sie dies nicht tun, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)