---
description: Ruft EAPOL-Konfigurationsparameter für die angegebene Wireless LAN-Schnittstelle ab.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Wzceapolgetinterfacesamams-Funktion (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356993"
---
# <a name="wzceapolgetinterfaceparams-function"></a>Wzceapolgetinterfaceparser-Funktion

\[**Wzceapolgetinterfaceparser** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

Die **wzceapolgetinterfaceparser** -Funktion ruft EAPOL-Konfigurationsparameter für die angegebene drahtlose LAN-Schnittstelle ab.

## <a name="syntax"></a>Syntax


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psrvaddr* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll. Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL auf dem lokalen Computer aufgerufen.

Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.

</dd> <dt>

*pwszguid* \[ in\]
</dt> <dd>

Der GUID der Schnittstelle, für die Daten abgerufen werden sollen.

</dd> <dt>

*dwsizeofssid* \[ in\]
</dt> <dd>

Die Größe des Netzwerk Bezeichners, für den die Daten abgerufen werden sollen.

</dd> <dt>

*pbssid* \[ in\]
</dt> <dd>

Ein Zeiger auf den Netzwerk Bezeichner, für den Daten abgerufen werden sollen.

</dd> <dt>

*pintfparametriams* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**EAPOL \_ INTF \_**](eapol-intf-params.md) -Parameter Struktur, die Schnittstellenparameter enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Erfolg des Fehlers zurück, \_ Wenn der Vorgang erfolgreich abgeschlossen wurde. andernfalls wird einer der Windows-Systemfehler Codes zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn **wzceapolgetinterfaceparser** einen Fehler Erfolg zurückgibt \_ , sollte der Aufrufer [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) aufrufen, um die für die zurückgegebenen Daten zugewiesenen internen Puffer freizugeben, sobald diese Informationen nicht mehr benötigt werden.

> [!Note]  
> Die Header Datei " *wzcsapi. h* " und die Datei " *wzcsapi. lib* Import Library" sind im Windows SDK nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                         |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wzcenumschlag-Schnittstellen**](wzcenuminterfaces.md)
</dt> <dt>

[**Wzcqueryinterface**](wzcqueryinterface.md)
</dt> <dt>

[**Wzkrefreshinterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
