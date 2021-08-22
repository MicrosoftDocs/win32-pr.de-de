---
description: Erstellt eine hierarchische Struktur von IWiaItem2-Objekten für ein wia 2.0-Gerät (Windows Image Acquisition).
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: IWiaDevMgr2::CreateDevice-Methode (Wia.h)
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
ms.openlocfilehash: a40267e77671b807f0e6969845a3a5a7096694e4f4e7978467ee9ca5909284d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965729"
---
# <a name="iwiadevmgr2createdevice-method"></a>IWiaDevMgr2::CreateDevice-Methode

Erstellt eine hierarchische Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) für ein wia 2.0-Gerät (Windows Image Acquisition).

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

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstrDeviceID* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den eindeutigen Bezeichner des WIA 2.0-Geräts an.

</dd> <dt>

*ppWiaItem2Root* \[ out\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Empfängt die Adresse eines Zeigers auf die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des Stammelements in der hierarchischen Struktur für das WIA 2.0-Gerät.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen verwenden die **IWiaDevMgr2::CreateDevice-Methode,** um ein Geräteobjekt für die WIA 2.0-Geräte zu erstellen, die durch den bstrDeviceID-Parameter angegeben werden. Nach der Rückgabe speichert die **IWiaDevMgr2::CreateDevice-Methode** eine Adresse eines Zeigers im Parameter *ppWiaItem2Root,* der auf das Stammelement der Struktur von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) verweist, die von **IWiaDevMgr2::CreateDevice** erstellt wurden. Anwendungen können diese Struktur von Objekten verwenden, um Daten vom WIA 2.0-Gerät zu steuern und abzurufen.

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Zeiger aufrufen, die sie über den *ppWiaItem2Root-Parameter* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
