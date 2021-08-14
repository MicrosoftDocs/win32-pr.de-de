---
description: Installiert das angegebene ActiveX Objekt.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: IeAxiSystemInstaller::InitializeSystemInstaller-Methode
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
ms.openlocfilehash: 9619557395ede0510e04378a03f2ded32fa7a9c829c8c6f40acdaf58b8e0fda2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414650"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a>IeAxiSystemInstaller::InitializeSystemInstaller-Methode

Die **InitializeSystemInstaller-Methode** installiert das angegebene ActiveX Objekt.

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

*bstrUrl* \[ In\]
</dt> <dd>

Die URL des ActiveX zu installierenden Objekts.

</dd> <dt>

*dwClientPID* \[ In\]
</dt> <dd>

Die Prozess-ID des aufrufenden Prozesses.

</dd> <dt>

*pCallback* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Instanz der [**IeAxiServiceCallback-Schnittstelle,**](ieaxiservicecallback.md) der überprüft, ob das ActiveX-Objekt installiert werden darf.

</dd> <dt>

*pbstrNonce* \[ out\]
</dt> <dd>

Ein Kontext, der zum Freigeben von Zustandsinformationen in Aufrufen anderer Methoden verwendet werden kann, die zum Überprüfen und Herunterladen des ActiveX werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](/windows/desktop/SecCrypto/common-hresult-values)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller ist als a50ea6f8-4764-4299-b309-022b2a8b4d8d definiert.<br/>                   |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IeAxiSystemInstaller**](ieaxisysteminstaller.md)
</dt> </dl>

 

