---
description: Gibt den zuvor erstellten Gerätekontext (DC) für das angegebene Microsoft DirectDraw-Oberflächenobjekt im Kernelmodus frei.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: NtGdiDdReleaseDC-Funktion (Ntgdi.h)
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
ms.openlocfilehash: daa4cad2f6f3937ebe29b3996ebbaa72b894ee743f97222cb1f6e2ff61f7dbb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824910"
---
# <a name="ntgdiddreleasedc-function"></a>NtGdiDdReleaseDC-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Gibt den zuvor erstellten Gerätekontext (DC) für das angegebene Microsoft DirectDraw-Oberflächenobjekt im Kernelmodus frei.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für das zuvor erstellte DirectDraw-Oberflächenobjekt im Kernelmodus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dies erfolgreich ist, gibt diese Funktion **TRUE zurück.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Anwendungen, die einen DC für eine DirectDraw-Oberfläche abrufen müssen, können [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc)verwenden, wodurch diese Funktionalität unabhängig vom Betriebssystem verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientunterstützung auf niedriger Grafikebene](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReleaseDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
