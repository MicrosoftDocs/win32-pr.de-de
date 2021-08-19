---
title: MpUpdateControl-Funktion (MpClient.h)
description: Ermöglicht die Steuerung eines Signaturaktualisierungsvorgangs, der asynchron über MpUpdateStart initiiert wurde.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Legacy-Windows-Umgebungsfeatures der MpUpdateControl-Funktion
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69926f26b470ba41226883bdb32fab13c5d776858595c256fe70e7f95e898c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476272"
---
# <a name="mpupdatecontrol-function"></a>MpUpdateControl-Funktion

Ermöglicht die Steuerung eines Signaturaktualisierungsvorgangs, der asynchron über [**MpUpdateStart**](mpupdatestart.md)initiiert wurde. Zum Aufrufen dieser Funktion sind Administratorrechte erforderlich, da sie den Abbruch eines systemweiten Signaturupdates ermöglicht.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hUpdateHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Verarbeiten eines asynchronen Signaturaktualisierungsvorgangs. Dieses Handle wird von der [**MpScanStart-Funktion**](mpscanstart.md) zurückgegeben.

</dd> <dt>

*UpdateControl* \[ In\]
</dt> <dd>

Typ: **MPCONTROL**

Gibt die Signaturupdate-Steuerelementoption an. Es muss der folgende Wert sein:



| Wert                                                                                                                                                               | Bedeutung                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl> | Abbrechen des Signaturaktualisierungsvorgangs.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **S \_ OK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





