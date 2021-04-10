---
description: Legt die Gamma-Rampe für das Gerät fest.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Ntgdiddsetgammaramp-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125930"
---
# <a name="ntgdiddsetgammaramp-function"></a>Ntgdiddsetgammaramp-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Legt die Gamma-Rampe für das Gerät fest.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdraw* \[ in\]
</dt> <dd>

Handle für das Kernel Modus-Treiber Objekt, für das die Rampe festgelegt werden soll.

</dd> <dt>

*hdc* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*lpgammaramp* \[ in\]
</dt> <dd>

Zeiger auf ein Array von **ddgammaramp** -Strukturen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist " **true** ", wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls ist der Wert **null**.

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Anwendungen stattdessen die **idirectdrawgammacontrol:: setgammaramp** -oder [**IDirect3DDevice9:: setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) -Methoden verwenden, da diese Methoden unabhängig vom Betriebssystem die gleiche Funktionalität bieten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
