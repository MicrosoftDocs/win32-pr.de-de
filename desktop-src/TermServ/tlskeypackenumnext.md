---
title: TLSKeyPackEnumNext-Funktion
description: Setzt einen vorherigen Aufruf der TLSKeyPackEnumBegin-Funktion fort und gibt das nächste Schlüsselpaket zurück, das auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumNext-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352d94204e4c590668018546f0d6304d4faa3836bcc7289b675b05b1ae2b825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869260"
---
# <a name="tlskeypackenumnext-function"></a>TLSKeyPackEnumNext-Funktion

Setzt einen vorherigen Aufruf der [**TLSKeyPackEnumBegin-Funktion**](tlskeypackenumbegin.md) fort und gibt das nächste Schlüsselpaket zurück, das auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mstlsapi.dll herzustellen.

 

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ In\]
</dt> <dd>

Verarbeiten eines Remotedesktop Lizenzservers. Geben Sie ein Handle an, das von der [**TLSConnectToLsServer-Funktion**](tlsconnecttolsserver.md) geöffnet wird.

</dd> <dt>

*lpKeyPack* \[ In\]
</dt> <dd>

Zeiger auf eine [**LSKeyPack-Struktur,**](lskeypack.md) die das nächste Schlüsselpaket empfängt, das den Suchkriterien entspricht.

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

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ I \_ NO \_ MORE \_ DATA** (4001)


</dt> <dd>

Keine weiteren Schlüsselpakete, die den Suchkriterien entsprechen.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ INTERNER \_ FEHLER** (5001)


</dt> <dd>

Interner Fehler auf dem Lizenzserver.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ UNGÜLTIGE \_ SEQUENZ** (5006)


</dt> <dd>

Die aufrufende Sequenz war ungültig. Muss zuvor die [**TLSKeyPackEnumBegin()-Funktion**](tlskeypackenumbegin.md) aufrufen.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ AUSGELASTET** (5007)


</dt> <dd>

Der Lizenzserver ist zu stark ausgelastet, um die Anforderung zu verarbeiten.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

Der Aufruf war erfolgreich. Überprüfen Sie den Wert des *pdwErrCode-Parameters,* um den Rückgabecode für den Aufruf abzurufen.

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

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

