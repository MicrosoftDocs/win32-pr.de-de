---
description: Ruft Informationen zu den komprimierten Puffern ab, die für die hardwarebeschleunigte Decodierung erforderlich sind.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: IDirect3DVideoDevice9::GetDXVACompressedBufferInfo-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: efb96ec457cdb81f89982947bf1b9bc40543789b2e9ac253d83c81727f1efae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942290"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>IDirect3DVideoDevice9::GetDXVACompressedBufferInfo-Methode

Ruft Informationen zu den komprimierten Puffern ab, die für die hardwarebeschleunigte Decodierung erforderlich sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* 
</dt> <dd>

Zeiger auf eine GUID, die das DXVA-Profil angibt. Rufen Sie [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)auf, um eine Liste der unterstützten Profile abzurufen.

</dd> <dt>

*pUncompData* 
</dt> <dd>

Zeiger auf eine [**DXVAUncompDataInfo-Struktur,**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) die die Größe und das Pixelformat der nicht komprimierten Daten angibt.

</dd> <dt>

*pNumBuffers* 
</dt> <dd>

Gibt bei eingabe die Anzahl der Elemente im *pBufferInfo-Array* an. Wenn *pBufferInfo* **NULL** ist, muss der Wert von `*pNumBuffers` 0 (null) sein.

Wenn *pBufferInfo* **null** ist, erhält *pNumBuffers* bei der Ausgabe die Größe des zuzuordnenden Arrays. Andernfalls *empfängt pNumBuffers* die tatsächliche Anzahl von Elementen, die in das *pBufferInfo-Array* kopiert werden.

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Adresse eines Arrays von [**DXVACompBufferInfo-Strukturen**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) oder **NULL**. Wenn der Wert ungleich **NULL** ist, kopiert die Methode eine Liste von **DXVACompBufferInfo-Strukturen** in dieses Array. Jede Struktur entspricht einem Typ komprimierter Datenpuffer, der vom Videobeschleuniger verwendet wird.

Legen Sie alle Arrayelemente auf 0 (null) fest, bevor Sie diese Methode aufrufen.

Jeder Arrayindex entspricht einem der DXVA-Oberflächentypen, die in dxva.h definiert sind. Die Videobeschleunigung gibt eine Liste mit bis zu **DXVA \_ NUM TYPES \_ COMP \_ \_ BUFFERS-Arrayeinträgen** zurück. Ausführliche Informationen finden Sie in der [DXVA 1.0-Spezifikation,](/windows-hardware/drivers/display/directx-video-acceleration)Abschnitt 3.4, "Pufferbeschreibungsliste". Wenn kein bestimmter Puffertyp vom DXVA-Profil verwendet wird, enthält der Eintrag an diesem Index Nullen für alle Werte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
