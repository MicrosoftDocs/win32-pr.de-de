---
description: Hiermit wird ein ActiveX-Objekt überprüft und heruntergeladen.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Ieaxiservice:: Initialize-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218190"
---
# <a name="ieaxiserviceinitialize-method"></a>Ieaxiservice:: Initialize-Methode

Mit der **Initialize** -Methode wird ein ActiveX-Objekt überprüft und heruntergeladen. Wenn das-Objekt die Richtlinien Anforderungen erfüllt, initialisiert diese Methode ein Systemobjekt, das das ActiveX-Objekt installiert.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Fensters, das versucht, das ActiveX-Steuerelement zu installieren.

</dd> <dt>

*dwclientpid* \[ in\]
</dt> <dd>

Die Prozess-ID des aufrufenden Prozesses.

</dd> <dt>

*bstraudesktop* \[ in\]
</dt> <dd>

Der Desktop für das-Objekt.

</dd> <dt>

*bstrinclsid* \[ in\]
</dt> <dd>

Die Klassen-ID des zu installierenden ActiveX-Objekts.

</dd> <dt>

*bstrinurl* \[ in\]
</dt> <dd>

Die URL des zu installierenden ActiveX-Objekts.

</dd> <dt>

*pbstrinnonce* \[ vorgenommen\]
</dt> <dd>

Ein Kontext, der zum Freigeben von Zustandsinformationen in Aufrufen anderer Methoden verwendet werden kann, die zum Überprüfen und Herunterladen des ActiveX-Objekts verwendet werden.

</dd> <dt>

*ppisyncbrokerinterface* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Instanz der [**ieaxisysteminstaller**](ieaxisysteminstaller.md) -Schnittstelle, mit der das ActiveX-Steuerelement installiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Rückgabecode/-wert                                                                                                                                                              | BESCHREIBUNG                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Vertrauens \_ Stellung E \_ Betreff \_ nicht \_ vertrauenswürdig**</dt> <dt>0x800b0004</dt> </dl> | Das ActiveX-Objekt sollte nicht installiert werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxiservice ist definiert als E9E92380-9ecd-4982-A0EB-6815a56ccb27<br/>                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ieaxiservice**](ieaxiservice.md)
</dt> </dl>

 

 




