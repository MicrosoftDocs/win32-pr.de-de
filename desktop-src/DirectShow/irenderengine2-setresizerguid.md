---
description: Die Methode "Set tresizerguid" gibt die CLSID eines benutzerdefinierten Videos zum Ändern der Größenänderung an.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'IRenderEngine2:: stresizerguid-Methode (qedit. h)'
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
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356071"
---
# <a name="irenderengine2setresizerguid-method"></a>IRenderEngine2:: stresizerguid-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetResizerGUID` Methode gibt die CLSID eines benutzerdefinierten Videos zum Ändern der Größenänderung an. Verwenden Sie diese Methode, um den von DirectShow-Bearbeitungs Diensten verwendeten Standardfilter für die Größe der Größe zu ersetzen. Der Filter muss als COM-Objekt im System des Benutzers registriert sein, und er muss die [**iresize**](iresize.md) -Schnittstelle unterstützen.

Rufen Sie diese Methode auf, bevor Sie " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md)" aufrufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Resizerguid* \[ in\]
</dt> <dd>

Die CLSID des Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die folgende CLSID, um zum Standardwert für den des-Resizer zurückzukehren:


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**IRenderEngine2-Schnittstelle**](irenderengine2.md)
</dt> </dl>

 

 




