---
title: Allgemeine MIDL-Befehlszeilensyntax
description: Der MIDL-Compiler verarbeitet eine IDL-Datei und eine optionale Anwendungskonfigurationsdatei (Application Configuration File, ACF), um eine Reihe von Ausgabedateien zu generieren.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- Befehlszeilenreferenz MIDL , allgemeine Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3d3ded263237dffa425cebe3dea49b169e3494045cfc8b0d27cc249c5ebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384263"
---
# <a name="general-midl-command-line-syntax"></a>Allgemeine MIDL-Befehlszeilensyntax

Der MIDL-Compiler verarbeitet eine IDL-Datei und eine optionale Anwendungskonfigurationsdatei (Application Configuration File, ACF), um eine Reihe von Ausgabedateien zu generieren. Die in der Schnittstellenattributliste der IDL-Datei angegebenen Attribute bestimmen, ob der Compiler Quelldateien für eine RPC-Schnittstelle oder für eine benutzerdefinierte OLE-Schnittstelle generiert.

## <a name="switch-options"></a>Optionen wechseln

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*Befehlszeilenschalter*
</dt> <dd>

Gibt MIDL-Compilerbefehlszeilenschalter an. Schalter können in beliebiger Reihenfolge angezeigt werden.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*
</dt> <dd>

Gibt optionen an, die den einzelnen Schaltern zugeordnet sind. Gültige Optionen werden im Verweiseintrag für jeden MIDL-Compilerschalter beschrieben.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Gibt den Namen der IDL-Datei an. Diese Datei hat in der Regel die Erweiterung .idl, kann aber eine andere oder keine haben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In den folgenden Listen werden die Standardnamen der Dateien angezeigt, die für eine IDL-Datei mit dem Namen Name.idl generiert wurden. Sie können Befehlszeilenschalter verwenden, um diese Standardnamen zu überschreiben. Beachten Sie, dass der Name der IDL-Datei eine andere Erweiterung als .idl oder gar keine Erweiterung aufweisen kann.

Standardmäßig (d. h. wenn die Schnittstellenattributliste das [**Objekt**](object.md) oder [**das lokale**](local.md) Attribut nicht enthält), generiert der Compiler die folgenden Dateien für eine [RPC-Schnittstelle:](files-generated-for-an-rpc-interface.md)

-   Clientstub (Name \_ c.c)
-   Serverstub (Name \_ s.c)
-   Headerdatei (name.h)

Wenn [](object.md) das Objektattribut in der Schnittstellenattributliste angezeigt wird, generiert der Compiler die folgenden Dateien für eine COM-Schnittstelle:

-   Schnittstellenproxydatei (Name \_ p.c)
-   Schnittstellenheaderdatei (name.h)
-   Schnittstellen-UUID-Datei (Name \_ I.c)

Wenn das [**lokale**](local.md) Attribut in der Schnittstellenattributliste angezeigt wird, generiert der Compiler nur die Schnittstellenheaderdatei Name.h.

Der mit Microsoft RPC bereitgestellte MIDL-Compiler ruft den C-Präprozessor nach Bedarf auf, um die IDL-Datei zu verarbeiten. Der C-Compiler wird nicht automatisch aufgerufen, um generierte Dateien zu kompilieren.

> [!Note]  
> Der mit Microsoft RPC bereitgestellte MIDL-Compiler verwendet eine andere Befehlszeilensyntax als der DCE-IDL-Compiler.

 

Die MIDL-Compilerschalter [**/env,**](-env.md) [**/server,**](-server.md) [**/sstub**](-sstub.md)und [**/out**](-out.md) wirken sich auf die Serverstubdatei aus.

Ab MIDL-Version 6.0.359 ist die Standardbefehlszeilenoption für den MIDL-Compiler [**/Oicf**](-oi.md)Â [**/robust**](-robust.md). Um /robust zu deaktivieren, geben Sie die Option [**/no \_ robust**](-no-robust.md) an.

## <a name="the-header-file"></a>Die Headerdatei

Die Headerdatei enthält Definitionen aller Datentypen und Vorgänge, die in der IDL-Datei deklariert sind. Die Headerdatei muss von allen Anwendungsmodulen eingeschlossen werden, die die definierten Vorgänge aufrufen, die definierten Vorgänge implementieren oder die definierten Typen bearbeiten.

Die MIDL-Compilerschalter [**/header**](-header.md) und [**/out**](-out.md) wirken sich auf die Headerdatei aus.

 

 




