---
title: Think-Methode
description: Think-Methode
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858207"
---
# <a name="think-method"></a>Think-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Zeigt den angegebenen Text für das angegebene Zeichen in der Wort Sprechblase "Thought" an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Think* *  \[ *Text*\]



| Teil   | BESCHREIBUNG                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | Dies ist optional. Eine Zeichenfolge, die die übergeordnete Ausgabe des Zeichens angibt. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wie bei der Sprech Methode ist die Methode " **Think** " eine Anforderung in der Warteschlange, die Text in einer Wort Sprechblase anzeigt, mit **dem Unterschied** , dass die [**Sprech Wort Sprech**](speak-method.md) Blase optisch anders Außerdem unterstützt die Sprechblase nur das Lesezeichen-Steuerelement Tag (**\\ MRK**) und ignoriert alle anderen sprachkontrolltags. Anders als bei " **sprechen**" ändert die " **Think** "-Methode nicht den Animations Zustand des Zeichens.

Die [**Eigenschaften des Sprechblasen Objekts wirken**](/windows/desktop/lwef/the-balloon-object) sich auf die Ausgabe der Methoden " [**sprechen**](speak-method.md) " und " **Think** " aus. Beispielsweise muss die [**aktivierte**](enabled-property.md) Eigenschaft des Sprech **Blasen Objekts "** **true** " sein, damit der Text angezeigt wird.

Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Wenn die Datei nicht geladen wurde, legt der Server außerdem die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlercode Nummer fest.

Die automatische Wörter Trennung des Agents in der Wort Sprechblase unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen oder Tabstopps). Wenn dies jedoch nicht möglich ist, kann es dazu kommen, dass ein Wort an die Sprechblase angepasst wird. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens vor der Verwendung der Sprech Methode fest, um die entsprechende Textanzeige innerhalb der Wort [**Sprech**](speak-method.md) Blase sicherzustellen.

 

 

 