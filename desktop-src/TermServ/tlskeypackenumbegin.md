---
title: TLSKeyPackEnumBegin-Funktion
description: Beginnt mit der Enumeration über alle Schlüsselpakete, die auf einem Remotedesktop Lizenzserver basierend auf Suchkriterien installiert sind.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumBegin-Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469e4e255f3bdd64749060fcb712df480a8a1f6fc3683ebb25916be44856e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869330"
---
# <a name="tlskeypackenumbegin-function"></a>TLSKeyPackEnumBegin-Funktion

Beginnt mit der Enumeration über alle Schlüsselpakete, die auf einem Remotedesktop Lizenzserver basierend auf Suchkriterien installiert sind.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mstlsapi.dll.

 

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ In\]
</dt> <dd>

Handle für einen Remotedesktop Lizenzserver. Geben Sie ein Handle an, das von der [**TLSConnectToLsServer-Funktion geöffnet**](tlsconnecttolsserver.md) wird.

</dd> <dt>

*dwSearchParm* \[ In\]
</dt> <dd>

Gibt die Suchkriterien an. Dieser Parameter ist für die zukünftige Verwendung reserviert und muss 0xFFFFFFFF.

</dd> <dt>

*bMatchAll* \[ In\]
</dt> <dd>

Gibt an, ob alle Suchwerte übereinstimmen.

</dd> <dt>

*lpSearchParm* \[ In\]
</dt> <dd>

Zeiger auf eine [**LSKeyPack-Struktur,**](lskeypack.md) die die Suchparameter angibt, nach denen gesucht werden soll.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ SUCCESS** (0)


</dt> <dd>

Der Aufruf ist erfolgreich.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ INTERNER \_ \_ E-FEHLER** (5001)


</dt> <dd>

Interner Fehler auf dem Lizenzserver.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ \_ UNGÜLTIGE SEQUENZ** (5006)


</dt> <dd>

Die aufrufende Sequenz war ungültig. Höchstwahrscheinlich wurde eine vorherige Enumeration nicht beendet.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ AUSGELASTET** (5007)


</dt> <dd>

Der Lizenzserver ist zu ausgelastet, um die Anforderung zu verarbeiten.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ UNGÜLTIGE DATEN** (5009)


</dt> <dd>

Daten im Suchparameter sind ungültig.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

Der Aufruf war erfolgreich. Überprüfen Sie den Wert des *pdwErrCode-Parameters,* um den Rückgabecode für den Aufruf zu erhalten.

</dd> <dt>

**RPC \_ S \_ INVALID \_ ARG**
</dt> <dd>

Das Argument war ungültig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

