---
title: /OSF-Schalter
description: Der Schalter/OSF erzwingt eine strikte Kompatibilität mit OSF-DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /OSF-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038875"
---
# <a name="osf-switch"></a>/OSF-Schalter

Der Schalter **/OSF** erzwingt eine strikte Kompatibilität mit OSF-DCE.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diesen Switch, wenn Ihre Anwendung aus Gründen der Portabilität eine strikte Kompatibilität mit OSF-DCE erfordert.

Im **/OSF** -Modus wird das RPCSS-Paket automatisch aktiviert, wenn Sie vollständige Zeiger verwenden, die Argumente eine Speicher Belegung erfordern oder wenn Sie das Attribut " [**\_ zuordnen**](enable-allocate.md) " verwenden. Dies bedeutet, dass Sie in Ihrer Client-und Serveranwendung nicht die [**\_ Benutzer \_ Freihand**](/windows/desktop/Rpc/the-midl-user-free-function) -Funktionen für [**mittlere \_ Benutzer \_**](/windows/desktop/Rpc/the-midl-user-allocate-function) Zuordnungen und mittellose Benutzer angeben müssen.

Die folgenden von Microsoft erweiterten Features sind nicht verfügbar, wenn Sie mit dem **/OSF** -Schalter kompilieren:

-   Abstrakte Deklaratoren (unbenannte Parameter) in der IDL-Datei.
-   Schnittstellendefinitionen für COM-Objekte.
-   Schnittstellennamen mit mehr als 17 Zeichen.
-   Nur-Mittel-Attribute, z. b. [**Wire \_ Marshal**](wire-marshal.md), [**User \_ Marshal**](user-marshal.md)und die Export der Typbibliothek-Erweiterungen (ODL).
-   Verwenden von ACF-Schlüsselwörtern in einer IDL-Datei (die Option "Mittel l **/App \_ config** ").
-   Statische Rückruf Funktionen auf dem Client.
-   Das [**Async**](async.md) -Attribut.
-   [**cpp- \_ Anführungs**](cpp-quote.md) Zeichen und **\# pragma-Mittell- \_ Echo**.
-   [**WCHAR \_ t**](wchar-t.md) -breit Zeichen Typen,-Konstanten und-Zeichen folgen.
-   [](enum.md) enumerationsinitialisierung (Sparse-Enumeratoren).
-   Spezifikation für die [**out**](out-idl.md)-only-Größe.
-   Arrays mit gemischter Groß-und Größenanpassung.
-   Ausdrücke, die für Größen-und diskriminatorspezifiatoren verwendet werden.
-   Explizite handle-Parameter an einer beliebigen Position in der Argumentliste. Im **/OSF** -Modus sucht der mittlerer l-Compiler nach einem expliziten Bindungs Handle als ersten Parameter. Wenn der erste Parameter kein Bindungs Handle und mindestens ein Kontext Handle angegeben ist, wird das äußerste Kontext Handle als Bindungs Handle verwendet. Wenn der erste Parameter kein Handle ist und keine Kontext Handles vorhanden sind, verwendet die Prozedur die implizite Bindung mithilfe des [**impliziten \_ Handles**](implicit-handle.md) oder [**automatischen \_ Handles**](auto-handle.md)des ACF-Attributs.
-   Vererbung von Zeiger Attributen. Die OSF-DCE lässt keine nicht attributierten Zeiger zu. Daher muss jede IDL-Datei im **/OSF** -Modus Attribute für Ihre Zeiger definieren. Wenn ein Zeiger über kein explizites Attribut verfügt, muss die IDL-Datei eine [**Zeiger \_ Standard**](pointer-default.md) Spezifikation aufweisen, um den Zeigertyp festzulegen.
-   Mehrere Schnittstellen in einer IDL-Datei.
-   Definitionen außerhalb des Schnittstellen Blocks.
-   Typqualifizierer wie " **Far** " und " **StdCall"**.
-   Weglassen von direktionalen Attributen.

Die folgenden C/C++-Spracherweiterungen sind nicht verfügbar, wenn Sie die Kompilierung mit dem **/OSF** -Schalter durchlaufen:

-   Bitfelder in Strukturen und Unions.
-   Einzeilige Kommentare sind durch zwei Schrägstriche (//) getrennt.
-   Externe Deklarationen.
-   Prozeduren mit Ellipsen in der Parameterliste.
-   Geben Sie [**int**](int.md)ein.
-   Geben **Sie \* void** ein (außer mit dem [**Kontext \_ handle**](context-handle.md) -Attribut).
-   Typqualifizierer, einschließlich des Formulars mit dem ANSI-konforme Präfix, enthalten zwei Unterstriche: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Export**, **Export**, **\_ \_ weit**, **weit**, **\_ \_ loadds**, **loadds**, **\_ \_ near**, **near**, **\_ \_ Pascal**, **Pascal**, **\_ \_ StdCall,** **StdCall,** **\_ \_ volatile** und **volatile**.
-   Eine beliebige \# [**pragma**](pragma.md) -Warnung oder ein **\# pragma** -Kommentar.
-   Typserialisierung.
-   Der [**\_ \_ int3264**](--int3264.md) -Datentyp.
-   Der [**/Protocol**](-protocol.md) -Switch und die ndr64-Übertragungs Syntax.

## <a name="examples"></a>Beispiele

**Mittel l/OSF Dateiname. idl**

**Mittel l/OSF/APP \_ Konfigurations Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/APP- \_ Konfiguration**](-app-config.md)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[RPCSS-Speicher Verwaltungspaket](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 