---
description: Konvertiert einen Gebietsschemanamen in einen Gebietsschemabezeichner, der zum Abrufen von Informationen aus dem Betriebssystem verwendet werden kann.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: DownlevelLocaleNameToLCID-Funktion (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 39a0a6b274ba141553d2ddda927f71754cc9639ff5fc3a0d3870a974e46526a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898730"
---
# <a name="downlevellocalenametolcid-function"></a>DownlevelLocaleNameToLCID-Funktion

Konvertiert einen [Gebietsschemanamen](locale-names.md) in einen [Gebietsschemabezeichner,](locale-identifiers.md) der zum Abrufen von Informationen aus dem Betriebssystem verwendet werden kann.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die unter Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert ein Downloadpaket. Anwendungen, die nur auf Windows Vista und höher ausgeführt werden, sollten [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) aufrufen, um einen Gebietsschemabezeichner abzurufen.

 

## <a name="syntax"></a>Syntax


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpName* \[ In\]
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die einen [Gebietsschemanamen](locale-names.md)darstellt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die den Typ des Namens angeben. Der Standardwert ist DOWNLEVEL \_ LOCALE \_ NAME.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Gebietsschemabezeichner zurück, der dem Gebietsschemanamen entspricht.

Die Funktion gibt 0 zurück, wenn sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER \_ \_ UNGÜLTIGE FLAGS. Die für Flags angegebenen Werte waren ungültig.
-   FEHLER: \_ UNGÜLTIGER \_ PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Diese Funktion unterstützt keine neutralen Gebietsschemas. Die entsprechende [**LocaleNameToLCID-Funktion**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) unterstützt [benutzerdefinierte Gebietsschemas,](custom-locales.md)jedoch nur für Windows Vista und höher.

 

Die erforderliche Headerdatei und DLL sind Teil des Downloads "Downlevel Data Mapping APIs" von Microsoft NLS, der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                |
| Verteilbare Komponente<br/>          | Microsoft NLS Downlevel Data Mapping APIs onWindows XP with SP2 and laterorWindows Vista<br/> |
| Header<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützung für nationale Sprachen](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Zuordnen von Gebietsschemadaten](mapping-locale-data.md)
</dt> <dt>

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
