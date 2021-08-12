---
title: IDXCoreAdapter::IsPropertySupported
description: Bestimmt, ob dieses DXCore-Adapterobjekt und das aktuelle Betriebssystem die angegebene Adaptereigenschaft unterstützen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ddee6bea5af8fb64dfa2bfc15392e92239e7326b34cbd93cbd112559a6027912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279231"
---
# <a name="idxcoreadapterispropertysupported-method"></a>IDXCoreAdapter::IsPropertySupported-Methode

Bestimmt, ob dieses DXCore-Adapterobjekt und das aktuelle Betriebssystem die angegebene Adaptereigenschaft unterstützen.

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="property"></a>property

Typ: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Der Typ der Eigenschaft, für die Sie die Unterstützung abfragen. Weitere Informationen zu den einzelnen Adaptereigenschaften finden Sie in der Tabelle in [DXCoreAdapterProperty.](./ne-dxcore_interface-dxcoreadapterproperty.md)

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt `true` zurück, wenn dieses DXCore-Adapterobjekt und das aktuelle Betriebssystem die angegebene Adaptereigenschaft unterstützen. Andernfalls wird `false`zurückgegeben.

## <a name="see-also"></a>Siehe auch

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapterattribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)