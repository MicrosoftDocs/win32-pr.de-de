---
description: 'IWiaUIExtension2::GetDeviceIcon-Methode: Ruft ein benutzerdefiniertes Gerätesymbol ab.'
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: IWiaUIExtension2::GetDeviceIcon-Methode (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116618"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>IWiaUIExtension2::GetDeviceIcon-Methode

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

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn die Methode fehlschlägt, wird ein entsprechender Fehlercode zurückgegeben. In der folgenden Tabelle sind einige der möglichen Rückgabestatuscodes aufgeführt.



| Fehlercode    | BESCHREIBUNG                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | Der Parameter bstrDeviceId oder phIcon ist **NULL,** oder bstrDeviceId verweist nicht auf eine gültige WIA-Geräte-ID-Zeichenfolge. |
| E \_ FAIL       | Es ist keine Symbolressource verfügbar.                                                                               |
| E \_ NOTIMPL    | Es ist kein Symbol der angeforderten Größe verfügbar.                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




