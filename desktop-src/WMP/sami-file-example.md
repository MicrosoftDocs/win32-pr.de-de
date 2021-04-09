---
title: Beispiel für Sami-Datei
description: Beispiel für Sami-Datei
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Dateien
- Samisch (synchronisierter, zugänglicher Medienaustausch), Dateien
- Synchronisierter, barrierefreier Medienaustausch (Sami), Beispielcode
- Samisch (synchronisierter, zugänglicher Medienaustausch), Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869387"
---
# <a name="sami-file-example"></a>Beispiel für Sami-Datei

Der folgende Beispielcode ist eine vollständige Sami-Datei mit einem Satz von Closed Caption Text und mehreren Klassen Deklarationen für Textformat und Beschriftung Language.


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



Stile, die in einer Sami-Datei definiert sind, entsprechen der Standard-CSS-Selektor-Syntax für Elemente, Klassen und IDs. Im Body-Element haben alle p-Elemente den Stil, der für die P-Elementauswahl im Style-Element definiert ist. Das Class-Attribut eines-Elements gibt die Sprache dieses Elements gemäß der Definition durch die Klassenselektoren im Style-Element an (die Selektoren, die mit Zeiträumen beginnen). Die von den Klassenselektoren angegebenen Sprachnamen können eine beliebige Zeichenfolge sein. Für Elemente mit dem angegebenen ID-Attribut wird eine zusätzliche Formatierung angewendet, wie von den ID-Selektoren im Style-Element angegeben (die Selektoren mit vorangestelltem \# Zeichen).

Bei Verwendung in Verbindung mit dem Windows Media Player-Objektmodell entsprechen die Klassenselektoren den *closedcaption*. **Samilang** -Eigenschaft, die zum Angeben der Sprache der Beschriftungen verwendet werden kann. Die ID-Selektoren entsprechen *closedcaption*. **Samistyle** -Eigenschaft, die verwendet werden kann, um den Stil anzugeben, in dem die Beschriftungen angezeigt werden.

Weitere Informationen zum Erstellen von SAMI-Dateien finden Sie unter Understanding SAMI 1,0 auf der [Microsoft-Website](/documentation/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 