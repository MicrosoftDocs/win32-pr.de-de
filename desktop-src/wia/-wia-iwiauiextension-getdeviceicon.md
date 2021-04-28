---
description: 'IWiaUIExtension::GetDeviceIcon-Methode: Ruft ein benutzerdefiniertes Gerätesymbol ab.'
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: IWiaUIExtension::GetDeviceIcon-Methode (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 9bfa8e87736412822c1a70f75b129aeec30af20e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116658"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>IWiaUIExtension::GetDeviceIcon-Methode

Ruft ein benutzerdefiniertes Gerätesymbol ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDeviceId* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Typ: **HICON \***

Zeigt auf eine Speicherposition, die ein Handle für das Symbol für das Gerät erhält.

</dd> <dt>

*nSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Gibt die gewünschte Symbolgröße in Pixel an. Das Symbol wird als quadratisch angenommen, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




