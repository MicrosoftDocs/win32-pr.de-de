---
description: Konvertiert einen Gebiets Schema Namen in einen Gebiets Schema Bezeichner, der zum erhalten von Informationen aus dem Betriebssystem verwendet werden kann.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: Downlevellocalenametolcid-Funktion (nlsdl. h)
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
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364189"
---
# <a name="downlevellocalenametolcid-function"></a>Downlevellocalenametolcid-Funktion

Konvertiert einen Gebiets Schema [Namen](locale-names.md) in einen Gebiets Schema [Bezeichner](locale-identifiers.md) , der zum erhalten von Informationen aus dem Betriebssystem verwendet werden kann.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung erfordert ein Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) aufrufen, um einen Gebiets Schema Bezeichner abzurufen.

 

## <a name="syntax"></a>Syntax


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpname* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die einen Gebiets Schema [Namen](locale-names.md)darstellt.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flags, die den Typ des Namens angeben. Der Standardwert ist der Name des Gebiets Schema \_ \_ namens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung den Gebiets Schema Bezeichner zurück, der dem Gebiets Schema Namen entspricht.

Die Funktion gibt 0 zurück, wenn Sie nicht erfolgreich ist. Um erweiterte Fehlerinformationen abzurufen, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen, die einen der folgenden Fehlercodes zurückgeben kann:

-   \_ungültige \_ Flags. Die für Flags angegebenen Werte waren ungültig.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Funktion unterstützt keine neutralen Gebiets Schemas. Die entsprechende [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) -Funktion unterstützt [benutzerdefinierte](custom-locales.md)Gebiets Schemas, aber nur für Windows Vista und höher.

 

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

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
