---
description: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2::D evicedialog-Methode (wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214649"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2::D evicedialog-Methode

Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevicedialogdata* \[ in\]
</dt> <dd>

Typ: **PDEVICEDIALOGDATA2 \** _

Verweist auf eine [_ *DEVICEDIALOGDATA2* *](-wia-devicedialogdata2.md) -Struktur, die alle Daten enthält, die zum Implementieren des Geräte Dialogfelds erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn der Benutzer das Dialogfeld abbricht, gibt die Methode den Wert "false" zurück \_ . Wenn die Methode fehlschlägt, wird ein entsprechender Fehlercode zurückgegeben. In der folgenden Tabelle sind einige der möglichen Rückgabestatus Codes aufgeführt.



| Fehlercode    | BESCHREIBUNG                              |
|---------------|------------------------------------------|
| E \_ invalidArg | Pdevicedialogdata des Parameters ist **null**. |
| E \_ notimpl    | Die Methode ist nicht implementiert.           |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die [**IWiaUIExtension2**](-wia-iwiauiextension2.md) -Schnittstelle implementieren und die Systembenutzer Oberfläche nicht ersetzen möchten, muss diese Methode trotzdem implementiert werden, aber Sie sollte nicht mehr als "E \_ notimpl" zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




