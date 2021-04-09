---
description: Stellt ausführliche Informationen für eine drahtlose LAN-Schnittstelle bereit, die vom drahtlos Konfigurations Dienst für drahtlose Netzwerke verwaltet wird.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Wzcqueryinterface-Funktion (wzcsapi. h)
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
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867903"
---
# <a name="wzcqueryinterface-function"></a>Wzcqueryinterface-Funktion

\[**Wzcqueryinterface** wird ab Windows Vista und Windows Server 2008 nicht mehr unterstützt. Verwenden Sie stattdessen die Funktion [**wlanqueryinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) . Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md). \]

Die **wzcqueryinterface** -Funktion stellt ausführliche Informationen für eine drahtlose LAN-Schnittstelle bereit, die vom drahtlos Konfigurations Dienst für drahtlose Daten verwaltet wird.

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

*psrvaddr* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll. Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL auf dem lokalen Computer abgefragt.

Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.

</dd> <dt>

*dwInFlags* \[ in\]
</dt> <dd>

Die Felder, die abgefragt werden sollen. Dabei handelt es sich um eine Bitmaske, die eine beliebige Kombination der folgenden Flags enthalten kann.



| Wert                                                                                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_ Dynflags**</dt> <dt>0x00000010</dt> </dl>             | Gibt den Wert für den **dwdynflags** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ Descr**</dt> <dt>0x00010000 bis</dt> </dl>                      | Gibt den Wert für den **wszdescr** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ Ndismedia**</dt> <dt>0x00020000</dt> </dl>          | Gibt die Werte für die Member **ulmediastate**, **ulmediatype** und **ulphysicalmediatype** in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_ Preflist**</dt> <dt>0x00040000</dt> </dl>             | Gibt die bevorzugte Liste von Netzwerken im **rdstssidlist** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_ Funktionen**</dt> <dt>0x00080000</dt> </dl> | Gibt die Werte für die **DW-Funktionen** und die **rdniccapabili-** Elemente in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_ Inframode**</dt> <dt>0x00200000</dt> </dl>          | Gibt den Wert für das **ninframode** -Element in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.<br/> Der **ninframode** -Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_ Authmode**</dt> <dt>0x00400000</dt> </dl>             | Gibt den Wert für den **nauthmode** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist. <br/> Der **nauthmode** -Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_ Wepstatus**</dt> <dt>0x00800000</dt> </dl>          | Gibt den Wert für den **nwepstatus** -Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist. <br/> Der **nwepstatus** -Member ist nur in bestimmten Schnittstellen Kontext Zuständen gültig.<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_ SSID**</dt> <dt>0x01000000</dt> </dl>                         | Gibt den Wert für den **rdssid-** Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.<br/> Der **rdssid-** Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt> </dl>                      | Gibt den Wert für den **rdbssid-** Member in der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf den der *pintf* -Parameter verweist.<br/> Der **rdbssid-** Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_ Bssidlist**</dt> <dt>0x04000000</dt> </dl>          | Gibt die sichtbare Liste der Netzwerke im **rdbssidlist** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurück, auf die durch den *pintf* -Parameter verwiesen wird.<br/> Der **rdbssidlist** -Member ist nur in einigen Schnittstellen Kontext Zuständen gültig.<br/> |



 

</dd> <dt>

*pintf* \[ in, out\]
</dt> <dd>

Bei Eingabe ein Zeiger auf den Schlüssel der abzufragende Schnittstelle. Bei der Ausgabe ein Zeiger auf die angeforderten Schnittstellen Daten. Dieser Parameter ist ein Zeiger auf eine [**INTF- \_ Eintrags**](intf-entry.md) Struktur.

</dd> <dt>

*pdwOutFlags* \[ vorgenommen\]
</dt> <dd>

Eine Reihe von Feldern, die erfolgreich abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.



| Rückgabecode                                                                                               | Beschreibung                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler-Arena wurde durchlaufen \_ \_**</dt> </dl>      | Die Speicher Kontroll Blöcke wurden zerstört. Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL keine internen Objekte initialisiert hat.<br/>                                                                                                                      |
| <dl> <dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt> </dl>    | Die angegebene Datei wurde nicht gefunden. Dieser Fehler wird zurückgegeben, wenn die GUID im **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, nicht mit einer der Drahtlos-LAN-Schnittstellen auf dem lokalen Computer entsprach. <br/> |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl>  | Ein Parameter ist falsch. Dieser Fehler wird zurückgegeben, wenn der *pintf* -Parameter **null** ist. Dieser Fehler wird zurückgegeben, wenn das **wszguid** -Element der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, **null** ist. <br/>                            |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung zu verarbeiten und Arbeitsspeicher für die Abfrageergebnisse zuzuweisen.<br/>                                                                                                                                                                       |
| <dl> <dt>**RPC- \_ Status**</dt> </dl>                | Verschiedene Fehlercodes.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Der **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf den der *pintf* -Parameter verweist, muss eine Schnittstellen-GUID für eine drahtlose LAN-Schnittstelle enthalten. Eine Liste der Drahtlos-LAN-Schnittstellen kann durch Aufrufen der [**wzcenumschlag Interfaces**](wzcenuminterfaces.md) -Funktion abgerufen werden.

Die folgenden Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die von *pintf* verwiesen wird, müssen vor einem **wzcqueryinterface** -Befehl auf 0 festgelegt werden: **rdssid**, **rdbssid**, **rdbssidlist**, **rdstssidlist** und **rdctrldata**.

Der Konfigurations Dienst für drahtlose NULL-Werte aktualisiert den Medien Status nicht in einer Weise, auch wenn Medien verbundene und getrennte Ereignisse empfangen werden. Eine Anwendung sollte eine Medien Zustands Aktualisierung erzwingen, indem Sie die [**wzcrefreshinterface**](wzcrefreshinterface.md) -Funktion aufrufen, bevor Sie die **wzcqueryinterface** -Funktion aufrufen, wenn der NDIS-Medien Zustand angefordert werden soll (Das INTF \_ ndismedia-Bit wird im *dwInFlags* -Parameter festgelegt).

Wenn der *dwInFlags* -Parameter **INTF- \_ bssidlist** enthält, legt die **wzcqueryinterface** -Funktion nicht die-Eigenschaft " *dwoutflags* " mit **INTF \_ bssidlist** fest, wenn die sichtbare Liste der Netzwerke leer ist. Wenn der *dwInFlags* -Parameter **INTF \_ SSID** enthält, werden die *dwoutflags* von der **wzcqueryinterface** -Funktion nicht mit **INTF \_ SSID** festgelegt, wenn keine SSID verfügbar ist.

Wenn die **wzcqueryinterface** -Funktion den Fehler Erfolg zurückgibt \_ , sollte der Aufrufer die [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) -Funktion mit dem *pintf* -Parameter aufrufen, um die für die zurückgegebenen Daten zugewiesenen internen Puffer freizugeben, sobald diese Informationen nicht mehr benötigt werden. Dadurch werden die Puffer freigegeben, die von den Elementen **rdssid**, **rdbssid**, **rdbssidlist**, **rdstssidlist** und **rdctrldata** der [**INTF- \_ Eintrags**](intf-entry.md) Struktur verwendet werden, auf die durch den *pintf* -Parameter verwiesen wird.

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

[**INTF- \_ Eintrag**](intf-entry.md)
</dt> <dt>

[**Wzceapolgetinterfaceparametriams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**Wzcenumschlag-Schnittstellen**](wzcenuminterfaces.md)
</dt> <dt>

[**Wzkrefreshinterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
