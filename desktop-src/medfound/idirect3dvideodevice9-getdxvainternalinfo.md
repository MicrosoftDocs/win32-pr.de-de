---
description: Abfragen der Menge an Scratchspeicher, die die Hardwareabstraktionsschicht (Hardware Abstraction Layer, HALOGEN) für ihre private Verwendung zuteilen wird.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: IDirect3DVideoDevice9::GetDXVAInternalInfo-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: dd15dfdbd35db56262487482e811210970852dcee4e791d710e0551b84e9e620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777210"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>IDirect3DVideoDevice9::GetDXVAInternalInfo-Methode

Abfragen der Menge an Scratchspeicher, die die Hardwareabstraktionsschicht (Hardware Abstraction Layer, HALOGEN) für ihre private Verwendung zuteilen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* 
</dt> <dd>

Zeiger auf eine GUID, die das DXVA-Profil angibt. Um eine Liste der unterstützten Profile zu erhalten, rufen [**Sie IDirect3DVideoDevice9::GetDXVAGuids auf.**](idirect3dvideodevice9-getdxvaguids.md)

</dd> <dt>

*pUncompData* 
</dt> <dd>

Zeiger auf eine [**DXVAUncompDataInfo-Struktur,**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) die die Größe und das Pixelformat der unkomprimierten Daten angibt.

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

Empfängt die Menge des scratch-Arbeitsspeichers in Byte, die vom HALOGEN-Speicher reserviert wird.

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

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




