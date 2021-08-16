---
description: Der &\# 0034; Bitfield&0034; geben Sie ohne Kontextanforderungen ein, dass der Benutzer eine ganze Zahl angibt, deren Wert verwendet wird, um ein oder mehrere Bits in einem \# Bitfeld zu setzen. Dieser Text kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Beliebiger Bitfeldtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842c9d1725b2bfe9ef0585cafd085ac1ceba33554899909ae3317af38fd7caac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381384"
---
# <a name="arbitrary-bitfield-type"></a>Beliebiger Bitfeldtyp

Der Typ "Bitfield" ohne Kontextanforderungen, dass der Benutzer eine ganze Zahl angibt, deren Wert verwendet wird, um ein oder mehrere Bits in einem Bitfeld zu setzen. Dieser Text kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist.

Der Beliebige Bitfeldtyp des [semantischen Typs](semantic-types.md) ist einer der Bitfield-Typen. Dieser Typ besteht aus einer ganzen Zahl, die vom Benutzer aus einer Reihe von Auswahlmöglichkeiten ausgewählt wird. Das Mergetool ersetzt die ausgewählte ganze Zahl in die Vorlagen, die in der Spalte Wert der [ModuleSubs integer -Tabelle angegeben sind.](modulesubstitution-table.md) Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des Elements in die Spalte Name eingeben, "3" in die Spalte Format eingeben, die Spalte Typ leer lassen und die Liste der möglichen ganzen Zahlen in der ContextData -Spalte der [ModuleConfiguration-Tabelle eingeben.](moduleconfiguration-table.md)

Die Spalte Typ ist reserviert und muss NULL sein. Der Eintrag in der ContextData-Spalte für alle Bitfield Format-Typen muss das Format " <mask> haben.<Name>=<value>;<Name>=<value>....", wobei ein ganzzahliger Wert ist, der die bits of interest angibt, ist ein <mask> <Name> lokalisierbarer Anzeigename für die Auswahl, und <value> ist ein ganzzahliger Dezimalwert. Die Kontextspalte wird im [CMSM-Sonderformat und](cmsm-special-format.md) für alle Bitfeldtypen verwendet. Ein Literalzeichen "=" oder ";" kann in das Feld eingegeben werden, indem ihm ein schräger Schrägstrich <Name> (' \\ ') vorangestellt wird.

 

 



