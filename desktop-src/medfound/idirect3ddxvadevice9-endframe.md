---
description: Beendet die Verarbeitung zum Erstellen eines decodierten Bilds.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'IDirect3DDXVADevice9:: Endframe-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130344"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>IDirect3DDXVADevice9:: Endframe-Methode

Beendet die Verarbeitung zum Erstellen eines decodierten Bilds.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sizefehldata* 
</dt> <dd>

Die Größe des von *pfehldata* angegebenen Puffers in Bytes. Der Wert muss 2 sein.

</dd> <dt>

*pfehldaten* 
</dt> <dd>

Zeiger auf einen Puffer, der Daten für die Video Zugriffstaste enthält. Dieser Puffer muss den gleichen Frame Index enthalten, der der [**IDirect3DDXVADevice9:: beginFrame**](idirect3ddxvadevice9-beginframe.md) -Methode im *pinputdata* -Parameter übergeben wurde.

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

 

 




