---
title: IDXCoreAdapter::IsQueryStateSupported
description: Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem die Abfrage des Werts des angegebenen Adapter Zustands unterstützen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102042"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>Idxcoreadapter:: isquerystaatupportiert-Methode

Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem die Abfrage des Werts des angegebenen Adapter Zustands unterstützen.

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="state"></a>state

Typ: **[dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md)**

Die Art des Zustands Elements, das Sie für die Unterstützung von Abfragen. Weitere Informationen zu den einzelnen adapterstatusarten finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem die Abfrage des angegebenen Adapter Zustands unterstützen. Andernfalls wird zurückgegeben  `false` .

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)