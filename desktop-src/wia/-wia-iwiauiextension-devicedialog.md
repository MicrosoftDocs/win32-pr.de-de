---
description: Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Iwiauiextension::D evicedialog-Methode (wiadevd. h)
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
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526447"
---
# <a name="iwiauiextensiondevicedialog-method"></a>Iwiauiextension::D evicedialog-Methode

Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevicedialogdata* \[ in\]
</dt> <dd>

Typ: **pdevicedialogdata \** _

Verweist auf eine [_ *devicedialogdata* *](-wia-devicedialogdata.md) -Struktur, die alle Daten enthält, die zum Implementieren des Geräte Dialogfelds erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn der Benutzer das Dialogfeld abbricht, gibt die Methode den Wert "false" zurück \_ . Wenn die Methode nicht implementiert ist, wird E \_ notimpl zurückgegeben. Wenn die Methode fehlschlägt, wird ein Standard-com-Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die [**iwiauiextension**](-wia-iwiauiextension.md) -Schnittstelle implementieren und die Systembenutzer Oberfläche nicht ersetzen möchten, muss diese Methode trotzdem implementiert werden. Sie sollte jedoch nichts weiter tun, als "E \_ notimpl" zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




