---
title: IDXCoreAdapter::IsSetStateSupported
description: Bestimmt, ob dieses DXCore-Adapterobjekt und das aktuelle Betriebssystem das Festlegen des Werts des angegebenen Adapterzustands unterstützen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: dc63b541a552f1b01792e9f503acc7aeee03ce5ac6cc92e7b70e271ae62a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278978"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>IDXCoreAdapter::IsSetStateSupported-Methode

Bestimmt, ob dieses DXCore-Adapterobjekt und das aktuelle Betriebssystem das Festlegen des Werts des angegebenen Adapterzustands unterstützen.

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="state"></a>state

Typ: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Die Art des Zustandselements, für das Sie die Unterstützung abfragen. Weitere Informationen zu den einzelnen Adapterzustandsarten finden Sie in der Tabelle in [DXCoreAdapterState.](./ne-dxcore_interface-dxcoreadapterstate.md)

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt `true` zurück, wenn dieses DXCore-Adapterobjekt und das aktuelle Betriebssystem das Festlegen des angegebenen Adapterzustands unterstützen. Andernfalls wird `false`zurückgegeben.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapterattribut-GUIDs](../dxcore-adapter-attribute-guids.md), Verwenden von DXCore zum [Aufzählen von Adaptern](../dxcore-enum-adapters.md)