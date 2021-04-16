---
description: Erstellt geschützte Ausgabe Objekte für ein Anzeigegerät.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Funktion "kreateopmprotectedoutputs"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524619"
---
# <a name="createopmprotectedoutputs-function"></a>Funktion "kreateopmprotectedoutputs"

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität des Anzeige Treibers zuzugreifen. Anwendungen sollten diese Funktion nicht aufzurufen.

 

Erstellt geschützte Ausgabe Objekte für ein Anzeigegerät.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstrindevicename* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Unicode- \_ Zeichen**](/windows/win32/api/subauth/ns-subauth-unicode_string) folgen Struktur, die den Namen des Anzeige Geräts enthält, wie von der [**getmonitorinfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) -Funktion zurückgegeben.

</dd> <dt>

*vos* \[ in\]
</dt> <dd>

Ein Member der **dxgkmdt \_ OPM- \_ Video \_ Ausgabe \_ Semantik** -Enumeration, der angibt, ob für die geschützte Ausgabe eine zertifizierte COPP-Semantik (Output Protection Protocol) oder eine OPM-Semantik verwendet wird.

</dd> <dt>

*dwopmprotectedoutputarraysize* \[ in\]
</dt> <dd>

Die Anzahl der Elemente im *pohopmprotectedoutputarray* -Array.

</dd> <dt>

*pdwnumopmprotectedoutputsinarray* \[ vorgenommen\]
</dt> <dd>

Empfängt die Anzahl der Elemente, die die Funktion in das *pohopmprotectedoutputarray* -Array kopiert.

</dd> <dt>

*pohopmprotectedoutputarray* \[ vorgenommen\]
</dt> <dd>

Ein Array, das Handles für die geschützten Ausgabe Objekte empfängt. Jedes Handle muss durch Aufrufen von [**destroyopmprotectedoutput**](destroyopmprotectedoutput.md)freigegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, wird der **Status \_ erfolgreich** zurückgegeben. Andernfalls wird ein **NTSTATUS** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufzurufen:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**Opmgetvideooutputsfromhmonitor**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Gdi32.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Funktionen](opm-functions.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 
