---
title: IDXCoreAdapter::IsPropertySupported
description: Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem (OS) die angegebene Adapter Eigenschaft unterstützen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338675"
---
# <a name="idxcoreadapterispropertysupported-method"></a>Idxcoreadapter:: ispropertysupported-Methode

Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem (OS) die angegebene Adapter Eigenschaft unterstützen.

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="property"></a>property

Type: **[dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Der Typ der Eigenschaft, die Sie für die Unterstützung von Abfragen. Weitere Informationen zu den einzelnen Adapter Eigenschaften finden Sie in der Tabelle unter [dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem (OS) die angegebene Adapter Eigenschaft unterstützen. Andernfalls wird zurückgegeben  `false` .

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)