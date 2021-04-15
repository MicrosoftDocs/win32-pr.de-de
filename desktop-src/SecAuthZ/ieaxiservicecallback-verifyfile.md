---
description: Führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende CAB-Datei heruntergeladen wurde.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Ieaxiservicecallback:: verifyfile-Methode'
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
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529879"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Ieaxiservicecallback:: verifyfile-Methode

Die **verifyfile** -Methode führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende CAB-Datei heruntergeladen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraufileurl* \[ in\]
</dt> <dd>

Die URL des zu überprüfen ActiveX-Objekts.

</dd> <dt>

*bstrapprovedfilename* \[ vorgenommen\]
</dt> <dd>

Der Name der Datei, in der die CAB-Datei, die dem ActiveX-Objekt zugeordnet ist, heruntergeladen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                 |
| IID<br/>                      | IID \_ ieaxiservicecallback ist als 1823e7ba-ec36-447a-9b2e-b4912e15afe7 definiert.<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ieaxiservicecallback**](ieaxiservicecallback.md)
</dt> </dl>

 

