---
description: Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'IWiaItem2:: enumdevicecapabili-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526468"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>IWiaItem2:: enumdevicecapabili-Methode

Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein Windows-Abbild Erfassungsgerät (WIA) 2,0 unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Gibt ein Flag an, das den Typ der aufzuzählenden Funktionen auswählt. Es handelt sich um einen der folgenden Werte.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA- \_ Geräte \_ Befehle**


</dt> <dd>

Listet Geräte Befehle auf.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA- \_ Geräte \_ Ereignisse**


</dt> <dd>

Listet Geräte Ereignisse auf.

</dd> </dl> </dd> <dt>

*ppienumwia \_ DEV \_* - \[ out\]
</dt> <dd>

Typ: **[ **ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Empfängt einen Zeiger auf die [**ienumwia \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) -Schnittstelle, die von dieser Methode erstellt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird verwendet, um ein Enumeratorobjekt zum Abrufen der Befehle und Ereignisse zu erstellen, die von einem WIA 2,0-Gerät unterstützt werden. Der *lFlags* -Parameter wird verwendet, um anzugeben, welche Arten von Gerätefunktionen aufgelistet werden sollen. Die **IWiaItem2:: enumdevicecapabili-** Methode speichert die Adresse der Schnittstelle des Enumeratorobjekts im *ppienumwia \_ dev \_ Caps* -Parameter.

Diese Methode kann nur für das Stamm Element von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten einer Gerätestruktur aufgerufen werden.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienumwia \_ dev \_ Caps* -Parameter erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
