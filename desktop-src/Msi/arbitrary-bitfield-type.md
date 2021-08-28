---
description: Der &\# 0034; Bitfield&0034; geben Sie ohne Kontextanforderungen ein, dass der Benutzer eine ganze Zahl angibt, deren Wert verwendet wird, um ein oder mehrere Bits in einem \# Bitfeld zu setzen. Dieser Text kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Beliebiger Bitfeldtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521889ffb1677bed249a92f757556a2fdbe36768
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884581"
---
# <a name="arbitrary-bitfield-type"></a>Beliebiger Bitfeldtyp

Der Typ "Bitfield" ohne Kontextanforderungen, dass der Benutzer eine ganze Zahl angibt, deren Wert verwendet wird, um ein oder mehrere Bits in einem Bitfeld zu setzen. Dieser Text kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist.

Der Beliebige Bitfeldtyp des [semantischen Typs](semantic-types.md) ist einer der Bitfield-Typen. Dieser Typ besteht aus einer ganzen Zahl, die vom Benutzer aus einer Reihe von Auswahlmöglichkeiten ausgewählt wird. Das Mergetool ersetzt die ausgewählte ganze Zahl in die Vorlagen, die in der Spalte Wert der [ModuleSubs integer -Tabelle angegeben sind.](modulesubstitution-table.md) Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des Elements in die Spalte Name eingeben, "3" in die Spalte Format eingeben, die Spalte Typ leer lassen und die Liste der möglichen ganzen Zahlen in der ContextData -Spalte der [ModuleConfiguration-Tabelle eingeben.](moduleconfiguration-table.md)

Die Spalte Typ ist reserviert und muss NULL sein. Der Eintrag in der ContextData-Spalte für alle Bitfield Format-Typen muss das Format " &lt; mask &gt; &lt; ; Name &gt; = &lt; value &gt; ; &lt; Name value ...", wobei mask ein ganzzahliger Wert ist, der die bits of interest angibt, Name ist ein lokalisierbarer Anzeigename für die Auswahl, und value ist ein dezimaler &gt; = &lt; &gt; &lt; &gt; &lt; &gt; ganzzahliger &lt; &gt; Wert. Die Kontextspalte wird im [CMSM-Sonderformat und](cmsm-special-format.md) für alle Bitfeldtypen verwendet. Ein Literalzeichen "=" oder ";" kann in das Feld Name eingegeben werden, indem ihm ein schräger Schrägstrich &lt; &gt; (' \\ ') vorangestellt wird.

 

 



