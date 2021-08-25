---
description: Erstellt geschützte Ausgabeobjekte für ein Anzeigegerät.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: CreateOPMProtectedOutputs-Funktion
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
ms.openlocfilehash: fe2bcc0d190cf94a48b10f3d588ab4acd2d93913552f8ccef9d7eb92fefa598b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829060"
---
# <a name="createopmprotectedoutputs-function"></a>CreateOPMProtectedOutputs-Funktion

> [!IMPORTANT]
> Diese Funktion wird vom [Output Protection Manager](output-protection-manager.md) (OPM) verwendet, um auf die Funktionalität im Anzeigetreiber zu zugreifen. Anwendungen sollten diese Funktion nicht aufrufen.

 

Erstellt geschützte Ausgabeobjekte für ein Anzeigegerät.

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

*pstrDeviceName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**UNICODE \_ STRING-Struktur,**](/windows/win32/api/subauth/ns-subauth-unicode_string) die den Namen des Anzeigegeräts enthält, wie von der [**GetMonitorInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) zurückgegeben.

</dd> <dt>

*vos* \[ In\]
</dt> <dd>

Ein Member der **DXGKMDT \_ OPM \_ VIDEO OUTPUT \_ \_ SEMANTICS-Enumeration** und gibt an, ob die geschützte Ausgabe über coPP-Semantik (Certified Output Protection Protocol) oder OPM-Semantik verfügen soll.

</dd> <dt>

*dwOPMProtectedOutputArraySize* \[ In\]
</dt> <dd>

Die Anzahl der Elemente im *array pohOPMProtectedOutputArray.*

</dd> <dt>

*pdwNumOPMProtectedOutputsInArray* \[ out\]
</dt> <dd>

Empfängt die Anzahl der Elemente, die die Funktion in das *array pohOPMProtectedOutputArray kopiert.*

</dd> <dt>

*pohOPMProtectedOutputArray* \[ out\]
</dt> <dd>

Ein Array, das Handles für die geschützten Ausgabeobjekte empfängt. Jedes Handle muss durch Aufrufen von [**DestroyOPMProtectedOutput freigegeben werden.**](destroyopmprotectedoutput.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **STATUS \_ SUCCESS zurückgegeben.** Andernfalls wird ein **NTSTATUS-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Anstatt diese Funktion zu verwenden, sollten Anwendungen eine der folgenden Funktionen aufrufen:

-   [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

Dieser Funktion ist keine Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Gdi32.dll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Funktionen](opm-functions.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> </dl>

 

 
