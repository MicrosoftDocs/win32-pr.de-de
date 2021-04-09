---
description: Erstellt eine hierarchische Struktur von IWiaItem2-Objekten für ein Windows-Abbild Erfassungsgerät (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2:: kreatedevice-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865252"
---
# <a name="iwiadevmgr2createdevice-method"></a>IWiaDevMgr2:: kreatedevice-Methode

Erstellt eine hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten für ein Windows-Abbild Erfassungsgerät (WIA) 2,0.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den eindeutigen Bezeichner des WIA 2,0-Geräts an.

</dd> <dt>

*ppWiaItem2Root* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements in der hierarchischen Struktur für das WIA 2,0-Gerät.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anwendungen verwenden die **IWiaDevMgr2:: kreatedevice** -Methode, um ein Geräte Objekt für die WIA 2,0-Geräte zu erstellen, die durch den bstrindeviceid-Parameter angegeben werden. Wenn der Wert zurückgegeben wird, speichert die **IWiaDevMgr2:: kreatedevice** -Methode eine Adresse eines Zeigers im Parameter *ppWiaItem2Root*, der auf das Stamm Element der [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte zeigt, die von **IWiaDevMgr2:: kreatedevice** erstellt wurden. Anwendungen können diese Objektstruktur verwenden, um Daten aus dem WIA 2,0-Gerät zu steuern und abzurufen.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Zeiger aufrufen, die Sie über den *ppWiaItem2Root* -Parameter empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
