---
description: Legt die Gamma-Rampe für das Gerät fest.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: NtGdiDdSetGammaRamp-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 78e68a76fed6db78a2f3d247c5bec1b73f3df3b6fe204e0d09b1bc5f14a014b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668809"
---
# <a name="ntgdiddsetgammaramp-function"></a>NtGdiDdSetGammaRamp-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

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

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für das Kernelmodustreiberobjekt, für das die Rampe festgelegt werden soll.

</dd> <dt>

*hdc* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*lpGammaRamp* \[ In\]
</dt> <dd>

Zeiger auf ein Array von **DDGAMMARAMP-Strukturen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **TRUE,** wenn die Funktion erfolgreich ist. Andernfalls ist es **NULL.**

## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Anwendungen stattdessen die Methoden **IDirectDrawGammaControl::SetGammaRamp** oder [**IDirect3DDevice9::SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) verwenden, da diese Methoden unabhängig vom Betriebssystem die gleiche Funktionalität bieten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
