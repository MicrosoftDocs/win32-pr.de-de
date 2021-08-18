---
description: Gibt das Microsoft DirectX-API-Handle im Kernelmodus zurück, das in nachfolgenden Aufrufen der Einstiegspunkte im Kernelmodus verwendet werden soll, die den DirectX-API-Mechanismus steuern.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: NtGdiDdGetDxHandle-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 13234c7ebe350f096164f0a5de0bde7a60e819e80899aa87258a76727855b869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331920"
---
# <a name="ntgdiddgetdxhandle-function"></a>NtGdiDdGetDxHandle-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Gibt das Microsoft DirectX-API-Handle im Kernelmodus zurück, das in nachfolgenden Aufrufen der Einstiegspunkte im Kernelmodus verwendet werden soll, die den DirectX-API-Mechanismus steuern.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDirectDraw* \[ In\]
</dt> <dd>

Handle für directDraw-Objekt, das die Oberfläche besitzt. Dieser Parameter ist optional und kann auf NULL **festgelegt werden.**

</dd> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für die Oberfläche, für die ein DirectX-API-Handle im Kernelmodus zurückgeben werden soll. Dieser Parameter ist optional und kann auf NULL **festgelegt werden.**

</dd> <dt>

*bRelease* \[ In\]
</dt> <dd>

Legen Sie auf **TRUE** fest, wenn die Schnittstelle für den DirectX-API-Kernelmodus freigegeben werden soll. Andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein DirectX-API-Handle, das in nachfolgenden DirectX-API-orientierten Kerneleinstiegspunkten verwendet wird.

## <a name="remarks"></a>Hinweise

Wenn *sowohl hDirectDraw als* *auch hSurface* angegeben sind, *wird hSurface* ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




