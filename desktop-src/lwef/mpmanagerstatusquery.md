---
title: Mpmanagerstatus Query-Funktion (mpclient. h)
description: Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück. | Mpmanagerstatus Query-Funktion (mpclient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Mpmanagerstatus Query-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352249"
---
# <a name="mpmanagerstatusquery-function"></a>Mpmanagerstatus Query-Funktion

\[**Mpmanagerstatus Query** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [**mpmanagerstatus-QUERYEX**](mpmanagerstatusqueryex.md).\]

Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*pstatusinfo* \[ vorgenommen\]
</dt> <dd>

Typ: **pmpstatus- \_ Informationen**

Zeiger auf eine-Struktur, die Statusinformationen zu den letzten Scans, aktiven Bedrohungen und verschiedenen Komponenten Status zurückgibt. Siehe [**mpstatus- \_ Informationen**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**. Dieser Funktions Aufrufvorgang ist garantiert auch dann erfolgreich, wenn kein antischadsoftwaredienst ausgeführt wird.

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

[**Mpmanagerstatus-QUERYEX**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**mpstatus- \_ Informationen**](mpstatus-info.md)
</dt> </dl>

 

 





