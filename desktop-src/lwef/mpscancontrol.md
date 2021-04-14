---
title: Mpscancontrol-Funktion (mpclient. h)
description: Ermöglicht das Steuern einer Überprüfung, die asynchron über mpscanstart initiiert wurde.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Mpscancontrol-Funktion Legacy Funktionen der Windows-Umgebung
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
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476497"
---
# <a name="mpscancontrol-function"></a>Mpscancontrol-Funktion

Ermöglicht das Steuern einer Überprüfung, die asynchron über [**mpscanstart**](mpscanstart.md)initiiert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hscanhandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für einen asynchronen Scanvorgang. Dieses Handle wird von der [**mpscanstart**](mpscanstart.md) -Funktion zurückgegeben. Dieser Parameter kann auch auf das von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegebene Malware Protection Manager-Schnittstellen handle festgelegt werden, um eine vom System initiierte Überprüfung zu steuern. in diesem Fall muss der Aufrufer über Administrator Berechtigungen verfügen.

</dd> <dt>

*SCANcontrol* \[ in\]
</dt> <dd>

Typ: **MPControl**

Gibt eine Scan Steuerungs Option an. Dieser Parameter muss eine der folgenden Steuerungs Optionen sein:



| Wert                                                                                                                                                                  | Bedeutung                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**Mpcontrol- \_ Abbruch**</dt> </dl>    | Abbrechen des Scanvorgangs.<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**Mpcontrol- \_ Pause**</dt> </dl>    | Hält den Scanvorgang an.<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**Mpcontrol-Fortsetzung \_**</dt> </dl> | Setzen Sie den angehaltenen Scanvorgang fort.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code. Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mperrormessageformat**](mperrormessageformat.md)
</dt> <dt>

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[**Mpscanstart**](mpscanstart.md)
</dt> </dl>

 

 





