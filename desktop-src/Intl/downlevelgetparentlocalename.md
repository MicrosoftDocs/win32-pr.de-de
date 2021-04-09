---
description: Ruft den Gebiets Schema Namen für das übergeordnete Element des angegebenen Gebiets Schemas ab.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: Downlevelgetparameentlocalename-Funktion (nlsdl. h)
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
ms.openlocfilehash: d3a556d68c33249d2e6b49c48035cc58d8bac8e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960568"
---
# <a name="downlevelgetparentlocalename-function"></a>Downlevelgetparameentlocalename-Funktion

Ruft den Gebiets Schema [Namen](locale-names.md) für das übergeordnete Element des angegebenen Gebiets Schemas ab.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung von erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) mit *LCTYPE* aufrufen, der auf [locale \_ sparent](locale-sparent.md)festgelegt ist.

 

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

Gebiets Schema  \[ in\]
</dt> <dd>

Gebiets Schema [Bezeichner](locale-identifiers.md) des Gebiets Schemas. Sie können das [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro verwenden, um einen Gebiets Schema Bezeichner zu erstellen, oder einen der folgenden vordefinierten Werte verwenden.

-   [Gebiets Schema \_ invariant](locale-invariant.md)
-   [Standard für Gebiets Schema \_ System \_](locale-system-default.md)
-   [\_Standardbenutzer Name für locale \_](locale-user-default.md)

**Windows Vista und höher:** Die folgenden benutzerdefinierten Gebiets Schema Bezeichner werden ebenfalls unterstützt.

-   [\_benutzerdefinierter locale- \_ Standard](locale-custom-constants.md)
-   [benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung](locale-custom-constants.md)
-   [Gebiets Schema \_ Benutzer \_ definiert nicht angegeben](locale-custom-constants.md)

</dd> <dt>

*lpname* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem die Funktion den übergeordneten Gebiets Schema Namen oder einen der folgenden vordefinierten Werte abruft. Dieser Parameter ist auf **null** festgelegt, wenn *cchName* auf 0 festgelegt ist.

-   [Gebiets Schema \_ Name \_ invariant](locale-name-constants.md)
-   [Standardwert des Gebiets Schema \_ namens \_ Systems \_](locale-name-constants.md)
-   [\_Standard Name \_ des Gebiets Schemas \_](locale-name-constants.md)

</dd> <dt>

*cchName* \[ in\]
</dt> <dd>

Größe des von *lpname* festgelegten Puffers in UTF-16-Code Punkten. Der Wert 0 für diesen Parameter bewirkt, dass die Funktion den *lpname* -Puffer ignoriert und die Größe des Puffers (in Zeichen (NULL Zeichen eingeschlossen) zurückgibt, der den übergeordneten Gebiets Schema Namen enthalten muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von UTF-16-Code Punkten im Gebiets Schema Namen zurück, einschließlich des abschließenden NULL-Zeichens, wenn erfolgreich.

Diese Funktion gibt 0 (null) zurück, wenn Sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ beim \_ Puffer. Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Microsoft nls-Downlevel-Daten Mapping-APIs onwindows XP mit SP2 und höher<br/>  |
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

 

 
