---
description: Führt einen Decodierungsvorgang der DirectX-Videobeschleunigung (DXVA) aus.
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: IDirect3DDXVADevice9::Execute-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ac00e5f78e4281523c006216f3173745ba26bc6429ddfdd9d74c9abbe616b89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465960"
---
# <a name="idirect3ddxvadevice9execute-method"></a>IDirect3DDXVADevice9::Execute-Methode

Führt einen Decodierungsvorgang der DirectX-Videobeschleunigung (DXVA) aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FunctionNum* 
</dt> <dd>

Ein **DWORD,** das mindestens eine DXVA-Funktionsnummer enthält. Weitere Informationen finden Sie in der [DXVA 1.0-Spezifikation.](/windows-hardware/drivers/display/directx-video-acceleration)

</dd> <dt>

*pInputData* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der Eingabedaten für den Decodierungsvorgang enthält. Die Bedeutung dieser Daten hängt vom Oberflächentyp und der Funktionsnummer ab.

</dd> <dt>

*InputSize* 
</dt> <dd>

Die Größe der Eingabedaten in Bytes.

</dd> <dt>

*OutputData* 
</dt> <dd>

Zeiger auf einen Puffer, in den der Videobeschleuniger Ausgabedaten schreibt.

</dd> <dt>

*OutputSize* 
</dt> <dd>

Die Größe des *OutputData-Puffers* in Bytes.

</dd> <dt>

*NumBuffers* 
</dt> <dd>

Die Anzahl der Elemente im *pBufferInfo-Array.*

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Ein Zeiger auf ein Array von [**DXVABufferInfo-Strukturen.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
