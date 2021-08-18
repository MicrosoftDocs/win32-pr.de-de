---
description: Beschreibt die Erstellungsparameter für ein Gerät.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: D3DDEVICE_CREATION_PARAMETERS -Struktur (D3D9Types.h)
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
ms.openlocfilehash: 64b3e13300d6c305d06b6b13db246134cb889cbfc407e4a99c6ae45adbf916e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805019"
---
# <a name="d3ddevice_creation_parameters-structure"></a>D3DDEVICE \_ CREATION \_ PARAMETERS-Struktur

Beschreibt die Erstellungsparameter für ein Gerät.

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

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ordinalzahl, die den Adapter kennzeichnet. D3DADAPTER \_ DEFAULT ist immer der primäre Anzeigeadapter. Verwenden Sie diese Ordnungszahl als Adapter-Parameter für eine der [**IDirect3D9-Methoden.**](/windows/desktop/api) Beachten Sie, dass verschiedene Instanzen von Direct3D 9.0-Objekten unterschiedliche Ordinalzahlen verwenden können. Adapter können ein System ein- oder verlassen, wenn Benutzer z. B. Monitore zu einem System mit mehreren Monitoren hinzufügen oder daraus entfernen oder wenn sie einen Laptop austauschen. Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.

</dd> <dt>

**DeviceType**
</dt> <dd>

Typ: **[ **D3DDEVTYPE**](./d3ddevtype.md)**

</dd> <dd>

Member des [**aufzählten D3DDEVTYPE-Typs.**](./d3ddevtype.md) Gibt die Menge der emulierten Funktionen für dieses Gerät an. Der Wert dieses Parameters spiegelt den Wert wieder, der an den [**CreateDevice-Aufruf**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) übergeben wurde, der dieses Gerät erstellt hat.

</dd> <dt>

**hFocusWindow**
</dt> <dd>

Typ: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Fensterhand handle, zu dem der Fokus für dieses Direct3D-Gerät gehört. Der Wert dieses Parameters spiegelt den Wert wieder, der an den [**CreateDevice-Aufruf**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) übergeben wurde, der dieses Gerät erstellt hat.

</dd> <dt>

**Behaviorflags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Eine Kombination aus mindestens einer [D3DCREATE-Konstante,](d3dcreate.md) die das globale Verhalten des Geräts steuern. Diese Konstanten spiegeln die Konstanten wieder, die beim Erstellen des Geräts an [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) übergeben wurden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetCreationParameters**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
