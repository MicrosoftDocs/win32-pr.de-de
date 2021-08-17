---
description: Die SetResizerGUID-Methode gibt die CLSID eines benutzerdefinierten Filters für die Größenänderung von Videos an.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: IRenderEngine2::SetResizerGUID-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e650a250333ac784e599d0bce820ef390a937f49bff2371b1b7a52b18d9d0ad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818535"
---
# <a name="irenderengine2setresizerguid-method"></a>IRenderEngine2::SetResizerGUID-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetResizerGUID` -Methode gibt die CLSID eines benutzerdefinierten Video-Größenänderungsfilters an. Rufen Sie diese Methode auf, um den von DirectShow Editing Services verwendeten Standardfilter für die Größenänderung zu ersetzen. Ihr Filter muss als COM-Objekt auf dem System des Benutzers registriert sein und die [**IResize-Schnittstelle**](iresize.md) unterstützen.

Rufen Sie diese Methode auf, bevor [**Sie IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md)aufrufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ResizerGuid* \[ In\]
</dt> <dd>

Die CLSID des Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie die folgende CLSID, um zum Standard-DES-Resizer zurückzukehren:


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9.0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IRenderEngine2-Schnittstelle**](irenderengine2.md)
</dt> </dl>

 

 




