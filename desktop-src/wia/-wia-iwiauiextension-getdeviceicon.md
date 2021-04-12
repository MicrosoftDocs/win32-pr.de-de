---
description: Ruft ein benutzerdefiniertes Gerätesymbol ab.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'Iwiauiextension:: getdeviceicon-Methode (wiadevd. h)'
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
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129408"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a>Iwiauiextension:: getdeviceicon-Methode

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

*bstraude viceid* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt die Geräte-ID des WIA-Geräts an, für das das Symbol abgerufen werden soll.

</dd> <dt>

*phicon* \[ vorgenommen\]
</dt> <dd>

Typ: **HICON \** _

Verweist auf einen Speicherort, der ein Handle für das Symbol für das Gerät empfängt.

</dd> <dt>

_nSize * \[ in\]
</dt> <dd>

Typ: **ulong**

Gibt die gewünschte Symbolgröße in Pixel an. Es wird davon ausgegangen, dass das Symbol quadratisch ist, und nSize gibt sowohl die Breite als auch die Höhe des angeforderten Symbols an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




