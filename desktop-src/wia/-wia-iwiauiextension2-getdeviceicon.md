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
ms.openlocfilehash: 236a12bdf37a3d4c73a4601dd35667e946442bab3fc8dc66340d5f889b165f20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669382"
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

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn bei der Methode ein Fehler auftritt, wird ein entsprechender Fehlercode zurückgegeben. In der folgenden Tabelle sind einige der möglichen Rückgabestatuscodes aufgeführt.



| Fehlercode    | BESCHREIBUNG                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ INVALIDARG | Der Parameter bstrDeviceId oder phIcon ist **NULL,** oder bstrDeviceIdzeigen nicht auf eine gültige WIA-Geräte-ID-Zeichenfolge. |
| E \_ FAIL       | Es ist keine Symbolressource verfügbar.                                                                               |
| E \_ NOTIMPL    | Es ist kein Symbol der angeforderten Größe verfügbar.                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




