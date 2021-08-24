---
description: Ruft den Locale Identifier für das übergeordnete Element des angegebenen Locale ab.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: DownlevelGetParentLocaleLCID-Funktion (Nlsdl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 64cefdf4cc2a2c522a8295ab44e1810f0364d706d378979637700a7a3b72343a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765440"
---
# <a name="downlevelgetparentlocalelcid-function"></a>DownlevelGetParentLocaleLCID-Funktion

Ruft den [Locale Identifier für](locale-identifiers.md) das übergeordnete Element des angegebenen Locale ab.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf vista-Windows ausgeführt werden. Die Verwendung erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) aufrufen, bei dem *LCType* auf [LOCALE \_ SPARENT festgelegt ist.](locale-sparent.md)

 

## <a name="syntax"></a>Syntax


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Locale* \[ In\]
</dt> <dd>

Der Locale-Bezeichner des Locale,für das der übergeordnete Locale-Bezeichner abgerufen werden soll. Sie können das [**MAKELCID-Makro**](/windows/desktop/api/Winnt/nf-winnt-makelcid) verwenden, um einen Locale Identifier zu erstellen, oder einen der folgenden vordefinierten Werte verwenden.

-   [LOCALE \_ INVARIANT](locale-invariant.md)
-   [LOCALE \_ SYSTEM \_ DEFAULT](locale-system-default.md)
-   [LOCALE \_ USER \_ DEFAULT](locale-user-default.md)

**Windows Vista und höher:** Die folgenden benutzerdefinierten Locale Identifiers werden ebenfalls unterstützt.

-   [BENUTZERDEFINIERTER \_ \_ LOCALE-STANDARDWERT](locale-custom-constants.md)
-   [STANDARDEINSTELLUNG DER \_ BENUTZERDEFINIERTEN \_ BENUTZEROBERFLÄCHE FÜR DAS LOCALE \_](locale-custom-constants.md)
-   [LOCALE \_ CUSTOM \_ UNSPECIFIED](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den übergeordneten Locale Identifier zurück, wenn erfolgreich, andernfalls 0. Um erweiterte Fehlerinformationen zu erhalten, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, wodurch einer der folgenden Fehlercodes zurückgegeben werden kann:

-   FEHLER \_ \_ UNGÜLTIGER PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Die erforderliche Headerdatei und DLL sind Teil des Downloads "Microsoft NLS Downlevel Data Mapping APIs", der im [Microsoft Download Center verfügbar ist.](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Microsoft NLS-APIs für die Datenzuordnung auf Windows XPor Windows Vista<br/>     |
| Header<br/>                   | <dl> <dt>Nlsdl.h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der Landessprache](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Zuordnen von Locale Data](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
