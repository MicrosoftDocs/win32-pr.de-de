---
description: Bestimmt, ob ein durch den Namen angegebener Gebiets Schema auf dem Betriebssystem installiert oder unterstützt wird.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Rtlisvalidlocalename-Funktion (ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862452"
---
# <a name="rtlisvalidlocalename-function"></a>Rtlisvalidlocalename-Funktion

Bestimmt, ob ein durch den Namen angegebener Gebiets Schema auf dem Betriebssystem installiert oder unterstützt wird.

> [!Note]  
> Diese Funktion ist nur für die Verwendung in Windows Vista verfügbar. Sie wird möglicherweise in nachfolgenden Versionen geändert oder ist nicht verfügbar. Anwendungen sollten [**isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)verwenden.

 

## <a name="syntax"></a>Syntax


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Localename* \[ in\]
</dt> <dd>

Zu überprüfende Gebiets Schema [Name](locale-names.md) . Mit diesem Parameter kann der Name eines [benutzerdefinierten](custom-locales.md)Gebiets Schemas angegeben werden.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Flags, die angeben, ob neutrale Gebiets Schemata als gültig eingestuft werden. Derzeit ist das einzige definierte Flag " [locale \_ Allow \_ neutral](locale-allow-neutral.md)". Der Standardwert ist, dass dies nicht der Fall ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls 0.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ähnelt [**isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename). Der einzige Unterschied besteht darin, \_ dass \_ **rtlisvalidlocalename** für einen Namen, der einem neutralen Gebiets Schema (wie z. b. "en-US") entspricht, **true** zurück [**gibt,**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) wenn "locale Allow  neutral" festgelegt ist. Neutrale Gebiets Schemas werden als Teil der Strategie zum Laden von Ressourcen in Windows Vista und höher verwendet. Nur eine kleine Klasse von hoch spezialisierten Anwendungen verwendet **rtlisvalidlocalename** und Set locale \_ Allow \_ neutral, da neutrale Gebiets Schemas sehr eingeschränkt verwendet werden. Keine der Funktionen, die unter [Aufrufen der "locale Name"-Funktion](calling-the--locale-name--functions.md) beschrieben werden, akzeptiert neutrale Gebiets Schemas als Eingaben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ntrtl. h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> <dt>

[**Isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




