---
description: Zerstört ein zuvor zugeordnetes Kernelmodus-Microsoft DirectDraw-Oberflächenobjekt.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: NtGdiDdDestroySurface-Funktion (Ntgdi.h)
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
ms.openlocfilehash: 1ec5538e7aea7abd938cb57dc3dfba9c51e7c6c60f81630bf6665c1ee467ed24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956509"
---
# <a name="ntgdidddestroysurface-function"></a>NtGdiDdDestroySurface-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Zerstört ein zuvor zugeordnetes Kernelmodus-Microsoft DirectDraw-Oberflächenobjekt.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSurface* \[ In\]
</dt> <dd>

Handle für zuvor zugeordnetes Kernelmodus-Oberflächenobjekt.

</dd> <dt>

*bRealDestroy* \[ In\]
</dt> <dd>

Gibt an, wie die Oberfläche zerstört werden soll. Kann einer der folgenden Werte sein.

<dt>



 (TRUE)


</dt> <dd>

Zerstören Sie die Oberfläche und den freien Videospeicher.

</dd> <dt>



 (FALSE)


</dt> <dd>

Geben Sie den Videospeicher frei, belassen Sie die Oberfläche jedoch in einem nicht initialisierten Zustand.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiDdDestroySurface** gibt einen der folgenden Rückrufcodes zurück.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BEHANDELTER \_ DDHAL-TREIBER \_**</dt> </dl>    | Der Treiber hat den Vorgang ausgeführt und einen gültigen Rückgabecode für diesen Vorgang zurückgegeben. Wenn dieser Code DD \_ OK ist, wird DirectDraw oder Direct3D mit der Funktion fortgesetzt. Andernfalls gibt DirectDraw oder Direct3D den vom Treiber bereitgestellten Fehlercode zurück und bricht die Funktion ab.<br/>                                                                                 |
| <dl> <dt>**\_DDHAL-TREIBER \_ NICHT BEHANDELT**</dt> </dl> | Der Treiber hat keinen Kommentar zum angeforderten Vorgang. Wenn der Treiber einen bestimmten Rückruf implementiert haben muss, meldet DirectDraw oder Direct3D eine Fehlerbedingung. Andernfalls verarbeitet DirectDraw oder Direct3D den Vorgang so, als ob der Treiberrückruf nicht durch Ausführen der geräteunabhängigen DirectDraw- oder Direct3D-Implementierung definiert worden wäre.<br/> |



 

## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Anwendungen anstelle dieser Funktion die DirectDraw- und Direct3D-APIs verwenden, um Oberflächen zu erstellen und zu zerstören.

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

 

 




