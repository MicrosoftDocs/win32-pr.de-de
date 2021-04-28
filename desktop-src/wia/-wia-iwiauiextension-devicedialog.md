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
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116708"
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

## <a name="remarks"></a>Bemerkungen

Wenn Sie die [**IWiaUIExtension-Schnittstelle**](-wia-iwiauiextension.md) implementieren und die Systembenutzerschnittstelle nicht ersetzen möchten, muss diese Methode weiterhin implementiert werden, sollte aber nur E \_ NOTIMPL zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




