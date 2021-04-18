---
description: Konvertiert einen Gebiets Schema Bezeichner in einen Gebiets Schema Namen.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: Downlevellcidtolocalename-Funktion (nlsdl. h)
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
ms.openlocfilehash: 2f8e4ce9763348cf765522ebbd624a6e82f1071a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350874"
---
# <a name="downlevellcidtolocalename-function"></a>Downlevellcidtolocalename-Funktion

Konvertiert einen Gebiets Schema [Bezeichner](locale-identifiers.md) in einen Gebiets Schema [Namen](locale-names.md).

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert ein Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, müssen [**lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) aufrufen, um einen Gebiets Schema Namen abzurufen.

 

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

Gebiets Schema  \[ in\]
</dt> <dd>

Der zu übersetzende Gebiets Schema Bezeichner. Sie können das [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) -Makro verwenden, um einen Gebiets Schema Bezeichner zu erstellen. Diese Funktion unterstützt keine neutralen Gebiets Schemas oder die folgenden spezifischen Gebiets Schema-Bezeichnerwerte.

-   [Standard für Gebiets Schema \_ System \_](locale-system-default.md)
-   [\_Standardbenutzer Name für locale \_](locale-user-default.md)
-   [\_benutzerdefinierter locale- \_ Standard](locale-custom-constants.md)
-   [benutzerdefinierte Benutzeroberflächen- \_ \_ \_ Standardeinstellung](locale-custom-constants.md)
-   [Gebiets Schema \_ Benutzer \_ definiert nicht angegeben](locale-custom-constants.md)

</dd> <dt>

*lpname* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Funktion den Gebiets Schema Namen abruft. Die-Funktion ruft **null** ab, wenn *cchName* auf 0 festgelegt ist.

</dd> <dt>

*cchName* \[ in\]
</dt> <dd>

Größe des Gebiets Schema namens Puffers in UTF-16-Code Punkten. Die Anwendung legt diesen Parameter auf 0 fest, um die erforderliche Größe des Gebiets Schema-namens Puffers zurückzugeben.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flags, die den Typ des abzurufenden namens angeben. Der Standardwert ist der Name des Gebiets Schemas auf der Ebene \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl von UTF-16-Code Punkten im Gebiets Schema Namen zurück, einschließlich des abschließenden NULL-Zeichens, wenn erfolgreich. Wenn die Funktion erfolgreich ausgeführt wird und der Wert von *cchName* 0 ist, ist der Rückgabewert die erforderliche Größe (einschließlich NULL Zeichen) in Zeichen für den Namen des Gebiets Schema namens.

Die Funktion gibt 0 zurück, wenn Sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   Fehler \_ beim \_ Puffer. Eine angegebene Puffergröße war nicht groß genug, oder Sie wurde falsch auf **null** festgelegt.
-   \_ungültige \_ Flags. Der Wert von ' *dwFlags* ' ist ungültig.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Funktion unterstützt keine [benutzerdefinierten](custom-locales.md)Gebiets Schemas.

 

Die erforderlichen Header Dateien und dll-Dateien sind Bestandteil des Downloads "Microsoft nls-downleveldatenmapping-APIs", der im [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)zur Verfügung steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                |
| Verteilbare Komponente<br/>          | Microsoft nls-Downlevel-Daten Mapping-APIs onwindows XP mit SP2 und lateral Order Windows Vista<br/> |
| Header<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> <dt>

[Zuordnung von Gebiets Schema Daten](mapping-locale-data.md)
</dt> <dt>

[**Lcidtolocalename**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
