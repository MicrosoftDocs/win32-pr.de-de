---
description: Ermöglicht es dem Treiber anzugeben, wie viele zwischen Flächen zur Unterstützung der angegebenen GUID erforderlich sind, sowie die Größe, den Speicherort und das Format der einzelnen Oberflächen.
ms.assetid: 1f3207a8-aa6a-47a3-a1d0-19166592eeca
title: Ntgdiddgetwcompbuffinfo-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompBuffInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03d471e62edd061ce167e0baf2051836e9634fae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041423"
---
# <a name="ntgdiddgetmocompbuffinfo-function"></a>Ntgdiddgetwcompbuffinfo-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Ermöglicht es dem Treiber anzugeben, wie viele zwischen Flächen zur Unterstützung der angegebenen GUID erforderlich sind, sowie die Größe, den Speicherort und das Format der einzelnen Oberflächen.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdGetMoCompBuffInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETMOCOMPCOMPBUFFDATA puGetBuffData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdraw* \[ in\]
</dt> <dd>

Handle für das zuvor erstellte Kernel Modus-DirectDraw-Objekt.

</dd> <dt>

*pugetbuffdata* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**DD \_ getmucompcompbuffdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) -Struktur, die die komprimierten Puffer Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddgetwcompbuffinfo** gibt einen der folgenden Rückruf Codes zurück.



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

 

 
