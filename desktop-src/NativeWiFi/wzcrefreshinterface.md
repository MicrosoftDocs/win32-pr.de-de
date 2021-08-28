---
description: Aktualisiert Schnittstelleninformationen für eine bestimmte WLAN-Schnittstelle.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: WZCRefreshInterface-Funktion (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 43f2b35215c930517d5352073c679a116388eb49aaa3bd6a3c567467e50be1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064510"
---
# <a name="wzcrefreshinterface-function"></a>WZCRefreshInterface-Funktion

\[**WZCRefreshInterface** wird ab Windows Vista und Windows Server 2008 nicht unterstützt. Verwenden Sie stattdessen die [Native Wifi-API](native-wifi-reference.md), die ähnliche Funktionen bereitstellt. Weitere Informationen finden Sie unter [Informationen zur Native Wifi-API.](about-the-native-wifi-api.md)\]

Die **WZCRefreshInterface-Funktion** aktualisiert Schnittstelleninformationen für eine bestimmte WLAN-Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSrvAddr* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll. Wenn dieser Parameter **NULL** ist, wird der Wireless Zero Configuration-Dienst auf dem lokalen Computer aufgerufen.

Wenn der angegebene *pSrvAddr-Parameter* ein Remotecomputer ist, muss der Remotecomputer Remote-RPC-Aufrufe unterstützen.

</dd> <dt>

*dwInFlags* \[ In\]
</dt> <dd>

Eine Gruppe von Feldern, die aktualisiert werden sollen, zusammen mit bestimmten Aktualisierungsaktionen, die ausgeführt werden sollen. Dies ist eine Bitmaske, die eine beliebige Kombination der folgenden Flags enthalten kann.



| Wert                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ DESCR**</dt> <dt>0x00010000</dt> </dl>             | Aktualisieren Sie die Schnittstellenbeschreibung für eine WLAN-Schnittstelle.<br/> Die aktualisierte Schnittstellenbeschreibung kann durch Aufrufen der [**WZCQueryInterface-Funktion**](wzcqueryinterface.md) abgerufen werden, wobei das **INTF \_ DESCR-Bit** im *dwInFlags-Parameter* festgelegt ist. Die Schnittstellenbeschreibung wird im **wszDescr-Member** der [**INTF \_ ENTRY-Struktur zurückgegeben,**](intf-entry.md) auf die der *pIntf-Parameter* zeigt, der von der **WZCQueryInterface-Funktion** zurückgegeben wird.<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | Aktualisieren Sie die NDIS-Medieninformationen für eine WLAN-Schnittstelle.<br/> Die aktualisierten NDIS-Medieninformationen können durch Aufrufen der [**WZCQueryInterface-Funktion**](wzcqueryinterface.md) abgerufen werden, wobei das **INTF \_ NDISMEDIA-Bit** im *dwInFlags-Parameter* festgelegt ist. Die NDIS-Medieninformationen werden in den **Membern ulMediaState,** **ulMediaType** und **ulPhysicalMediaType** der [**INTF \_ ENTRY-Struktur zurückgegeben,**](intf-entry.md) auf die der *pIntf-Parameter* zeigt, der von der **WZCQueryInterface-Funktion** zurückgegeben wird.<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ ALL \_ OIDS**</dt> <dt>0xFFF00000</dt> </dl>   | Aktualisieren Sie alle NDIS-OIDs für eine WLAN-Schnittstelle. Mit dieser Option werden die meisten Daten für eine WLAN-Schnittstelle aktualisiert.<br/> Die aktualisierten Informationen können durch Aufrufen der [**WZCQueryInterface-Funktion**](wzcqueryinterface.md) abgerufen werden.<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**INTF \_ ENTRY-Struktur,**](intf-entry.md) die den Schlüssel der zu aktualisierenden Schnittstelle enthält.

</dd> <dt>

*pdwOutFlags* \[ out\]
</dt> <dd>

Eine Gruppe von Feldern, die erfolgreich aktualisiert wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FEHLER \_ IM \_ PAPIERKORB**</dt> </dl>     | Die Speicherkontrollblöcke wurden zerstört. Dieser Fehler wird zurückgegeben, wenn der Wireless Zero Configuration-Dienst keine internen Objekte initialisiert hat.<br/>                                                                                                                      |
| <dl> <dt>**FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>   | Die angegebene Datei wurde nicht gefunden. Dieser Fehler wird zurückgegeben, wenn die GUID im **wszGuid-Member** der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf die der *pIntf-Parameter* zeigt, keiner der WLAN-Schnittstellen auf dem lokalen Computer entspricht. <br/> |
| <dl> <dt>**FEHLER: \_ UNGÜLTIGER \_ PARAMETER**</dt> </dl> | Ein Parameter ist falsch. Dieser Fehler wird zurückgegeben, wenn der *pIntf-Parameter* **NULL** ist. Dieser Fehler wird zurückgegeben, wenn der **wszGuid-Member** der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf die der *pIntf-Parameter* zeigt, **NULL** ist. <br/>                            |
| <dl> <dt>**\_RPC-STATUS**</dt> </dl>               | Verschiedene Fehlercodes.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Hinweise

Der **wszGuid-Member** der [**INTF \_ ENTRY-Struktur,**](intf-entry.md) auf den der *pIntf-Parameter* zeigt, muss eine Schnittstellen-GUID für eine WLAN-Schnittstelle enthalten. Eine Liste der WLAN-Schnittstellen kann durch Aufrufen der [**WZCEnumInterfaces-Funktion**](wzcenuminterfaces.md) abgerufen werden.

> [!Note]  
> Die *Headerdatei "Wzcsapi.h"* und die Importbibliotheksdatei *"Wzcsapi.lib"* sind im Windows SDK nicht verfügbar.

 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**\_INTF-EINTRAG**](intf-entry.md)
</dt> </dl>

 

 




