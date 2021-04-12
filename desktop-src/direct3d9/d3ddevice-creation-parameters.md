---
description: Beschreibt die Erstellungs Parameter für ein Gerät.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: D3DDEVICE_CREATION_PARAMETERS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354476"
---
# <a name="d3ddevice_creation_parameters-structure"></a>Struktur der D3DDEVICE- \_ Erstellungs \_ Parameter

Beschreibt die Erstellungs Parameter für ein Gerät.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a>Member

<dl> <dt>

**AdapterOrdinal**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Ordinalzahl, die den Anzeige Adapter bezeichnet. D3DADAPTER \_ der Standardwert ist immer der primäre Anzeige Adapter. Verwenden Sie diese Ordinalzahl als Adapter Parameter für jede der [**IDirect3D9**](/windows/desktop/api) -Methoden. Beachten Sie, dass verschiedene Instanzen von Direct3D 9,0-Objekten unterschiedliche ordinale verwenden können. Adapter können ein System eingeben oder verlassen, wenn Benutzer z. b. Monitore von einem System mit mehreren Monitoren hinzufügen oder entfernen oder wenn Sie einen Laptop mit einem anderen Laptop austauschen. Folglich sollten Sie diese Ordinalzahl nur in einer Direct3D 9,0-Instanz verwenden, die bekanntermaßen gültig ist, d. h. entweder den Direct3D 9,0, der diese [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle erstellt hat, oder Direct3D 9,0, der von [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d)zurückgegeben wurde, wie durch diese **IDirect3DDevice9** -Schnittstelle

</dd> <dt>

**DeviceType**
</dt> <dd>

Typ: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Member des [**D3DDEVTYPE**](./d3ddevtype.md) -Enumerationstyps. Gibt den Umfang der emulierten Funktionen für dieses Gerät an. Der Wert dieses Parameters spiegelt den Wert wider, der an den aufzurufenden Befehl "up- [**Device**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " übergeben wurde.

</dd> <dt>

**hfocus Window**
</dt> <dd>

Typ: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Fenster Handle, zu dem der Fokus für dieses Direct3D-Gerät gehört. Der Wert dieses Parameters spiegelt den Wert wider, der an den aufzurufenden Befehl "up- [**Device**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " übergeben wurde.

</dd> <dt>

**Verhaltflags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Eine Kombination aus einer oder mehreren [D3DCREATE](d3dcreate.md) -Konstanten, die das globale Verhalten des Geräts steuern. Diese Konstanten spiegeln die Konstanten wider, die beim Erstellen des Geräts an " [**kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " übergeben wurden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getkreationparameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**"Kreatedevice"**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
