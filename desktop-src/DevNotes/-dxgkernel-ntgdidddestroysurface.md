---
description: Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Ntgdidddestroysurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041427"
---
# <a name="ntgdidddestroysurface-function"></a>Ntgdidddestroysurface-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Zerstört ein zuvor zugewiesenes Microsoft DirectDraw Surface-Objekt im Kernel Modus.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsurface* \[ in\]
</dt> <dd>

Handle für das zuvor zugewiesene kernelmodusetobjekt.

</dd> <dt>

*brealdestroy* \[ in\]
</dt> <dd>

Gibt an, wie die-Oberfläche zerstört werden soll. Kann einen der folgenden Werte aufweisen.

<dt>



 Fall


</dt> <dd>

Zerstören der Oberfläche und kostenlosen Video Arbeitsspeichers.

</dd> <dt>



 Alarm


</dt> <dd>

Geben Sie den Videospeicher frei, aber lassen Sie die Oberfläche in einem nicht initialisierten Zustand.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdidddestroysurface** gibt einen der folgenden Rückruf Codes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ddhal- \_ Treiber \_ behandelt**</dt> </dl>    | Der Treiber hat den Vorgang durchgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, fährt DirectDraw oder Direct3D mit der-Funktion fort. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**ddhal- \_ Treiber \_ nothandled**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementieren muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls behandelt DirectDraw oder Direct3D den Vorgang so, als ob der Treiber Rückruf nicht durch Ausführen der geräteunabhängigen DirectDraw-oder Direct3D-Implementierung definiert wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Es wird empfohlen, dass Anwendungen die DirectDraw-und Direct3D-APIs verwenden, um Oberflächen anstelle dieser Funktion zu erstellen und zu zerstören.

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

 

 




