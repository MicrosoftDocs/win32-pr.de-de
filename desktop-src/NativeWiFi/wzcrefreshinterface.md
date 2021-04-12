---
description: Aktualisiert Schnittstellen Informationen für eine bestimmte drahtlose LAN-Schnittstelle.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Wzkrefreshinterface-Funktion (wzcsapi. h)
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
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348109"
---
# <a name="wzcrefreshinterface-function"></a>Wzkrefreshinterface-Funktion

\[**Wzkrefreshinterface** wird ab Windows Vista und Windows Server 2008 nicht unterstützt. Verwenden Sie stattdessen die [native WiFi-API](native-wifi-reference.md), die eine ähnliche Funktionalität bietet. Weitere Informationen finden Sie unter Informationen zur [nativen WiFi-API](about-the-native-wifi-api.md).\]

Die **wzkrefreshinterface** -Funktion aktualisiert Schnittstellen Informationen für eine bestimmte drahtlose LAN-Schnittstelle.

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

*psrvaddr* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Computers enthält, auf dem diese Funktion ausgeführt werden soll. Wenn dieser Parameter **null** ist, wird der Konfigurations Dienst für drahtlose NULL auf dem lokalen Computer aufgerufen.

Wenn der angegebene *psrvaddr* -Parameter ein Remote Computer ist, muss der Remote Computer Remote-RPC-Aufrufe unterstützen.

</dd> <dt>

*dwInFlags* \[ in\]
</dt> <dd>

Eine Gruppe von Feldern, die zusammen mit bestimmten Aktualisierungs Aktionen aktualisiert werden sollen. Dabei handelt es sich um eine Bitmaske, die eine beliebige Kombination der folgenden Flags enthalten kann.



| Wert                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_ Descr**</dt> <dt>0x00010000 bis</dt> </dl>             | Aktualisieren Sie die Schnittstellen Beschreibung für eine drahtlose LAN-Schnittstelle.<br/> Die aktualisierte Schnittstellen Beschreibung kann abgerufen werden, indem Sie die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion aufrufen, wobei das **INTF- \_ descr** -Bit im *dwInFlags* -Parameter festgelegt ist. Die Schnittstellen Beschreibung wird im **wszdescr** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurückgegeben, auf den der *pintf* -Parameter verweist, der von der **wzcqueryinterface** -Funktion zurückgegeben wird.<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_ Ndismedia**</dt> <dt>0x00020000</dt> </dl> | Aktualisieren Sie die NDIS-Medieninformationen für eine drahtlose LAN-Schnittstelle.<br/> Die aktualisierten NDIS-Medieninformationen können abgerufen werden, indem Sie die [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion mit dem **INTF \_ ndismedia** -Bit aufrufen, das im *dwInFlags* -Parameter festgelegt ist. Die NDIS-Medieninformationen werden in den Elementen **ulmediastate**, **ulmediatype** und **ulphysicalmediatype** der [**INTF- \_ Eintrags**](intf-entry.md) Struktur zurückgegeben, auf die durch den *pintf* -Parameter verwiesen wird, der von der **wzcqueryinterface** -Funktion zurückgegeben wird.<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_ Alle \_ OIDs**</dt> <dt>0xfff00000</dt> </dl>   | Aktualisieren Sie alle NDIS-OIDs für eine drahtlose LAN-Schnittstelle. Mit dieser Option werden die meisten Daten für eine drahtlose LAN-Schnittstelle aktualisiert.<br/> Die aktualisierten Informationen können durch Aufrufen der [**wzcqueryinterface**](wzcqueryinterface.md) -Funktion abgerufen werden.<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pintf* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**INTF- \_ Eintrags**](intf-entry.md) Struktur, die den Schlüssel der zu aktualisierenden Schnittstelle enthält.

</dd> <dt>

*pdwOutFlags* \[ vorgenommen\]
</dt> <dd>

Ein Satz von Feldern, die erfolgreich aktualisiert wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Rückgabecodes sein.



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler-Arena wurde durchlaufen \_ \_**</dt> </dl>     | Die Speicher Kontroll Blöcke wurden zerstört. Dieser Fehler wird zurückgegeben, wenn der Konfigurations Dienst für drahtlose NULL keine internen Objekte initialisiert hat.<br/>                                                                                                                      |
| <dl> <dt>**Fehler \_ Datei \_ nicht \_ gefunden.**</dt> </dl>   | Die angegebene Datei wurde nicht gefunden. Dieser Fehler wird zurückgegeben, wenn die GUID im **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, nicht mit einer der Drahtlos-LAN-Schnittstellen auf dem lokalen Computer entsprach. <br/> |
| <dl> <dt>**Fehler bei \_ ungültigem \_ Parameter**</dt> </dl> | Ein Parameter ist falsch. Dieser Fehler wird zurückgegeben, wenn der *pintf* -Parameter **null** ist. Dieser Fehler wird zurückgegeben, wenn das **wszguid** -Element der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf die durch den *pintf* -Parameter verwiesen wird, **null** ist. <br/>                            |
| <dl> <dt>**RPC- \_ Status**</dt> </dl>               | Verschiedene Fehlercodes.<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Der **wszguid** -Member der [**INTF- \_ Eintrags**](intf-entry.md) Struktur, auf den der *pintf* -Parameter verweist, muss eine Schnittstellen-GUID für eine drahtlose LAN-Schnittstelle enthalten. Eine Liste der Drahtlos-LAN-Schnittstellen kann durch Aufrufen der [**wzcenumschlag Interfaces**](wzcenuminterfaces.md) -Funktion abgerufen werden.

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

[**Wzceapolgetinterfaceparametriams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**Wzcenumschlag-Schnittstellen**](wzcenuminterfaces.md)
</dt> <dt>

[**Wzcqueryinterface**](wzcqueryinterface.md)
</dt> <dt>

[**INTF- \_ Eintrag**](intf-entry.md)
</dt> </dl>

 

 




