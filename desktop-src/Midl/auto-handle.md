---
title: auto_handle-Attribut
description: Das Attribut \ Auto \_ handle \ ACF weist den Stub an, automatisch die Bindung für eine Funktion zu erstellen, die keinen expliziten Bindungs handle-Parameter hat. Beachten Sie, dass dieses Attribut veraltet ist und nicht mehr unterstützt wird.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471909"
---
# <a name="auto_handle-attribute"></a>Attribut für automatisches \_ handle

Das ACF-Attribut für **\[ automatische \_ Handles \]** weist den Stub an, automatisch die Bindung für eine Funktion einzurichten, die über keinen expliziten Bindungs handle-Parameter verfügt.

> [!Note]  
> Dieses Attribut ist veraltet und wird nicht mehr unterstützt. Die Verwendung des [**/robust**](-robust.md) -Schalters wird empfohlen.

 

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

*Interface-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die auf die gesamte Schnittstelle angewendet werden, z. b. [**Code**](code.md) oder [**NoCode**](nocode.md). Trennen Sie Schnittstellen Attribute durch Kommas.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Schnittstellen Definition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Attribut für **\[ Automatisches \_ handle \]** wird im Schnittstellen Header der ACF angezeigt. Sie wird auch im Schnittstellen Header der IDL-Datei angezeigt, wenn Sie den Mittelwert Compiler Switch [**/App \_ config**](-app-config.md)angeben.

Wenn der Client eine Funktion aufruft, die die automatische Bindung verwendet, und keine Bindung an einen Server vorhanden ist, richtet der Stub automatisch die Bindung ein. Die Bindung wird für nachfolgende Aufrufe anderer Funktionen in der-Schnittstelle wieder verwendet, die die automatische Bindung verwenden. Das Client Anwendungsprogramm muss keine Verarbeitung in Bezug auf das Bindungs handle deklarieren oder ausführen.

Wenn die ACF nicht vorhanden ist oder das [**\[ implizite \_ handle \]**](implicit-handle.md) -Attribut nicht enthält, verwendet der Mittell-Compiler das **\[ automatische \_ handle \]** und gibt eine Informations Meldung aus. Der mittlerer l-Compiler verwendet bei Bedarf auch das **\[ automatische \_ handle \]**, um die anfängliche Bindung für ein [**\[ Kontext \_ handle \]**](context-handle.md)herzustellen.

Das Attribut für **\[ Automatisches \_ handle \]** kann nur auftreten, wenn das [**\[ implizite \_ handle \]**](implicit-handle.md) oder das [**\[ explizite \_ handle \]**](explicit-handle.md) nicht auftritt. Das Attribut für **\[ Automatisches \_ handle \]** kann höchstens einmal im ACF-oder IDL-Schnittstellen Header auftreten.

> [!Note]  
> Wenn Sie Daten über Pipes verarbeiten, können Sie keine automatische Bindung verwenden (entweder mit dem Attribut "Automatisches **\[ \_ handle \]** " oder standardmäßig).

 

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

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/APP- \_ Konfiguration**](-app-config.md)
</dt> <dt>

[**Ordnung**](code.md)
</dt> <dt>

[**explizites \_ handle**](explicit-handle.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> </dl>

 

 




