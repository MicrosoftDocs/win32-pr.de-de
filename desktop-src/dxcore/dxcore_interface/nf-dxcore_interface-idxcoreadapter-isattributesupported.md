---
title: IDXCoreAdapter::IsAttributeSupported
description: Bestimmt, ob dieses DXCore-Adapterobjekt das angegebene Adapterattribut unterstützt.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787080"
---
# <a name="idxcoreadapterisattributesupported-method"></a>IDXCoreAdapter::IsAttributeSupported-Methode

Bestimmt, ob dieses DXCore-Adapterobjekt das angegebene Adapterattribut unterstützt.

## <a name="syntax"></a>Syntax

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parameter

### <a name="attributeguid"></a>attributeGUID

Typ: **REFGUID**

Ein Verweis auf eine Adapterattribut-GUID. Eine Liste der Attribut-GUIDs finden Sie unter [DXCore-Adapterattribut-GUIDs](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Gibt zurück

Typ: **bool**

Gibt `true` zurück, wenn dieses DXCore-Adapterobjekt das angegebene Adapterattribut unterstützt. Andernfalls wird `false`zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapterattribut-GUIDs](../dxcore-adapter-attribute-guids.md), Verwenden von DXCore zum [Aufzählen von Adaptern](../dxcore-enum-adapters.md)