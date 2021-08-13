---
description: 'IWiaUIExtension2::D eviceDialog-Methode: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standardsystem-Benutzeroberfläche ersetzt.'
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2::D eviceDialog-Methode (Wiadevd.h)
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
ms.openlocfilehash: 582a2fe90e6a455b2c0d0119b749a9d86b912b58150d30f3804466ef5bea2a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439884"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2::D eviceDialog-Methode

Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standard-Benutzeroberfläche des Systems ersetzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDeviceDialogData* \[ In\]
</dt> <dd>

Typ: **PDEVICEDIALOGDATA2 \***

Verweist auf eine [**DEVICEDIALOGDATA2-Struktur,**](-wia-devicedialogdata2.md) die alle Daten enthält, die zum Implementieren des Gerätedialogfelds erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn der Benutzer das Dialogfeld abbricht, gibt die Methode S \_ FALSE zurück. Wenn bei der Methode ein Fehler auftritt, wird ein entsprechender Fehlercode zurückgegeben. In der folgenden Tabelle sind einige der möglichen Rückgabestatuscodes aufgeführt.



| Fehlercode    | BESCHREIBUNG                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | Der Parameter pDeviceDialogData ist **NULL.** |
| E \_ NOTIMPL    | Die Methode ist nicht implementiert.           |



 

## <a name="remarks"></a>Hinweise

Wenn Sie die [**IWiaUIExtension2-Schnittstelle**](-wia-iwiauiextension2.md) implementieren und die Benutzeroberfläche des Systems nicht ersetzen möchten, muss diese Methode weiterhin implementiert werden, sollte aber nur E \_ NOTIMPL zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




