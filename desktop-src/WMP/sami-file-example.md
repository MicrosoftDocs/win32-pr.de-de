---
title: Beispiel für eine SAMI-Datei
description: Beispiel für eine SAMI-Datei
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Objektmodell, Synchronized Accessible Media Interchange (SAMI)
- Objektmodell,Synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player Mobiler, synchronisierter austauschbarer Medienaustausch (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Mobile ActiveX,Synchronized Accessible Media Interchange (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronized Accessible Media Interchange (SAMI),files
- SAMI (Synchronized Accessible Media Interchange), Files
- Synchronized Accessible Media Interchange (SAMI), Beispielcode
- SAMI (Synchronized Accessible Media Interchange), Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d4e2ab5189f99118afae3fb2dae7374323cc8c16605bb458a04bd31810ed91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569806"
---
# <a name="sami-file-example"></a>Beispiel für eine SAMI-Datei

Der folgende Beispielcode ist eine vollständige SAMI-Datei mit einem Satz von Untertiteltexten und mehreren Klassendeklarationen für Textformat und Beschriftungssprache.


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



In einer SAMI-Datei definierte Stile entsprechen der standardmäßigen CSS-Selektorsyntax für Elemente, Klassen und IDs. Im BODY-Element wird für alle P-Elemente der Stil definiert, der für die P-Elementauswahl im STYLE-Element definiert ist. Das Klassenattribut eines Elements gibt die Sprache dieses Elements an, wie von den Klassenauswahlen im STYLE-Element definiert (die Selektoren, die mit Zeiträumen beginnen). Die von den Klassenauswahlen angegebenen Sprachnamen können eine beliebige Zeichenfolge sein. Für Elemente mit dem angegebenen ID-Attribut werden zusätzliche Stile angewendet, wie durch die ID-Selektoren im STYLE-Element angegeben (die Selektoren mit Zeichen \# als Präfix).

Bei Verwendung in Verbindung mit dem Windows Media Player-Objektmodell entsprechen die Klassenauswahlen *closedCaption*. **SAMILang-Eigenschaft,** die verwendet werden kann, um die Sprache der Untertitel anzugeben. Die ID-Selektoren entsprechen *closedCaption*. **SAMIStyle-Eigenschaft,** die verwendet werden kann, um den Stil anzugeben, in dem die Beschriftungen angezeigt werden.

Weitere Informationen zum Erstellen von SAMI-Dateien finden Sie auf der [Microsoft-Website](/documentation/)unter Understanding SAMI 1.0 (Grundlegendes zu SAMI 1.0).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 