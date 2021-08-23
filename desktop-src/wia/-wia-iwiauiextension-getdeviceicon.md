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
ms.openlocfilehash: 040bcc6bcc5e4e8a7126c5ef7d0a72dbb688a6e5605512ff67527c21bfaa3026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813860"
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

Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol erhalten werden soll.

</dd> <dt>

*phIcon* \[ out\]
</dt> <dd>

Typ: **HICON \***

Zeigt auf einen Speicherort, der ein Handle für das Symbol für das Gerät erhält.

</dd> <dt>

*nSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Gibt die gewünschte Symbolgröße in Pixel an. Das Symbol wird als quadratisch angenommen, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




