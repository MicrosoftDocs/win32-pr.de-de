---
title: DXCoreNotificationType
description: Definiert Konstanten, die Typen von Benachrichtigungen angeben, die von [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -oder [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Objekten ausgelöst werden.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3eacd77d2cf15c78a0dc959285874de943fd9130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101811"
---
# <a name="dxcorenotificationtype-enum"></a>Dxcorenotificationtype-Aufzählung

Definiert Konstanten, die Typen von Benachrichtigungen angeben, die von [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -oder [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Objekten ausgelöst werden.

Sie können sich für diese Benachrichtigungen registrieren und die Registrierung aufheben, indem Sie [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) bzw. [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)aufrufen.

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

### <a name="adapterliststale"></a>Adapterliststale

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">idxcoreadapterlist</a> -Objekt ausgelöst, wenn die Adapter Liste veraltet ist. Der aktuellste Übergang ist unidirektional und einmal, sodass diese Benachrichtigung höchstens einmal ausgelöst wird.

### <a name="adapternolongervalid"></a>Adapternolongervalid

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">idxcoreadapter</a> -Objekt ausgelöst, wenn der Adapter nicht mehr gültig wird. Der gültige-bis-ungültige Übergang ist unidirektional und einmalig, sodass diese Benachrichtigung höchstens einmal ausgelöst wird.

### <a name="adapterbudgetchange"></a>Adapterbudgetchange

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">idxcoreadapter</a> -Objekt ausgelöst, wenn ein Adapter Budget geändert wird. Diese Benachrichtigung kann mehrmals auftreten. Die Verwendung dieser Benachrichtigung ähnelt der Funktionsweise von <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3:: registervideomemorybudgetchangenotificationevent</a>. Als Reaktion auf dieses Ereignis sollte [idxcoreadapter:: querystate](./nf-dxcore_interface-idxcoreadapter-querystate.md) (mit [dxcoreadapterstate:: adaptermemorybudget](./ne-dxcore_interface-dxcoreadapterstate.md)) aufgerufen werden, um den aktuellen Arbeitsspeicher-Budget Status auszuwerten.

### <a name="adapterhardwarecontentprotectionteardown"></a>Adapterhardwarecontentschutzteardown

Diese Benachrichtigung wird von einem <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">idxcoreadapter</a> -Objekt ausgelöst, um über den Hardware Content Protection-Löschvorgang eines Adapters zu benachrichtigen. Diese Benachrichtigung kann mehrmals auftreten. Es ist funktionell vergleichbar mit <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3:: registerhardwarecontentschützteardownstatus usevent</a>. Als Reaktion auf dieses Ereignis sollten Sie den aktuellen Status der Kryptografiesitzung neu auswerten. beispielsweise durch Aufrufen von [ID3D11VideoContext1:: checkcryptosessionstatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) , um die Auswirkung der Hardware Löschung für eine bestimmte [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) -Schnittstelle zu bestimmen.

## <a name="see-also"></a>Siehe auch

[Idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [using DXCore to auflisten Adapters](../dxcore-enum-adapters.md)