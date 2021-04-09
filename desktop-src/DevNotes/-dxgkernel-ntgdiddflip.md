---
description: Bewirkt, dass der mit dem Ziel und den aktuellen Oberflächen verknüpfte Oberflächen Speicher geändert wird.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Ntgdiddflip-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861096"
---
# <a name="ntgdiddflip-function"></a>Ntgdiddflip-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Bewirkt, dass der mit dem Ziel und den aktuellen Oberflächen verknüpfte Oberflächen Speicher geändert wird.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsurfakecurrent* \[ in\]
</dt> <dd>

Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die aktuelle Oberfläche beschreibt.

</dd> <dt>

*hsurfaketarget* \[ in\]
</dt> <dd>

Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die Ziel Oberfläche beschreibt, d. h. die Oberfläche, auf die der Treiber kippen soll.

</dd> <dt>

*hsurfakecurrentleft* \[ in\]
</dt> <dd>

Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die aktuelle linke Oberfläche beschreibt.

</dd> <dt>

*hsurfaketargetleft* \[ in\]
</dt> <dd>

Handle für die [ \_ \_ lokale DD-Oberflächen](https://msdn.microsoft.com/library/ms793861.aspx) Struktur, die die linke Ziel Oberfläche beschreibt, zu der gewechselt werden soll.

</dd> <dt>

*puflipdata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [DD- \_ flipdata](https://msdn.microsoft.com/library/ms794213.aspx) -Struktur, die die zum Ausführen des kippen erforderlichen Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddflip** gibt einen der folgenden Rückruf Codes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ddhal- \_ Treiber \_ behandelt**</dt> </dl>    | Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**ddhal- \_ Treiber \_ nothandled**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.<br/> |



 

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

 

 




