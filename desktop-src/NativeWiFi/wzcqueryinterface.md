---
description: Enthält ausführliche Informationen zu einer WLAN-Schnittstelle, die vom Wireless Zero Configuration-Dienst verwaltet wird.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: WZCQueryInterface-Funktion (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3dd7ce876501486b9bec4dbad63ce5812b910b32b9dcdaa1eb80aff3e7cc415e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797410"
---
# <a name="wzcqueryinterface-function"></a>WZCQueryInterface-Funktion

\[**WZCQueryInterface** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie [**stattdessen die WlanQueryInterface-Funktion.**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) Weitere Informationen finden Sie unter [Informationen zur Native Wifi-API.](about-the-native-wifi-api.md) \]

Die **WZCQueryInterface-Funktion** enthält ausführliche Informationen zu einer wlan-Schnittstelle, die vom Wireless Zero Configuration-Dienst verwaltet wird.

Stellt ausführliche Informationen für eine bestimmte Schnittstelle bereit.

## <a name="syntax"></a>Syntax


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrvAddr* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll. Wenn dieser Parameter **NULL ist,** wird der Wireless Zero Configuration-Dienst auf dem lokalen Computer abgefragt.

Wenn der *angegebene pSrvAddr-Parameter* ein Remotecomputer ist, muss der Remotecomputer REMOTE-RPC-Aufrufe unterstützen.

</dd> <dt>

*dwInFlags* \[ In\]
</dt> <dd>

Die felder, die abgefragt werden sollen. Dies ist eine Bitmaske, die eine beliebige Kombination der folgenden Flags enthalten kann.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ DYNFLAGS-0x00000010**</dt> <dt></dt> </dl>             | Gibt den Wert für den **dwDynFlags-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ DESCR**</dt> <dt>0x00010000</dt> </dl>                      | Gibt den Wert für den **wszDescr-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA-0x00020000**</dt> <dt></dt> </dl>          | Gibt die Werte für **die Member ulMediaState,** **ulMediaType** und **ulPhysicalMediaType** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ PREFLIST-0x00040000**</dt> <dt></dt> </dl>             | Gibt die bevorzugte Liste der Netzwerke im **rdStSSIDList-Member** der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ CAPABILITIES**</dt> <dt>0x00080000</dt> </dl> | Gibt die Werte für **die dwCapabilities-** und **rdNicCapabilities-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter zeigt.*<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_ INFRAMODE-0x00200000**</dt> <dt></dt> </dl>          | Gibt den Wert für den **nInfraMode-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/> Der **nInfraMode-Member** ist nur in einigen Schnittstellenkontextzuständen gültig.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ AUTHMODE-0x00400000**</dt> <dt></dt> </dl>             | Gibt den Wert für den **nAuthMode-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt. <br/> Der **nAuthMode-Member** ist nur in einigen Schnittstellenkontextzuständen gültig.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ WEPSTATUS-0x00800000**</dt> <dt></dt> </dl>          | Gibt den Wert für das **nWepStatus-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt. <br/> Der **nWepStatus-Member** ist nur in einigen Schnittstellenkontextzuständen gültig.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID-0x01000000**</dt> <dt></dt> </dl>                         | Gibt den Wert für den **rdSSID-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/> Der **rdSSID-Member** ist nur in einigen Schnittstellenkontextzuständen gültig.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID-0x02000000**</dt> <dt></dt> </dl>                      | Gibt den Wert für das **rdBSSID-Member** in der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf das der *pIntf-Parameter* zeigt.<br/> Der **rdBSSID-Member** ist nur in einigen Schnittstellenkontextzuständen gültig.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ BSSIDLIST-0x04000000**</dt> <dt></dt> </dl>          | Gibt die sichtbare Liste der Netzwerke im **rdBSSIDList-Member** der [**INTF \_ ENTRY-Struktur**](intf-entry.md) zurück, auf die der *pIntf-Parameter* zeigt.<br/> Der **rdBSSIDList-Member** ist nur in einigen Schnittstellenkontextzuständen gültig.<br/> |



 

</dd> <dt>

*pIntf* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf den Schlüssel der zu abfragenden Schnittstelle. Bei der Ausgabe ein Zeiger auf die angeforderten Schnittstellendaten. Dieser Parameter ist ein Zeiger auf eine [**INTF \_ ENTRY-Struktur.**](intf-entry.md)

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Ein Satz von Feldern wurde erfolgreich abgerufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.



| Rückgabecode                                                                                               | Beschreibung                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ BEIM \_ PAPIERKORB**</dt> </dl>      | Die Speicherkontrollblöcke wurden zerstört. Dieser Fehler wird zurückgegeben, wenn der Wireless Zero Configuration-Dienst keine internen Objekte initialisiert hat.<br/>                                                                                                                      |
| <dl> <dt>**FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>    | Die angegebene Datei wurde nicht gefunden. Dieser Fehler wird zurückgegeben, wenn die GUID im **wszGuid-Member** der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf die der *pIntf-Parameter* verweist, nicht mit einer der WLAN-Schnittstellen auf dem lokalen Computer übereinstimmen. <br/> |
| <dl> <dt>**FEHLER \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl>  | Ein Parameter ist falsch. Dieser Fehler wird zurückgegeben, wenn *der pIntf-Parameter* **NULL ist.** Dieser Fehler wird zurückgegeben, wenn der **wszGuid-Member** der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf die der *pIntf-Parameter* verweist, **NULL ist.** <br/>                            |
| <dl> <dt>**FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung zu verarbeiten und Arbeitsspeicher für die Abfrageergebnisse zu reservieren.<br/>                                                                                                                                                                       |
| <dl> <dt>**\_RPC-STATUS**</dt> </dl>                | Verschiedene Fehlercodes.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Hinweise

Der **wszGuid-Member** der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf die der *pIntf-Parameter* zeigt, muss eine Schnittstellen-GUID für eine DRAHTLOSE LAN-Schnittstelle enthalten. Eine Liste der WLAN-Schnittstellen kann durch Aufrufen der [**WZCEnumInterfaces-Funktion abgerufen**](wzcenuminterfaces.md) werden.

Die folgenden Member der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf die *pIntf* zeigt, müssen vor einem Aufruf der **WZCQueryInterface-Funktion** auf 0 festgelegt werden: **rdSSID,** **rdBSSID,** **rdBSSIDList,** **rdStSSIDList** und **rdCtrlData**.

Der Drahtlose Zero Configuration-Dienst aktualisiert den Medienzustand selbst dann nicht automatisch, wenn ereignisse empfangen werden, die mit medien verbundenen und getrennten Medien verbunden sind. Eine Anwendung sollte eine Aktualisierung des Medienzustands erzwingen, indem sie die [**WZCRefreshInterface-Funktion**](wzcrefreshinterface.md) aufruft, bevor sie die **WZCQueryInterface-Funktion** aufruft, wenn der NDIS-Medienzustand angefordert werden soll (das INTF NDISMEDIA-Bit wird im \_ *dwInFlags-Parameter* festgelegt).

Wenn der *dwInFlags-Parameter* **INTF \_ BSSIDLIST** enthält, wird von der **WZCQueryInterface-Funktion** nicht *dwOutFlags* mit **INTF \_ BSSIDLIST** festgelegt, wenn die sichtbare Liste der Netzwerke leer ist. Wenn der *dwInFlags-Parameter* **INTF \_ SSID** enthält, wird von der **WZCQueryInterface-Funktion** *nicht dwOutFlags* mit **INTF \_ SSID** festgelegt, wenn keine SSID verfügbar ist.

Wenn die **WZCQueryInterface-Funktion** ERROR SUCCESS zurückgibt, sollte der Aufrufer die LocalFree-Funktion mit dem \_ *pIntf-Parameter* aufrufen, um die internen Puffer frei zu geben, die für die zurückgegebenen Daten zugeordnet sind, sobald diese Informationen nicht mehr benötigt werden. [](/windows/win32/api/winbase/nf-winbase-localfree) Dadurch werden die Puffer, die von den **RdSSID-,** **rdBSSID-,** **rdBSSIDList-,** **rdStSSIDList-** und **rdCtrlData-Membern** der [**INTF \_ ENTRY-Struktur**](intf-entry.md) verwendet werden, auf die vom *pIntf-Parameter* verwiesen wird, frei.

> [!Note]  
> Die *Wzcsapi.h-Headerdatei* und *die Wzcsapi.lib-Importbibliotheksdatei* sind im Windows SDK nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP mit SP3<br/>                                                         |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_INTF-EINTRAG**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
