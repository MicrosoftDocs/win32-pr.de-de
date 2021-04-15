---
title: Mpupdatecontrol-Funktion (mpclient. h)
description: Ermöglicht das Steuern eines Signatur Aktualisierungs Vorgangs, der asynchron über mpupdatestart initiiert wurde.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Mpupdatecontrol-Funktion Legacy Funktionen der Windows-Umgebung
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
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477655"
---
# <a name="mpupdatecontrol-function"></a>Mpupdatecontrol-Funktion

Ermöglicht das Steuern eines Signatur Aktualisierungs Vorgangs, der asynchron über [**mpupdatestart**](mpupdatestart.md)initiiert wurde. Zum Aufrufen dieser Funktion ist Administrator Berechtigung erforderlich, da Sie den Abbruch eines systemweiten Signatur Updates zulässt.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hupdatehandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für einen asynchronen Signatur Aktualisierungs Vorgang. Dieses Handle wird von der [**mpscanstart**](mpscanstart.md) -Funktion zurückgegeben.

</dd> <dt>

*Updatecontrol* \[ in\]
</dt> <dd>

Typ: **MPControl**

Gibt die Option zum Aktualisieren der Signatur Aktualisierung an. Er muss den folgenden Wert aufweisen:



| Wert                                                                                                                                                               | Bedeutung                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**Mpcontrol- \_ Abbruch**</dt> </dl> | Brechen Sie den Signatur Aktualisierungs Vorgang ab.<br/> |



 

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

[**Mpscanstart**](mpscanstart.md)
</dt> </dl>

 

 





