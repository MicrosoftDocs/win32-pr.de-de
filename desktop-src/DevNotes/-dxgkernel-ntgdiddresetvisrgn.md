---
description: Wird verwendet, um den Benutzermodus zu aktivieren, um ein gültiges Verständnis des Ausschneidebereichs für Fenster auf dem Desktop zu erhalten. Diese Beschneidung kann sich aus Der Sicht von Benutzermodusthreads asynchron ändern.
ms.assetid: 286f1c06-c27b-42bd-aecc-3a6923e3df29
title: NtGdiDdResetVisrgn-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 3077351b804f854520cff421fcad8a575278bb5a960f60ef760db38e7ca2f3a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833640"
---
# <a name="ntgdiddresetvisrgn-function"></a>NtGdiDdResetVisrgn-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. Diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Wird verwendet, um den Benutzermodus zu aktivieren, um ein gültiges Verständnis des Ausschneidebereichs für Fenster auf dem Desktop zu erhalten. Diese Beschneidung kann sich aus Der Sicht von Benutzermodusthreads asynchron ändern.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdResetVisrgn(
  _In_ HANDLE hSurface,
  _In_ HWND   hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurface* \[ In\]
</dt> <dd>

Zeiger auf das Benutzermodusobjekt einer beliebigen Oberfläche, die zum DirectDraw-Gerät gehört, für das clipping zurückgesetzt werden soll. Weitere Informationen finden Sie in der DDK-Dokumentation.

</dd> <dt>

*hwnd* \[ In\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dies erfolgreich ist, gibt diese Funktion **TRUE zurück.** Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

Das Ausschneiden kann sich aus Der Sicht von Threads im Benutzermodus asynchron ändern. Die Kernelmodusteile von DirectDraw und Windows Graphics Device Interface (GDI) verwalten einen Leistungsindikator, der erhöht wird, wenn sich die Clippingliste für den gesamten Desktop ändert. Ein Aufruf dieser Funktion zeichnet diesen Indikator mit jeder vorhandenen primären DirectDraw-Oberfläche auf dem System auf.

Zu einem späteren Zeitpunkt, wenn eine dieser primären Oberflächen durch einen [IDirectDrawSurface7::Blt-](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-blt) oder [IDirectDrawSurface7::Lock-Vorgang](/previous-versions/ms858221(v=msdn.10)) geändert wird (siehe DDK-Dokumentation), wird der mit der Oberfläche aufgezeichnete Zähler mit dem globalen Zähler verglichen. Wenn diese Werte unterschiedlich sind, wird ein Fehlercode DDERR \_ VISRGNCHANGED an den Benutzermoduscode zurückgegeben. Der Benutzermoduscode fragen dann die aktuelle Beschneidung für den Desktop erneut ab, rufen **NtGdiDdResetVisrgn** auf und versuchen erneut, die auf die primäre Oberfläche angewendete IDirectDrawSurface7::Blt unter Einhaltung der neuen Beschneidung zu testen. Schließlich ist der Clipping, der vom Benutzermoduscode entnommen wurde, mit dem aktuellen Clipping im Besitz des Kernelmodus identisch, und IDirectDrawSurface7::Blt kann fortgesetzt werden.

Anwendungen wird empfohlen, die [IDirectDrawClipper-Schnittstelle](/previous-versions/aa919448(v=msdn.10)) oder [die IDirect3DDevice8::P resent-Methode](/previous-versions/ms889707(v=msdn.10)) zu verwenden, um asynchrone Clippingänderungen zu verarbeiten. Diese Konstrukte implementieren asynchrones Clipping auf automatisierte und betriebssystemunabhängige Weise.

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

[**DdResetVisrgn**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddresetvisrgn)
</dt> </dl>

 

 
