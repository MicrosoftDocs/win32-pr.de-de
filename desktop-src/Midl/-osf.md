---
title: /osf-Switch
description: Der Schalter /osf erzwingt die strikte Kompatibilität mit OSF DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /osf switch MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb887997642b0d0ff81314d6cf81dc148e57547727a09b1fe646f04d0391f967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014118"
---
# <a name="osf-switch"></a>/osf-Switch

Der **Schalter /osf** erzwingt die strikte Kompatibilität mit OSF DCE.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Schalter verfügt über keine Parameter.

## <a name="remarks"></a>Hinweise

Verwenden Sie diesen Switch, wenn Ihre Anwendung aus Gründen der Portabilität eine strikte Kompatibilität mit OSF DCE erfordert.

Im **Modus /osf** wird das RpcSs-Paket automatisch aktiviert, wenn Sie vollständige Zeiger verwenden, die Argumente eine Speicherbelegung erfordern oder wenn Sie das [**Attribut enable \_ allocate**](enable-allocate.md) verwenden. Dies bedeutet, dass Sie die funktionen [**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) und [**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function) in Ihrer Client- und Serveranwendung nicht bereitstellen müssen.

Die folgenden erweiterten Microsoft-Features sind nicht verfügbar, wenn Sie mit dem Schalter **/osf** kompilieren:

-   Abstrakte Deklaratoren (unbenannte Parameter) in der IDL-Datei.
-   Schnittstellendefinitionen für COM-Objekte.
-   Schnittstellennamen mit mehr als 17 Zeichen.
-   Nur MIDL-Attribute, z. [**B. Wire \_ Marshal,**](wire-marshal.md) [**\_ Benutzer-Marshalling**](user-marshal.md)und die Typelib-Erweiterungen (ODL).
-   Verwenden von ACF-Schlüsselwörtern in einer IDL-Datei (midl **\_ /app-Konfigurationsoption).**
-   Statische Rückruffunktionen auf dem Client.
-   Das [**asynchrone**](async.md) Attribut.
-   [**cpp \_ quote**](cpp-quote.md) and **\# pragma midl \_ echo**.
-   [**wchar \_ t**](wchar-t.md) Breitzeichentypen, Konstanten und Zeichenfolgen.
-   [**Enumerationsinitialisierung**](enum.md) (Sparseenumeratoren).
-   [](out-idl.md)Out-Only-Größenangabe.
-   Zeiger mit gemischter Größe und Arrays mit gemischter Größe.
-   Ausdrücke, die für Größen- und Diskriminatorspezifizierer verwendet werden.
-   Explizite Handleparameter an einer beliebigen Position in der Argumentliste. Im **Modus /osf** sucht der MIDL-Compiler nach einem expliziten Bindungshandle als ersten Parameter. Wenn der erste Parameter kein Bindungshandle ist und mindestens ein Kontexthandle angegeben wird, wird das ganz links gelassene Kontexthandle als Bindungshandle verwendet. Wenn der erste Parameter kein Handle ist und keine Kontexthandles vorhanden sind, verwendet die Prozedur die implizite Bindung mit dem impliziten Handle des ACF-Attributs oder [**dem automatischen \_ Handle**](auto-handle.md). [**\_**](implicit-handle.md)
-   Zeigerattributtypvererbung. OSF DCE lässt keine nicht attributierten Zeiger zu. Daher muss jede IDL-Datei im **/osf-Modus** Attribute für ihre Zeiger definieren. Wenn ein Zeiger kein explizites Attribut besitzt, muss die IDL-Datei über eine [**\_ Zeigerstandardspezifikation**](pointer-default.md) verfügen, um den Zeigertyp festzulegen.
-   Mehrere Schnittstellen in einer IDL-Datei.
-   Definitionen außerhalb des Schnittstellenblocks.
-   Typqualifizierer wie **far** und **stdcall.**
-   Weglassen von direktionalen Attributen.

Die folgenden C/C++-Spracherweiterungen sind nicht verfügbar, wenn Sie mit dem Schalter **/osf** kompilieren:

-   Bitfelder in Strukturen und Unions.
-   Einzeilige Kommentare, die durch zwei Schrägstriche (/) getrennt sind.
-   Externe Deklarationen.
-   Prozeduren mit Ausellipsen in der Parameterliste.
-   Geben Sie [**int**](int.md)ein.
-   Geben Sie **void \** _ ein (mit Ausnahme des [*_context handle-Attributs). \_* *](context-handle.md)
-   Typqualifizierer, einschließlich des Formulars mit dem ANSI-konformen Präfix, enthalten zwei **\_ \_ Unterstriche: cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ export**, **export**, **\_ \_ far** **,** loadds , **\_ \_ loadds**, in **\_ \_ der** **Nähe** von , pascal , **\_ \_ pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volatile** und **volatile**.  
-   Alle \# [**Pragmawarnungen**](pragma.md) oder **\# Pragmakommentare.**
-   Typserialisierung.
-   Der [**\_ \_ int3264-Datentyp.**](--int3264.md)
-   Der Schalter [**/protocol**](-protocol.md) und die ndr64-Übertragungssyntax.

## <a name="examples"></a>Beispiele

**midl /osf filename.idl**

**midl /osf /app \_ config filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**\_/app-Konfiguration**](-app-config.md)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[Rpcss-Speicherverwaltungspaket](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 