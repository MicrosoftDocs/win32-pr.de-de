---
description: Die inetgetautodial-Funktion gibt die AutoDial-Einstellungen aus der Registrierung zurück.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: Inetgetautodial-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359710"
---
# <a name="inetgetautodial-function"></a>Inetgetautodial-Funktion

\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Windows-Versionen geändert oder nicht verfügbar sein. \]

Die **inetgetautodial** -Funktion gibt die AutoDial-Einstellungen aus der Registrierung zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpfenable* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob AutoDial aktiviert ist. Der Wert **true** bei Return gibt an, dass AutoDial aktiviert ist.

</dd> <dt>

*lpszentryname* \[ vorgenommen\]
</dt> <dd>

Enthält bei der Rückgabe den Namen des Telefonbucheintrags, der für AutoDial festgelegt ist.

</dd> <dt>

*cbentrynamesize* \[ in\]
</dt> <dd>

Größe des Puffers, der vom Aufrufer für den Namen des Telefonbucheintrags zugewiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Fehler \_ erfolgreich**</dt> </dl>              | Der Aufruf war erfolgreich.<br/>                                                                                                                       |
| <dl> <dt>**Ungültige Argumente für Fehler \_ \_**</dt> </dl>       | *lpfenable* oder *lpszentryname* enthält einen **null** -Zeiger, oder der Wert von *cbentrynamesize* ist 0 (null).<br/>                                         |
| <dl> <dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt> </dl>  | Es war nicht genügend Arbeitsspeicher zum Zuordnen interner Puffer vorhanden.<br/>                                                                                    |
| <dl> <dt>**Fehler \_ beim \_ Puffer.**</dt> </dl> | *cbentrynamesize* gibt nicht an, dass der Puffer, auf den von *lpszentryname* verwiesen wird, groß genug ist, um den Namen des Telefonbucheintrags zu erhalten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
