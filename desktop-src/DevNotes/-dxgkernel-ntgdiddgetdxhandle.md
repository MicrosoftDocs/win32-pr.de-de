---
description: Gibt den Kernel Modus-Microsoft DirectX-API-Handle zurück, der bei nachfolgenden Aufrufen der kernelmoduseinstiegs Punkte verwendet werden soll, die den DirectX-API-Mechanismus steuern.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Ntgdiddgetdxhandle-Funktion (ntgdi. h)
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
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342765"
---
# <a name="ntgdiddgetdxhandle-function"></a>Ntgdiddgetdxhandle-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Gibt den Kernel Modus-Microsoft DirectX-API-Handle zurück, der bei nachfolgenden Aufrufen der kernelmoduseinstiegs Punkte verwendet werden soll, die den DirectX-API-Mechanismus steuern.

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

*hdirectdraw* \[ in\]
</dt> <dd>

Handle für das DirectDraw-Objekt, das die Oberfläche besitzt. Dieser Parameter ist optional und kann auf **null** festgelegt werden.

</dd> <dt>

*hsurface* \[ in\]
</dt> <dd>

Handle für die Oberfläche, für die ein DirectX-API-Handle im Kernel Modus zurückgegeben werden soll. Dieser Parameter ist optional und kann auf **null** festgelegt werden.

</dd> <dt>

*brelease* \[ in\]
</dt> <dd>

Legen Sie diese Einstellung auf " **true** " fest, wenn die DirectX API-kernelmodusschnittstelle Andernfalls **false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein DirectX-API-handle, das in nachfolgenden DirectX-API-orientierten Kernel Einstiegspunkten verwendet wird.

## <a name="remarks"></a>Bemerkungen

Wenn sowohl *hdirectdraw* als auch *hsurface* angegeben werden, wird *hsurface* ignoriert.

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

 

 




