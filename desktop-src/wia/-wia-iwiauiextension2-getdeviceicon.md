---
description: Ruft ein benutzerdefiniertes Gerätesymbol ab.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2:: getdeviceicon-Methode (wiadevd. h)'
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
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526444"
---
# <a name="iwiauiextension2getdeviceicon-method"></a>IWiaUIExtension2:: getdeviceicon-Methode

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

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn die Methode fehlschlägt, wird ein entsprechender Fehlercode zurückgegeben. In der folgenden Tabelle sind einige der möglichen Rückgabestatus Codes aufgeführt.



| Fehlercode    | BESCHREIBUNG                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| E \_ invalidArg | Der Parameter "bstrintoviceid" oder "phicon" ist **null**, oder bstrintoviceid verweist nicht auf eine gültige WIA-Geräte-ID-Zeichenfolge. |
| E \_ fehlschlagen       | Es ist keine Symbol Ressource verfügbar.                                                                               |
| E \_ notimpl    | Es ist kein Symbol der angeforderten Größe verfügbar.                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




