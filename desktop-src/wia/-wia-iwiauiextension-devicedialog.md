---
description: 'IWiaUIExtension::D eviceDialog-Methode: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standardsystembenutzeroberfläche ersetzt.'
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension::D eviceDialog-Methode (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: a06ac5428743c31bae22c6d106ee927791739295754b15ac9764045c3aeeffab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813870"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension::D eviceDialog-Methode

Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standardsystem-Benutzeroberfläche ersetzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDeviceDialogData* \[ In\]
</dt> <dd>

Typ: **PDEVICEDIALOGDATA \***

Zeigt auf eine [**DEVICEDIALOGDATA-Struktur,**](-wia-devicedialogdata.md) die alle Daten enthält, die zum Implementieren des Gerätedialogs erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn der Benutzer den Dialog abbricht, gibt die Methode S \_ FALSE zurück. Wenn die Methode nicht implementiert ist, wird E \_ NOTIMPL zurückgegeben. Wenn die Methode fehlschlägt, wird ein COM-Standardfehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn Sie die [**IWiaUIExtension-Schnittstelle**](-wia-iwiauiextension.md) implementieren und die Systembenutzerschnittstelle nicht ersetzen möchten, muss diese Methode weiterhin implementiert werden, sollte aber nur E \_ NOTIMPL zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




