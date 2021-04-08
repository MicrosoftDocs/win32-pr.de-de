---
description: Installiert das angegebene ActiveX-Objekt.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Ieaxisysteminstaller:: initializesysteminstaller-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867812"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>Ieaxisysteminstaller:: initializesysteminstaller-Methode

Die **initializesysteminstaller** -Methode installiert das angegebene ActiveX-Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinurl* \[ in\]
</dt> <dd>

Die URL des zu installierenden ActiveX-Objekts.

</dd> <dt>

*dwclientpid* \[ in\]
</dt> <dd>

Die Prozess-ID des aufrufenden Prozesses.

</dd> <dt>

*pCallback* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Instanz der [**ieaxiservicecallback**](ieaxiservicecallback.md) -Schnittstelle, die überprüft, ob das ActiveX-Objekt installiert werden darf.

</dd> <dt>

*pbstrinnonce* \[ vorgenommen\]
</dt> <dd>

Ein Kontext, der zum Freigeben von Zustandsinformationen in Aufrufen anderer Methoden verwendet werden kann, die zum Überprüfen und Herunterladen des ActiveX-Objekts verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxisysteminstaller ist als a50ea6f8-4764-4299-b309-022b2a8b4d8d definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ieaxisysteminstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

