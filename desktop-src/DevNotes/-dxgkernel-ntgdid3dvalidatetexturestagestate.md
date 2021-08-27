---
description: Gibt die Anzahl von Durchläufen zurück, bei denen die Hardware die im aktuellen Zustand angegebenen Blendingvorgänge ausführen kann.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: NtGdiD3DValidateTextureStageState-Funktion (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 521169773ae46fa3158752e0d80696888c8bffbfe3dd5d3c0068aee944c290ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088040"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a>NtGdiD3DValidateTextureStageState-Funktion

\[Diese Funktion kann bei jeder Betriebssystemrevision geändert werden. Verwenden Sie stattdessen Microsoft DirectDraw und Microsoft Direct3DAPIs. diese APIs isolieren Anwendungen vor solchen Betriebssystemänderungen und verbergen viele andere Schwierigkeiten bei der direkten Interaktion mit Anzeigetreibern.\]

Gibt die Anzahl von Durchläufen zurück, bei denen die Hardware die im aktuellen Zustand angegebenen Blendingvorgänge ausführen kann.

## <a name="syntax"></a>Syntax


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ in, out\]
</dt> <dd>

Zeiger auf eine [**D3DNTHAL \_ VALIDATETEXTURESTAGESTATEDATA-Struktur,**](/windows-hardware/drivers/ddi/) die die Informationen enthält, die der Treiber zum Ermitteln und Zurückgeben der Anzahl von Durchläufen benötigt, um die Überblendungsvorgänge auszuführen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**NtGdiD3DValidateTextureStageState** gibt einen der folgenden Rückrufcodes zurück.



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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Grafik– Clientunterstützung auf niedriger Ebene](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
