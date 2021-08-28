---
title: DXCoreNotificationType
description: Definiert Konstanten, die Typen von Benachrichtigungen angeben, die von [IDXCoreAdapter-](./nn-dxcore_interface-idxcoreadapter.md) oder [IDXCoreAdapterList-Objekten](./nn-dxcore_interface-idxcoreadapterlist.md) ausgelöst werden.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 230b6c103f83e72dfe0ba7803cde4b4695a32de724ce44c1aaccf5131d077bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726010"
---
# <a name="dxcorenotificationtype-enum"></a>DXCoreNotificationType-Enumeration

Definiert Konstanten, die Typen von Benachrichtigungen angeben, die von [IDXCoreAdapter-](./nn-dxcore_interface-idxcoreadapter.md) oder [IDXCoreAdapterList-Objekten](./nn-dxcore_interface-idxcoreadapterlist.md) ausgelöst werden.

Sie können die Registrierung für diese Benachrichtigungen aufheben, indem Sie [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) bzw. [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Konstanten

### <a name="adapterliststale"></a>AdapterList State

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList-Objekt</a> ausgelöst, wenn die Adapterliste veraltet ist. Der Übergang vom aktuellen zum veralteten Zeitpunkt erfolgt einmalig und einmalig, sodass diese Benachrichtigung höchstens einmal ausgelöst wird.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter-Objekt</a> ausgelöst, wenn der Adapter nicht mehr gültig ist. Der Übergang von "Valid-to-Invalid" erfolgt in einer Richtung und einmal, sodass diese Benachrichtigung höchstens einmal ausgelöst wird.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter-Objekt</a> ausgelöst, wenn eine Adapterbudgetänderung auftritt. Diese Benachrichtigung kann mehrmals auftreten. Die Verwendung dieser Benachrichtigung ähnelt funktional <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent</a>. Als Reaktion auf dieses Ereignis sollten Sie [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (mit [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) aufrufen, um den aktuellen Speicherbudgetstatus auszuwerten.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter-Objekt</a> ausgelöst, um den Hardwareinhaltsschutz eines Adapters zu benachrichtigen. Diese Benachrichtigung kann mehrmals auftreten. Es ist funktional ähnlich wie <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a>. Als Reaktion auf dieses Ereignis sollten Sie den aktuellen Status der Kryptositzung neu auswerten. Beispielsweise durch Aufrufen von [ID3D11VideoContext1::CheckCryptoSessionStatus,](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) um die Auswirkungen der Hardwareentschlüsselung für eine bestimmte [ID3D11CryptoSession-Schnittstelle](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) zu bestimmen.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)