---
description: Fügt zwei Oberflächendarstellungen im Kernelmodus an.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: NtGdiDdAttachSurface-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 8ec07f539cfa2a99338d8366f10f7c3d79dbdd5ef26a6de0ee0296941e2c84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088030"
---
# <a name="ntgdiddattachsurface-function"></a>NtGdiDdAttachSurface-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Fügt zwei Oberflächendarstellungen im Kernelmodus an.

## <a name="syntax"></a>Syntax


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurfaceFrom* \[ In\]
</dt> <dd>

Handle für das Kernelmodus-Oberflächenobjekt, das der Startpunkt der neuen Anlage ist.

</dd> <dt>

*hSurfaceTo* \[ In\]
</dt> <dd>

Handle für das Kernelmodus-Oberflächenobjekt, das der Endpunkt der neuen Anlage ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdAttachSurface** gibt eine der folgenden Angaben zurück:



| Rückgabecode                                                                          | Beschreibung                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>  | Der Funktionsaufruf war erfolgreich.<br/> |
| <dl> <dt>**FALSE**</dt> </dl> | Fehler beim Funktionsaufruf.<br/>    |



 

## <a name="remarks"></a>Hinweise

Eine vollständige Beschreibung der Oberflächenanlagen finden Sie unter DirectDraw Software Development Kit (SDK) und Driver Development Kit (DDK).

> [!Note]  
> Wie bei anderen Oberflächenanlagen ist die resultierende Anlage eine einseitige Anlage. Nachdem diese Funktion aufgerufen wurde, wird *hSurfaceTo* nicht an *hSurfaceFrom* angefügt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




