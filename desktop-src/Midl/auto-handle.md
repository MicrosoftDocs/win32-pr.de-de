---
title: auto_handle-Attribut
description: Das \_ ACF-Attribut \auto handle\ weist den Stub an, automatisch die Bindung für eine Funktion einzurichten, die keinen expliziten Bindungshandleparameter besitzt. Hinweis Dieses Attribut ist veraltet und wird nicht mehr unterstützt.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle-Attribut MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1f42a2fb643a2ce643437aad73b13c6e55d3462e92f9ce52ba208c6dc5cb68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807883"
---
# <a name="auto_handle-attribute"></a>\_Attribut für automatisches Handle

Das ACF-Attribut für das **\[ automatische \_ Handle \]** weist den Stub an, die Bindung für eine Funktion ohne expliziten Bindungshandleparameter automatisch einzurichten.

> [!Note]  
> Dieses Attribut ist veraltet und wird nicht mehr unterstützt. Die Verwendung des Schalters [**/robust**](-robust.md) wird empfohlen.

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*interface-attribute-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Schnittstelle als Ganzes gelten, z. B. [**Code**](code.md) oder [**Nocode.**](nocode.md) Trennen Sie Schnittstellenattribute durch Kommas.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Schnittstellendefinition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der Schnittstelle bilden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Attribut für das **\[ automatische \_ Handle \]** wird im Schnittstellenheader des ACF angezeigt. Sie wird auch im Schnittstellenheader der IDL-Datei angezeigt, wenn Sie den MIDL-Compilerschalter [**/app \_ config**](-app-config.md)angeben.

Wenn der Client eine Funktion aufruft, die die automatische Bindung verwendet und keine Bindung an einen Server vorhanden ist, richtet der Stub die Bindung automatisch ein. Die Bindung wird für nachfolgende Aufrufe anderer Funktionen in der -Schnittstelle wiederverwendet, die die automatische Bindung verwenden. Das Clientanwendungsprogramm muss keine Verarbeitung im Zusammenhang mit dem Bindungshandle deklarieren oder ausführen.

Wenn der ACF nicht vorhanden ist oder das [**\[ implizite \_ \] Handleattribut**](implicit-handle.md) nicht enthält, verwendet der MIDL-Compiler **\[ das automatische \_ Handle \]** und gibt eine Informationsmeldung aus. Der MIDL-Compiler verwendet bei Bedarf auch das **\[ automatische \_ Handle, \]** um die anfängliche Bindung für ein [**\[ \_ Kontexthandle \]**](context-handle.md)einzurichten.

Das **\[ Attribut für das automatische \_ \] Handle** kann nur auftreten, wenn das [**\[ implizite \_ Handle \]**](implicit-handle.md) oder das [**\[ explizite \_ \] Handleattribut**](explicit-handle.md) nicht auftritt. Das Attribut für das **\[ automatische \_ Handle \]** kann höchstens einmal im ACF- oder IDL-Schnittstellenheader auftreten.

> [!Note]  
> Sie können die automatische Bindung nicht verwenden (entweder mit dem Attribut für das **\[ automatische \_ Handle \]** oder standardmäßig), wenn Sie Daten über Pipes verarbeiten.

 

## <a name="examples"></a>Beispiele

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**\_/app-Konfiguration**](-app-config.md)
</dt> <dt>

[**Code**](code.md)
</dt> <dt>

[**Explizites \_ Handle**](explicit-handle.md)
</dt> <dt>

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[**Implizites \_ Handle**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> </dl>

 

 




