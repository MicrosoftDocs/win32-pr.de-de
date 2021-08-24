---
description: Ruft den Gebietsschemanamen für das übergeordnete Element des angegebenen Gebietsschemas ab.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: DownlevelGetParentLocaleName-Funktion (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: af7580188c7ded31c80476509aef8a10ee83b1cb1f9767ca5819eed053f1ce87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898740"
---
# <a name="downlevelgetparentlocalename-function"></a>DownlevelGetParentLocaleName-Funktion

Ruft den [Gebietsschemanamen](locale-names.md) für das übergeordnete Element des angegebenen Gebietsschemas ab.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die unter Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert das Downloadpaket. Anwendungen, die nur auf Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) aufrufen, wobei *LCType* auf [LOCALE \_ SPARENT](locale-sparent.md)festgelegt ist.

 

## <a name="syntax"></a>Syntax


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gebietsschema* \[ In\]
</dt> <dd>

[Gebietsschemabezeichner](locale-identifiers.md) des Gebietsschemas. Sie können das [**MAKELCID-Makro**](/windows/desktop/api/Winnt/nf-winnt-makelcid) verwenden, um einen Gebietsschemabezeichner zu erstellen, oder einen der folgenden vordefinierten Werte verwenden.

-   [GEBIETSSCHEMA \_ INVARIANT](locale-invariant.md)
-   [\_ \_ GEBIETSSCHEMASYSTEMSTANDARD](locale-system-default.md)
-   [\_ \_ GEBIETSSCHEMABENUTZERSTANDARD](locale-user-default.md)

**Windows Vista und höher:** Die folgenden benutzerdefinierten Gebietsschemabezeichner werden ebenfalls unterstützt.

-   [LOCALE \_ CUSTOM \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UI \_ DEFAULT](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UNSPECIFIED](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, in dem die Funktion den Namen des übergeordneten Gebietsschemas oder einen der folgenden vordefinierten Werte abruft. Dieser Parameter wird auf **NULL** festgelegt, wenn *cchName* auf 0 festgelegt ist.

-   [LOCALE \_ NAME \_ INVARIANT](locale-name-constants.md)
-   [LOCALE \_ NAME \_ SYSTEM \_ DEFAULT](locale-name-constants.md)
-   [LOCALE \_ NAME \_ USER \_ DEFAULT](locale-name-constants.md)

</dd> <dt>

*cchName* \[ In\]
</dt> <dd>

Größe des Puffers, der durch *lpName* in UTF-16-Codepunkten angegeben wird. Der Wert 0 für diesen Parameter bewirkt, dass die Funktion den *lpName-Puffer* ignoriert und die Größe des Puffers in Zeichen (enthaltene NULL-Zeichen) zurückgibt, die für den Namen des übergeordneten Gebietsschemas erforderlich sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die Anzahl der UTF-16-Codepunkte im Gebietsschemanamen zurück, einschließlich des abschließenden NULL-Zeichens.

Diese Funktion gibt 0 zurück, wenn sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER: \_ \_ UNZUREICHENDER PUFFER. Eine angegebene Puffergröße war nicht groß genug, oder sie wurde fälschlicherweise auf **NULL** festgelegt.
-   FEHLER: \_ UNGÜLTIGER \_ PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Die erforderliche Headerdatei und DLL sind Teil des Downloads "Downlevel Data Mapping APIs" von Microsoft NLS, der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Downlevel-Datenzuordnungs-APIs von Microsoft NLS unterWindows XP mit SP2 und höher<br/>  |
| Header<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprachen](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Zuordnen von Gebietsschemadaten](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
