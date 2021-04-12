---
description: Ruft den Gebiets Schema Bezeichner für das übergeordnete Element des angegebenen Gebiets Schemas ab.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: Downlevelgetparameentlocalelcid-Funktion (nlsdl. h)
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
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348148"
---
# <a name="downlevelgetparentlocalelcid-function"></a>Downlevelgetparameentlocalelcid-Funktion

Ruft den Gebiets Schema [Bezeichner](locale-identifiers.md) für das übergeordnete Element des angegebenen Gebiets Schemas ab.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung von erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCTYPE* aufrufen, der auf [locale \_ sparent](locale-sparent.md)festgelegt ist.

 

## <a name="syntax"></a>Syntax


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gebiets Schema  \[ in\]
</dt> <dd>

Gebiets Schema Bezeichner des Gebiets Schemas, für das der übergeordnete Gebiets Schema Bezeichner abgerufen wird Sie können das [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro verwenden, um einen Gebiets Schema Bezeichner zu erstellen, oder einen der folgenden vordefinierten Werte verwenden.

-   [Gebiets Schema \_ invariant](locale-invariant.md)
-   [Standard für Gebiets Schema \_ System \_](locale-system-default.md)
-   [\_Standardbenutzer Name für locale \_](locale-user-default.md)

**Windows Vista und höher:** Die folgenden benutzerdefinierten Gebiets Schema Bezeichner werden ebenfalls unterstützt.

-   [\_benutzerdefinierter locale- \_ Standard](locale-custom-constants.md)
-   [benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung](locale-custom-constants.md)
-   [Gebiets Schema \_ Benutzer \_ definiert nicht angegeben](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den übergeordneten Gebiets Schema Bezeichner zurück, wenn erfolgreich, andernfalls 0. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Microsoft nls-Downlevel-Daten Mapping-APIs onwindows xpor Windows Vista<br/>     |
| Header<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> <dt>

[Zuordnung von Gebiets Schema Daten](mapping-locale-data.md)
</dt> <dt>

[**Getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
