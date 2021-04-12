---
description: Startet die Decodierung eines neuen Frames.
ms.assetid: da2c231d-89a9-4fd9-99b5-f7c1309c26e0
title: Ntgdiddbeginmucompframe-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBeginMoCompFrame
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45c359092d1a161aae7671c437fdb9683a2a8eb9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523187"
---
# <a name="ntgdiddbeginmocompframe-function"></a>Ntgdiddbeginmucompframe-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Startet die Decodierung eines neuen Frames.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdBeginMoCompFrame(
  _In_    HANDLE                   hMoComp,
  _Inout_ PDD_BEGINMOCOMPFRAMEDATA puBeginFrameData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmucomp* \[ in\]
</dt> <dd>

Handle für eine [**\_ \_ lokale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) -Struktur, die eine Beschreibung der angeforderten Bewegungskompensation enthält.

</dd> <dt>

*pubeginframedata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ beginmucompframedata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_beginmocompframedata) -Struktur, die die Informationen enthält, die zum Starten der Decodierung eines neuen Frames benötigt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddbeginmucompframe** gibt einen der folgenden Rückruf Codes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ddhal- \_ Treiber \_ behandelt**</dt> </dl>    | Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**ddhal- \_ Treiber \_ nothandled**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie im Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

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

 

 
