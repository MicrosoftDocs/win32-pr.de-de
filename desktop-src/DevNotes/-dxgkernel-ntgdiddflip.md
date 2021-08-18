---
description: Bewirkt, dass der dem Ziel zugeordnete Oberflächenspeicher und die aktuellen Oberflächen ausgetauscht werden.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: NtGdiDdFlip-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 18113c841c22b31c9768d42491a63ead8cafee3c3b598bc46f442068592e67b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956489"
---
# <a name="ntgdiddflip-function"></a>NtGdiDdFlip-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Bewirkt, dass der dem Ziel zugeordnete Oberflächenspeicher und die aktuellen Oberflächen ausgetauscht werden.

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

*hSurfaceCurrent* \[ In\]
</dt> <dd>

Handle für die [DD \_ SURFACE \_ LOCAL-Struktur,](https://msdn.microsoft.com/library/ms793861.aspx) die die aktuelle Oberfläche beschreibt.

</dd> <dt>

*hSurfaceTarget* \[ In\]
</dt> <dd>

Handle für die [DD \_ SURFACE \_ LOCAL-Struktur,](https://msdn.microsoft.com/library/ms793861.aspx) die die Zieloberfläche beschreibt, d. h. die Oberfläche, auf die sich der Treiber drehen soll.

</dd> <dt>

*hSurfaceCurrentLeft* \[ In\]
</dt> <dd>

Handle für die [DD \_ SURFACE \_ LOCAL-Struktur,](https://msdn.microsoft.com/library/ms793861.aspx) die die aktuelle linke Oberfläche beschreibt.

</dd> <dt>

*hSurfaceTargetLeft* \[ In\]
</dt> <dd>

Handle für die [DD \_ SURFACE \_ LOCAL-Struktur,](https://msdn.microsoft.com/library/ms793861.aspx) die die linke Zieloberfläche beschreibt, auf die gekippt werden soll.

</dd> <dt>

*puFlipData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [ \_ DD-FLIPDATA-Struktur,](https://msdn.microsoft.com/library/ms794213.aspx) die die informationen enthält, die zum Ausführen des Flips erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdFlip** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

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

 

 




