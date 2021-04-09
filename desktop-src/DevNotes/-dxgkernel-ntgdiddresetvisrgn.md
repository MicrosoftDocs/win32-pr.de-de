---
description: Wird verwendet, um den Benutzermodus zu aktivieren, um ein gültiges Verständnis des Clippingbereichs für Windows auf dem Desktop zu erhalten. Dieses Clipping kann sich asynchron aus der Sicht der benutzermodusthreads ändern.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: Ntgdiddresetvisrgn-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdResetVisrgn
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dd83bcfd6c1f3dec31fb80cf78750bfdfef5e7a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860622"
---
# <a name="ntgdiddresetvisrgn-function"></a>Ntgdiddresetvisrgn-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Wird verwendet, um den Benutzermodus zu aktivieren, um ein gültiges Verständnis des Clippingbereichs für Windows auf dem Desktop zu erhalten. Dieses Clipping kann sich asynchron aus der Sicht der benutzermodusthreads ändern.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsurface* \[ in\]
</dt> <dd>

Zeiger auf das benutzermodusobjekt einer beliebigen Oberfläche, die zu dem DirectDraw-Gerät gehört, für das Clipping zurückgesetzt werden soll. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*HWND* \[ in\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, gibt diese Funktion **true** zurück. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Clipping kann sich asynchron von der Sicht der benutzermodusthreads aus ändern. Die kernelmodusteile von DirectDraw und Windows Graphics Device Interface (GDI) behalten einen-Wert bei, der immer dann erhöht wird, wenn sich die clippingliste für den gesamten Desktop ändert. Durch einen Aufrufen dieser Funktion wird dieser Counter mit jeder vorhandenen primären DirectDraw-Oberfläche auf dem System aufgezeichnet.

Wenn eine dieser primären Oberflächen zu einem späteren Zeitpunkt durch einen [IDirectDrawSurface7:: BLT](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) -oder [IDirectDrawSurface7:: Lock](/previous-versions/ms858221(v=msdn.10)) -Vorgang geändert wird (siehe DDK-Dokumentation), wird der mit der-Oberfläche aufgezeichnete-Wert mit dem globalen-Wert verglichen. Wenn diese Werte unterschiedlich sind, wird ein Fehlercode dderr \_ visrgnchanged an den Benutzermoduscode zurückgegeben. Der Benutzermoduscode fragt dann das aktuelle Clipping für den Desktop erneut ab, ruft **ntgdiddresetvisrgn** auf und wiederholt den auf die primäre Oberfläche angewendeten IDirectDrawSurface7:: BLT, wobei das neue Clipping respektiert wird. Schließlich ist das Clipping, das durch den Benutzermoduscode entnommen wurde, mit dem aktuellen Clipping im Besitz des Kernel Modus identisch, und IDirectDrawSurface7:: BLT kann fortgesetzt werden.

Anwendungen wird empfohlen, die [idirectdrawclipperschnittstelle](/previous-versions/aa919448(v=msdn.10)) oder die [IDirect3DDevice8::P Resent](/previous-versions/ms889707(v=msdn.10)) -Methode zu verwenden, um asynchrone clippingänderungen zu verarbeiten. Diese Konstrukte implementieren ein asynchrones Clipping in automatisierter und Betriebssystem unabhängiger Weise.

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

[**Ddresetvisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
