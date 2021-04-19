---
description: Fügt zwei Oberflächen Darstellungen im Kernel Modus an.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Ntgdiddattachsurface-Funktion (ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346626"
---
# <a name="ntgdiddattachsurface-function"></a>Ntgdiddattachsurface-Funktion

\[Diese Funktion kann bei jeder Betriebssystem Revision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs; Diese APIs isolieren Anwendungen vor solchen Betriebssystem Änderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeige Treibern.\]

Fügt zwei Oberflächen Darstellungen im Kernel Modus an.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsurfacefrom* \[ in\]
</dt> <dd>

Handle für das kernelmodusobjekt, das als Ausgangspunkt der neuen Anlage verwendet wird.

</dd> <dt>

*hsurfaceto* \[ in\]
</dt> <dd>

Handle für das kernelmodusobjekt, das der Endpunkt der neuen Anlage ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Ntgdiddattachsurface** gibt eine der folgenden Elemente zurück:



| Rückgabecode                                                                          | Beschreibung                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Der Funktions Aufrufvorgang war erfolgreich.<br/> |
| <dl> <dt>**Alarm**</dt> </dl> | Fehler beim Funktions Aufruf.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Eine vollständige Beschreibung der oberflächenanlagen finden Sie unter DirectDraw Software Development Kit (SDK) und Driver Development Kit (DDK).

> [!Note]  
> Wie bei anderen oberflächenanlagen ist die resultierende Anlage unidirektional. Nachdem diese Funktion aufgerufen wurde, wird *hsurfaceto* nicht an *hsurfacefrom* angefügt.

 

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

 

 




