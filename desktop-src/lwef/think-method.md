---
title: Think-Methode
description: Think-Methode
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c535912962a51961ae3f88f5cca412a55ecfa27506442aa78274fe697f2d7a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975510"
---
# <a name="think-method"></a>Think-Methode

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Zeigt den angegebenen Text für das angegebene Zeichen in einem "Thought"-Wortsprechblasen an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Think_ *  \[ *Text*\]



| Teil   | BESCHREIBUNG                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | Optional. Eine Zeichenfolge, die die Gedankenausgabe des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wie die [**Speak-Methode**](speak-method.md) ist die **Think-Methode** eine Anforderung in der Warteschlange, die Text in einem Wortsprechblasen anzeigt, mit der Ausnahme, dass sich der Think **Word-Balloon** visuell unterscheidet. Darüber hinaus unterstützt der Balloon nur das Lesezeichen-Sprachsteuerungstag (**\\ Mrk**) und ignoriert alle anderen Sprachsteuerungstags. Im **Gegensatz zu Speak** ändert die **Think-Methode** den Animationszustand des Zeichens nicht.

Die [**Eigenschaften des Balloon-Objekts**](/windows/desktop/lwef/the-balloon-object) wirken sich auf die Ausgabe der Methoden [**Speak und**](speak-method.md) **Think** aus. Beispielsweise muss die Enabled-Eigenschaft des **Balloon-Objekts** true sein, **damit** Text angezeigt wird. [](enabled-property.md)

Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Wenn die Datei nicht geladen wurde, legt der  Server außerdem die Status-Eigenschaft des [**Anforderungsobjekts**](status-property.md) mit einer entsprechenden Fehlercodenummer auf "failed" fest.

Der automatische Wortumbruch des Agents im Wort balloon unterbricht Wörter mithilfe von Leerzeichen (z. B. Leerzeichen oder Tabulator). Wenn dies jedoch nicht möglich ist, wird möglicherweise ein Wort an den Sprechblasen gepasst. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Aufbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) zwischen Zeichen ein, um logische Wörterumbrüche zu definieren.

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens fest, bevor Sie die [**Speak-Methode**](speak-method.md) verwenden, um eine geeignete Textanzeige im Wortsprechblasen zu gewährleisten.

 

 

 