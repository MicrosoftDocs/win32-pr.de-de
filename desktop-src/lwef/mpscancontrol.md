---
title: MpScanControl-Funktion (MpClient.h)
description: Ermöglicht die Steuerung eines Scans, der asynchron über MpScanStart initiiert wurde.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Legacy-Windows-Umgebungsfeatures der MpScanControl-Funktion
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893fe1d01f9004c9dc2933a5bbb23c4b13fb8933a6121c41810c6e447e5eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114550"
---
# <a name="mpscancontrol-function"></a>MpScanControl-Funktion

Ermöglicht die Steuerung eines Scans, der asynchron über [**MpScanStart**](mpscanstart.md)initiiert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hScanHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Handle für einen asynchronen Scanvorgang. Dieses Handle wird von der [**MpScanStart-Funktion**](mpscanstart.md) zurückgegeben. Dieser Parameter kann auch auf das Schnittstellenhandle des Schadsoftwareschutz-Managers festgelegt werden, das von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben wird, um eine vom System initiierte Überprüfung zu steuern. In diesem Fall muss der Aufrufer über Administratorrechte verfügen.

</dd> <dt>

*ScanControl* \[ In\]
</dt> <dd>

Typ: **MPCONTROL**

Gibt eine Scansteuerelementoption an. Dieser Parameter muss eine der folgenden Steuerelementoptionen sein:



| Wert                                                                                                                                                                  | Bedeutung                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL \_ ABORT**</dt> </dl>    | Abbrechen des Scanvorgangs.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**MPCONTROL \_ PAUSE**</dt> </dl>    | Halten Sie den Scanvorgang an.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**MPCONTROL \_ RESUME**</dt> </dl> | Setzen Sie den angehaltenen Scanvorgang fort.<br/> |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





