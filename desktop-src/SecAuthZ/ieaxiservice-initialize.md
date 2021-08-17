---
description: Überprüft und lädt ein ActiveX herunter.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: IeAxiService::Initialize-Methode
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
ms.openlocfilehash: 911d955f84d81b225a1b4062e47b2b9b6ab6d058aa6df2e6a72a8d40242345a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414890"
---
# <a name="ieaxiserviceinitialize-method"></a>IeAxiService::Initialize-Methode

Die **Initialize-Methode** überprüft und lädt ein ActiveX herunter. Wenn das -Objekt die Richtlinienanforderungen erfüllt, initialisiert diese Methode ein Systemobjekt, das das ActiveX installiert.

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

*hwndParent* \[ In\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster des Fensters, das versucht, das steuerelement ActiveX installieren.

</dd> <dt>

*dwClientPID* \[ In\]
</dt> <dd>

Die Prozess-ID des aufrufenden Prozesses.

</dd> <dt>

*bstrDesktop* \[ In\]
</dt> <dd>

Der Desktop für das -Objekt.

</dd> <dt>

*bstrClsID* \[ In\]
</dt> <dd>

Die Klassen-ID des ActiveX zu installierenden Objekts.

</dd> <dt>

*bstrURL* \[ In\]
</dt> <dd>

Die URL des ActiveX zu installierenden Objekts.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Ein Kontext, der zum Freigeben von Zustandsinformationen in Aufrufen anderer Methoden verwendet werden kann, die zum Überprüfen und Herunterladen des ActiveX werden.

</dd> <dt>

*ppISyncBrokerInterface* \[ out\]
</dt> <dd>

Ein Zeiger auf die Instanz der [**IeAxiSystemInstaller-Schnittstelle,**](ieaxisysteminstaller.md) die das ActiveX installiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.



| Rückgabecode/-wert                                                                                                                                                              | BESCHREIBUNG                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**VERTRAUEN \_ E \_ SUBJECT \_ NOT \_ TRUSTED**</dt> <dt>0x800B0004</dt> </dl> | Das ActiveX-Objekt sollte nicht installiert werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService ist als E9E92380-9ECD-4982-A0EB-6815A56CCF27 definiert.<br/>                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IeAxiService**](ieaxiservice.md)
</dt> </dl>

 

 




