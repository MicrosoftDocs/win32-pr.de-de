---
description: Benachrichtigt den Treiber, dass ein Software Decoder mit der Verwendung der Motion-Kompensierung mit der angegebenen GUID beginnt.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: Ntgdiddkreatemocomp-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126632"
---
# <a name="ntgdiddcreatemocomp-function"></a>Ntgdiddkreatemocomp-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Benachrichtigt den Treiber, dass ein Software Decoder mit der Verwendung der Motion-Kompensierung mit der angegebenen GUID beginnt.

## <a name="syntax"></a>Syntax


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdirectdraw* \[ in\]
</dt> <dd>

Handle für ein zuvor erstelltes DirectDraw-kernelmodusobjekt für das Gerät, für das die Motion-Kompensierung verwendet werden soll.

</dd> <dt>

*pukreatemocompdata* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine DD-Struktur [**\_ emocompdata**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) , die die Informationen enthält, die für die Verwendung der Motion-Kompensierung erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddkreatemocomp** gibt einen der folgenden Rückruf Codes zurück.



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

 

 
