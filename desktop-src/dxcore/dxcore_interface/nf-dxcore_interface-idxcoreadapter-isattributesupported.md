---
title: IDXCoreAdapter::IsAttributeSupported
description: Bestimmt, ob dieses DXCore-Adapter Objekt das angegebene Adapter Attribut unterstützt.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390461"
---
# <a name="idxcoreadapterisattributesupported-method"></a>Idxcoreadapter:: isattributesupportiert-Methode

Bestimmt, ob dieses DXCore-Adapter Objekt das angegebene Adapter Attribut unterstützt.

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="attributeguid"></a>attributeguid

Typ: **reguid**

Ein Verweis auf eine GUID des Adapter Attributs. Eine Liste der Attribut-GUIDs finden Sie unter [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt das angegebene Adapter Attribut unterstützt. Andernfalls wird zurückgegeben  `false` .

## <a name="see-also"></a>Siehe auch

[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)