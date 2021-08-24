---
description: Konvertiert einen Gebietsschemabezeichner in einen Gebietsschemanamen.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: DownlevelLCIDToLocaleName-Funktion (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b96d0c983c46c5d16007aae3a59659099a48855048194153d0c8102d26dc5bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898720"
---
# <a name="downlevellcidtolocalename-function"></a>DownlevelLCIDToLocaleName-Funktion

Konvertiert einen [Gebietsschemabezeichner](locale-identifiers.md) in einen [Gebietsschemanamen.](locale-names.md)

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die unter Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert ein Downloadpaket. Anwendungen, die nur auf Windows Vista und höher ausgeführt werden, sollten [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) aufrufen, um einen Gebietsschemanamen abzurufen.

 

## <a name="syntax"></a>Syntax


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gebietsschema* \[ In\]
</dt> <dd>

Der zu übersetzende Gebietsschemabezeichner. Sie können das [**MAKELCID-Makro**](/windows/desktop/api/Winnt/nf-winnt-makelcid) verwenden, um einen Gebietsschemabezeichner zu erstellen. Diese Funktion unterstützt keine neutralen Gebietsschemas oder die folgenden spezifischen Gebietsschemabezeichnerwerte.

-   [\_ \_ GEBIETSSCHEMASYSTEMSTANDARD](locale-system-default.md)
-   [\_ \_ GEBIETSSCHEMABENUTZERSTANDARD](locale-user-default.md)
-   [LOCALE \_ CUSTOM \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UI \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UNSPECIFIED](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion den Gebietsschemanamen abruft. Die Funktion ruft **NULL** ab, wenn *cchName* auf 0 festgelegt ist.

</dd> <dt>

*cchName* \[ In\]
</dt> <dd>

Größe des Gebietsschemanamenpuffers in UTF-16-Codepunkten. Die Anwendung legt diesen Parameter auf 0 fest, um die erforderliche Größe des Gebietsschemanamenpuffers zurückzugeben.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die den Typ des abzurufenden Namens angeben. Der Standardwert ist DOWNLEVEL \_ LOCALE \_ NAME.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Anzahl der UTF-16-Codepunkte im Gebietsschemanamen zurück, einschließlich des abschließenden NULL-Zeichens. Wenn die Funktion erfolgreich ist und der Wert von *cchName* 0 ist, ist der Rückgabewert die erforderliche Größe in Zeichen (einschließlich NULL-Zeichen) für den Gebietsschemanamenpuffer.

Die Funktion gibt 0 zurück, wenn sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER: \_ \_ UNZUREICHENDER PUFFER. Eine angegebene Puffergröße war nicht groß genug, oder sie wurde fälschlicherweise auf **NULL** festgelegt.
-   FEHLER: \_ UNGÜLTIGE \_ FLAGS. Der Wert von *dwFlags* ist ungültig.
-   FEHLER: \_ UNGÜLTIGER \_ PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Diese Funktion unterstützt keine [benutzerdefinierten Gebietsschemas.](custom-locales.md)

 

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

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
