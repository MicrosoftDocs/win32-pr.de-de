---
title: Behandeln von Fehlern und Entfernen von Geräten in der directml
description: In diesem Thema wird erläutert, wie Sie das Entfernen von Geräte-und anderen Fehlerzuständen in directml Debuggen.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548684"
---
# <a name="handling-errors-and-device-removal-in-directml"></a>Behandeln von Fehlern und Entfernen von Geräten in der directml

## <a name="device-removal"></a>Gerät-entfernen

Wenn ein nicht BEHEB barer Fehler auftritt, kann das directml-Gerät in den Zustand "Gerät entfernt" wechseln. Nicht BEHEB Bare Fehler, die das Entfernen von Geräten bewirken, beinhalten eine ungültige API-Verwendung (bei Methoden, die kein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)zurückgeben), Treiber Fehler, Hardwarefehler oder OOM-Bedingungen (Out-of-Memory).

Wenn ein directml-Gerät entfernt wird, werden alle Methodenaufrufe auf dem Gerät und alle von diesem Gerät erstellten Objekte. Bei Methoden, die ein [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)zurückgeben, wird ein [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) Fehlercode zurückgegeben. Sie können die [ **idmldevice:: getdeviceremovedreason** -Methode](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) verwenden, um zu überprüfen, ob das directml-Gerät entfernt wurde, und um einen ausführlicheren Fehlercode abzurufen.

Sie können keine Wiederherstellung von der Geräte Entfernung durchführt, außer indem Sie das betroffene Gerät und alle ihm untergeordneten Elemente freigeben und dann das directml-Gerät von Grund auf neu erstellen.

Wenn das zugrunde liegende Direct3D 12-Gerät entfernt wird, wird auch das directml-Gerät entfernt. Umgekehrt ist dies jedoch nicht möglich. Das Entfernen von directml-Geräten bewirkt möglicherweise nicht notwendigerweise, dass das zugrunde liegende Direct3D 12-Gerät entfernt wird.

## <a name="debugging-directml-device-removal-and-other-errors"></a>Debuggen der directml-Geräte Löschung und anderer Fehler

Die häufigste Ursache für directml-Fehler ist die ungültige API-Verwendung. Eine ungültige API-Verwendung kann zu einem **E_INVALIDARG** HRESULT-Fehlercode führen, oder es kann zu einem Geräte Entfernungs Vorgang führen.

Es wird dringend empfohlen, die [directml-debugschicht](dml-debug-layer.md) während der Entwicklung zu aktivieren, um solche Fehler zu erfassen und zu debuggen. Die directml-debugschicht führt eine umfassende Validierung von Methoden Parametern und API-Verwendung durch und gibt debugausgabenachrichten aus, die Sie beim Debuggen unterstützen

## <a name="see-also"></a>Siehe auch

* [Verwenden der directml-debugschicht](dml-debug-layer.md)
