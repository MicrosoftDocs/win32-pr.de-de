---
title: Allgemeine Syntax der Mittell-Befehlszeile
description: Der mittlerer l-Compiler verarbeitet eine IDL-Datei und eine optionale Anwendungs Konfigurationsdatei (ACF), um einen Satz von Ausgabedateien zu generieren.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- Befehlszeilen Referenz-Mittell, allgemeine Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856844"
---
# <a name="general-midl-command-line-syntax"></a>Allgemeine Syntax der Mittell-Befehlszeile

Der mittlerer l-Compiler verarbeitet eine IDL-Datei und eine optionale Anwendungs Konfigurationsdatei (ACF), um einen Satz von Ausgabedateien zu generieren. Die in der Schnittstellen Attribut Liste der IDL-Datei angegebenen Attribute bestimmen, ob der Compiler Quelldateien für eine RPC-Schnittstelle oder für eine benutzerdefinierte OLE-Schnittstelle generiert.

## <a name="switch-options"></a>Optionen wechseln

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*Befehls Zeilenschalter*
</dt> <dd>

Gibt Befehls Zeilenschalter für Mittel-Compiler an. Switches können in beliebiger Reihenfolge angezeigt werden.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*Switch-Optionen*
</dt> <dd>

Gibt die jedem Switch zugeordneten Optionen an. Gültige Optionen werden im Verweis Eintrag für jeden Mittelpunkt-Compilerschalter beschrieben.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Gibt den Namen der IDL-Datei an. Diese Datei weist in der Regel die Erweiterung. idl auf, Sie kann jedoch auch einen anderen Wert oder keinen enthalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In den folgenden Listen sind die Standardnamen der Dateien aufgeführt, die für eine IDL-Datei namens. IDL generiert werden. Sie können Befehls Zeilenschalter verwenden, um diese Standardnamen zu überschreiben. Beachten Sie, dass der Name der IDL-Datei eine andere Erweiterung als IDL oder keine Erweiterung aufweisen kann.

Standardmäßig generiert der Compiler die folgenden Dateien für eine [RPC-Schnittstelle](files-generated-for-an-rpc-interface.md), wenn die Schnittstellen Attribut Liste das [**Objekt**](object.md) oder das [**lokale**](local.md) Attribut nicht enthält.

-   Client-Stub (Name \_ c. c)
-   Server-Stub (Name \_ s. c)
-   Header Datei (Name. h)

Wenn das [**Objekt**](object.md) Attribut in der Liste der Schnittstellen Attribute angezeigt wird, generiert der Compiler die folgenden Dateien für eine COM-Schnittstelle:

-   Schnittstellen Proxy Datei (Name \_ p. c)
-   Schnittstellen Header Datei (Name. h)
-   Interface UUID-Datei (Name \_ I. c)

Wenn das [**lokale**](local.md) Attribut in der Liste der Schnittstellen Attribute angezeigt wird, generiert der Compiler nur die Schnittstellen Header Datei namens. h.

Der von Microsoft RPC bereitgestellte mittlerer l-Compiler ruft den C-Präprozessor nach Bedarf auf, um die IDL-Datei zu verarbeiten. Der C-Compiler wird nicht automatisch aufgerufen, um generierte Dateien zu kompilieren.

> [!Note]  
> Der mit Microsoft RPC bereitgestellte mittlerer l-Compiler verwendet eine andere Befehlszeilen Syntax als der DCE-IDL-Compiler.

 

Der-Compilerschalter [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)und [**/out**](-out.md) wirkt sich auf die Server-Stub-Datei aus.

Beginnend mit der 6.0.359-Mittell-Version ist die standardmäßige Befehlszeilenoption für den-Mittell-Compiler [**/Oicf**](-oi.md)- [**/robust**](-robust.md). Um/robust zu deaktivieren, geben Sie die [**/No \_ robust**](-no-robust.md) -Option an.

## <a name="the-header-file"></a>Die Header Datei

Die Header Datei enthält Definitionen aller in der IDL-Datei deklarierten Datentypen und Vorgänge. Die Header Datei muss von allen Anwendungsmodulen eingeschlossen werden, die die definierten Vorgänge aufzurufen, die definierten Vorgänge implementieren oder die definierten Typen bearbeiten.

Die Mittel-Compilerschalter [**/Header**](-header.md) und [**/out**](-out.md) wirken sich auf die Header Datei aus.

 

 




