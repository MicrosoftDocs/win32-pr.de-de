---
title: TLSKeyPackEnumEnd-Funktion
description: Setzt einen vorherigen Aufruf der TLSKeyPackEnumBegin-Funktion fort und beendet die -Enumeration.
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumEnd-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 176c5d6b03fabe2e085b2582043233cd5fdc2681ef04ef07723ba5435a465863
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986920"
---
# <a name="tlskeypackenumend-function"></a>TLSKeyPackEnumEnd-Funktion

Setzt einen vorherigen Aufruf der [**TLSKeyPackEnumBegin-Funktion**](tlskeypackenumbegin.md) fort und beendet die -Enumeration.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mstlsapi.dll herzustellen.

 

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ In\]
</dt> <dd>

Verarbeiten eines Remotedesktop Lizenzservers. Geben Sie ein Handle an, das von der [**TLSConnectToLsServer-Funktion**](tlsconnecttolsserver.md) geöffnet wird.

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

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ E \_ \_ UNGÜLTIGES HANDLE** (5005)


</dt> <dd>

Das Handle ist ungültig.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> </dl>

 

