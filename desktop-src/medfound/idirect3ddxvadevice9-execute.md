---
description: Führt einen DXVA-Decodierungs Vorgang (DirectX Video Acceleration) aus.
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9:: Execute-Methode (DXVA. h)'
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
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358842"
---
# <a name="idirect3ddxvadevice9execute-method"></a>IDirect3DDXVADevice9:: Execute-Methode

Führt einen DXVA-Decodierungs Vorgang (DirectX Video Acceleration) aus.

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

*Functionnum* 
</dt> <dd>

Ein **DWORD** , das mindestens eine DXVA-Funktions Nummer enthält. Weitere Informationen finden Sie in der [DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pinputdata* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der Eingabedaten für den Decodierungs Vorgang enthält. Die Bedeutung dieser Daten hängt vom Surface-Typ und der Funktions Nummer ab.

</dd> <dt>

*Input size* 
</dt> <dd>

Die Größe der Eingabedaten in Bytes.

</dd> <dt>

*OutputData* 
</dt> <dd>

Zeiger auf einen Puffer, in den die Video Zugriffstaste Ausgabedaten schreibt.

</dd> <dt>

*Outputsize* 
</dt> <dd>

Die Größe des *outputData* -Puffers in Bytes.

</dd> <dt>

*Numbuffers* 
</dt> <dd>

Die Anzahl der Elemente im *pbufferinfo* -Array.

</dd> <dt>

*pbufferinfo* 
</dt> <dd>

Ein Zeiger auf ein Array von [**dxvabufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) -Strukturen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
