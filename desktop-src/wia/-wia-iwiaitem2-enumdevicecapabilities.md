---
description: Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein Windows WIA 2.0-Gerät unterstützt.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: IWiaItem2::EnumDeviceCapabilities-Methode (Wia.h)
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
ms.openlocfilehash: 6748966beaa3bf16f668c4b8b0de60a4302ebcf514f06a3d588999d5faebaf3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450460"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>IWiaItem2::EnumDeviceCapabilities-Methode

Erstellt einen Enumerator, der verwendet wird, um die Befehle und Ereignisse zu ermitteln, die ein Windows WIA 2.0-Gerät unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Gibt ein Flag an, das den Typ der aufzuzählenden Funktionen auswählt. Dies ist einer der folgenden Werte.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_ \_ WIA-GERÄTEBEFEHLE**


</dt> <dd>

Aufzählen von Gerätebefehlen.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_WIA-GERÄTEEREIGNISSE \_**


</dt> <dd>

Aufzählen von Geräteereignissen.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ DEV \_ CAPS* \[ out\]
</dt> <dd>

Typ: **[ **IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Empfängt einen Zeiger auf die [**IEnumWIA \_ DEV \_ CAPS-Schnittstelle,**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) die von dieser Methode erstellt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um ein Enumeratorobjekt zu erstellen, um den Satz von Befehlen und Ereignissen abzurufen, die ein WIA 2.0-Gerät unterstützt. Der *lFlags-Parameter* wird verwendet, um anzugeben, welche Arten von Gerätefunktionen aufzählt werden sollen. Die **IWiaItem2::EnumDeviceCapabilities-Methode** speichert die Adresse der Schnittstelle des Enumeratorobjekts im *ppIEnumWIA \_ DEV \_ CAPS-Parameter.*

Diese Methode kann nur für das Stammelement von [**IWiaItem2-Objekten**](-wia-iwiaitem2.md) einer Gerätestruktur aufgerufen werden.

Anwendungen müssen die [IUnknown::Release-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Schnittstellenzeiger aufrufen, die sie über den *PPIEnumWIA \_ DEV \_ CAPS-Parameter* empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
