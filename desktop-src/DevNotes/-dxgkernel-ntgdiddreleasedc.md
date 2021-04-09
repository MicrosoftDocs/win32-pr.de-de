---
description: Gibt den zuvor erstellten Gerätekontext (DC) für den angezeigten Kernel Modus-Microsoft DirectDraw Surface-Objekt frei.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Ntgdiddreleasedc-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a7319b423f12d7e4415d78d995bfb1d7cd0341a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860624"
---
# <a name="ntgdiddreleasedc-function"></a>Ntgdiddreleasedc-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Gibt den zuvor erstellten Gerätekontext (DC) für den angezeigten Kernel Modus-Microsoft DirectDraw Surface-Objekt frei.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsurface* \[ in\]
</dt> <dd>

Handle für das zuvor erstellte Kernel Modus-DirectDraw-Oberflächen Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen, die einen Domänen Controller für eine DirectDraw-Oberfläche benötigen, können [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc)verwenden, die diese Funktionalität auf eine Weise unabhängig vom Betriebssystem verfügbar macht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der untergeordneten Grafik Ebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**Ddreleasedc**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
