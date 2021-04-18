---
description: Startet die Verarbeitung zum Erstellen eines decodierten Bilds.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9:: beginFrame-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347937"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>IDirect3DDXVADevice9:: beginFrame-Methode

Startet die Verarbeitung zum Erstellen eines decodierten Bilds.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdstsurface* 
</dt> <dd>

Ein Zeiger auf die **IDirect3DSurface9** -Schnittstelle der nicht komprimierten Ziel Oberfläche.

</dd> <dt>

*Sizinput Data* 
</dt> <dd>

Die Größe des durch *pinputdata* angegebenen Puffers in Bytes. Der Wert muss 2 sein.

</dd> <dt>

*pinputdata* 
</dt> <dd>

Zeiger auf einen Puffer, der Daten für die Video Zugriffstaste enthält. Dieser Puffer muss den NULL basierten Frame Index enthalten, der als **Wort** Wert angegeben wird.

</dd> <dt>

*psizeoutputdata* 
</dt> <dd>

Die Größe des von *poutputdata* angegebenen Puffers in Bytes. Der Wert muss 0 (null) sein.

</dd> <dt>

*poutputdata* 
</dt> <dd>

Zeiger auf einen Puffer, in den die Video Zugriffstaste schreiben kann. Legen Sie diesen Parameter auf **null** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Für jeden Aufrufen von **beginFrame** muss der Decoder einen entsprechenden [**IDirect3DDXVADevice9:: Endframe**](idirect3ddxvadevice9-endframe.md)aufrufen.

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

 

 




