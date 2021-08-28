---
description: Bestimmt, ob ein durch den Namen angegebenes Locale auf dem Betriebssystem installiert oder unterstützt wird.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: RtlIsValidLocaleName-Funktion (Ntrtl.h)
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
ms.openlocfilehash: 993d819324987fccdfb66c26343bccfb9a815606655a18ff1a1e43f9a2af0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130280"
---
# <a name="rtlisvalidlocalename-function"></a>RtlIsValidLocaleName-Funktion

Bestimmt, ob ein durch den Namen angegebenes Locale auf dem Betriebssystem installiert oder unterstützt wird.

> [!Note]  
> Diese Funktion ist nur für die Verwendung in Windows Vista verfügbar. Sie kann in nachfolgenden Versionen geändert oder nicht verfügbar sein. Anwendungen sollten [**IsValidLocaleName verwenden.**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)

 

## <a name="syntax"></a>Syntax


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LocaleName* \[ In\]
</dt> <dd>

[Der zu überprüfende Locale-Name.](locale-names.md) Dieser Parameter kann den Namen eines benutzerdefinierten [-Locales angeben.](custom-locales.md)

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Flags, die angeben, ob neutrale Locales als gültig angesehen werden. Derzeit ist LOCALE ALLOW NEUTRAL das einzige definierte [ \_ \_ Flag.](locale-allow-neutral.md) Der Standardwert ist, dass sie nicht sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ähnelt [**IsValidLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) Wenn LOCALE ALLOW NEUTRAL festgelegt ist, gibt \_ \_ **RtlIsValidLocaleName** **true** für einen Namen zurück, der einem neutralen Locale entspricht (z.B. "en"), während [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) **TRUE** nur für ein bestimmtes Locale (z. B. "en-US") zurückgibt. Neutrale Locales werden als Teil der Strategie zum Laden von Ressourcen in Windows Vista und höher verwendet. Nur eine kleine Klasse von hoch spezialisierten Anwendungen verwendet **RtlIsValidLocaleName** und legen LOCALE ALLOW NEUTRAL fest, da \_ \_ neutrale Locales nur sehr eingeschränkt verwendet werden. Keine der unter Aufrufen der [Locale Name-Funktionen](calling-the--locale-name--functions.md) beschriebenen Funktionen akzeptiert neutrale Locales als Eingaben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ntrtl.h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung der Landessprache](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




