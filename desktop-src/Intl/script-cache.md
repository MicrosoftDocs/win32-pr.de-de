---
description: Definiert einen uniscrikcache für Schriftart Metrik.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350074"
---
# <a name="script_cache"></a>Skript \_ Cache

Definiert einen uniscrikcache für Schriftart Metrik.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Bemerkungen

Dies ist eine nicht transparente Struktur. Die Anwendung muss eine Skript \_ Cache Variable für jeden verwendeten Zeichenstil zuordnen und beibehalten. Die Variable muss mit **null** initialisiert werden.

Viele Skriptfunktionen nehmen eine Kombination aus einem Hardware Geräte-Kontext Handle und einer Skript \_ Cache Variable auf. Uniscriversucht zunächst, mithilfe der Skript Cache Variable auf Schriftart Daten zuzugreifen \_ . Der Hardware Gerätekontext wird nur überprüft, wenn die erforderlichen Daten nicht bereits zwischengespeichert wurden.

Das Hardware Gerätekontext Handle kann als **null** an unischreiber übermittelt werden. Wenn die von unischreiber benötigten Daten bereits zwischengespeichert sind, wird auf den Gerätekontext nicht zugegriffen, und der Vorgang wird normal fortgesetzt.

Wenn der Gerätekontext als **null** und unischreiber aus irgendeinem Grund darauf zugreifen muss, gibt uniscriden Fehlercode E \_ Pending zurück. Dieser Code wird schnell zurückgegeben, sodass die Anwendung zeitaufwändige [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) -Aufrufe vermeiden kann.

## <a name="examples"></a>Beispiele

Das folgende Beispiel gilt für alle Funktionen, die eine Skript \_ Cache Variable und ein optionales Handle für einen Hardware Gerätekontext akzeptieren.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unischreiber](uniscribe.md)
</dt> <dt>

[Uniscristrukturen](uniscribe-structures.md)
</dt> <dt>

[Zwischenspeichern](caching.md)
</dt> </dl>

 

 
