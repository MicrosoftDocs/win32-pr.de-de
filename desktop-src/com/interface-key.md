---
title: Schnittstellenschlüssel
description: Registriert neue Schnittstellen durch Zuordnen eines Schnittstellennamens zu einer Schnittstellen-ID (IID). Es muss einen IID-Unterschlüssel für jede neue Schnittstelle geben.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Schnittstellenregistrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda0cc29331521025a9274dca7b85080be2ddd5a9b631d2660eadaa13fe4941a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048148"
---
# <a name="interface-key"></a>Schnittstellenschlüssel

Registriert neue Schnittstellen durch Zuordnen eines Schnittstellennamens zu einer Schnittstellen-ID (IID). Es muss einen IID-Unterschlüssel für jede neue Schnittstelle geben.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE SOFTWARE Classes \\ \\ \\ Interface** \\ *{* IID *}*



| Registrierungswert                               | Beschreibung                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifiziert die Schnittstelle, von der die aktuelle Schnittstelle abgeleitet wird.                                  |
| [**NumMethods**](nummethods.md)             | Enthält die Anzahl der Methoden in der zugeordneten Schnittstelle, einschließlich Methoden von abgeleiteten Schnittstellen. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Karten einer IID zu einer CLSID in 16-Bit-Proxy-DLLs.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Karten einer IID in 32-Bit-Proxy-DLLs auf eine CLSID.                                                           |



 

## <a name="remarks"></a>Hinweise

Der **Schlüssel HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** entspricht dem **HKEY CLASSES \_ \_ ROOT-Schlüssel,** der aus Kompatibilitäts- mit früheren Versionen von COM beibehalten wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schnittstelle**](interface.md)
</dt> </dl>

 

 




