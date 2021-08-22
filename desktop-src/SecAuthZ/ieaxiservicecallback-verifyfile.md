---
description: Führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende .cab-Datei heruntergeladen wurde.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: IeAxiServiceCallback::VerifyFile-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3c8072680d42e214304cae1f0a6002b7a1fbc036fc075c5c6777dd7612733a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414710"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>IeAxiServiceCallback::VerifyFile-Methode

Die **VerifyFile-Methode** führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an den die entsprechende .cab Datei heruntergeladen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrFileUrl* \[ In\]
</dt> <dd>

Die URL des zu überprüfende ActiveX-Objekts.

</dd> <dt>

*bstrApprovedFileName* \[ out\]
</dt> <dd>

Der Name der Datei, in die die .cab Datei heruntergeladen wurde, die dem ActiveX-Objekt zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](/windows/desktop/SecCrypto/common-hresult-values)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, nur Windows Vista \[ Ultimate-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback ist als 1823E7BA-EC36-447a-9B2E-B4912E15AFE7 definiert.<br/>                   |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

